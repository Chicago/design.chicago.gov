---
layout: post
title: Using Google Translate for Internationalization
author: Abby Lammers
excerpt: The City of Chicago is exploring different strategies for web translation of City content. This demo was developed to test the viability of computer translation, specifically neural machine translation services (NMTS).
---

The City of Chicago is exploring different strategies for web translation of City content. This demo was developed to test the viability of computer translation, specifically neural machine translation services (NMTS); we've chosen to use Google Translate because it was the only out-of-the-box translation service to support Tagalog. After a bit of research and a bit of code, we have successfully shown how Google can be used to translate a static webpage into the six most commonly spoken languages in Chicago.

![GIF of translate demo](/assets/img/google-translate-demo.gif)

## Background

### Motivation

One of the chief roles of the Design Office is improving the accessibility and inclusion of government services. The new administration is pushing for better compliance with a 2015 [language access ordinance](https://www.chicago.gov/content/dam/city/depts/mayor/Office%20of%20New%20Americans/PDFs/Language%20Access%20Ordinance.pdf). As a result, the City of Chicago is developing a web content translation strategy for the six most commonly spoken languages in Chicago: English, Spanish, Polish, Arabic, Mandarin, and Tagalog. 

### Translation as a Service

The City of Chicago has a number of translation options available, ranging in quality, speed, and price. A high quality of translation requires human translation or human proofreading of computer translation. However, there is a trade-off between quality and speed: machine translation services like Google Translate provide translation nearly instantaneously, while human translation takes longer. 

### Neural Machine Translation Services

The City of Chicago has an enormous amount of digital content across a number of different websites. Translating web content isn't as easy as flipping a switch -- while new neural machine translation services (NMTS) can translate text quickly with some accuracy, there are certain caveats. Some phrases that are common on Chicago websites, like acronyms or department names, may be mistranslated by an out-of-the-box NMTS. To remedy this, human translators can create dictionaries of these special cases and help to train the NMTS to improve future translation. When content is written with metaphors or idioms, a NMTS may misrepresent the meaning. Human translators can help proofread NMTS translation to ensure high quality and readability in other languages. 

## Technical Deep-Dive

In this section I will break down the javascript behind this demo and discuss the limitations of this script. If you're a developer interested in using the Google Translate API for your own web content, this part is for you.

### The API Key

```js
API_KEY = "your-api-key"; // replace with google api key, available from google console project
```

Getting an API Key from Google was a bit more difficult than expected. I strongly recommend following the [Google codelabs tutorial](https://codelabs.developers.google.com/codelabs/cloud-translation-intro/index.html#0), specifically steps 2-5, to get started.

### The Translate Button

Clicking the translate button initiates the API call. All of the translation code happens inside the function:

```js
$("#translateButton").click(function () {...}
```

This function references the `#translateButton`, part of a form on the HTML side:

```
<form>
   <select id="targetLanguage">
    <option value="EN" selected="selected">English</option>
    <option value="ES">Spanish</option>
    <option value="PL">Polish</option>
    <option value="AR">Arabic</option>
    <option value="ZH">Mandarin</option>
    <option value="TL">Tagalog</option>
  </select>

  <input type="button" id="translateButton" value="Translate" />
</form>
```

### Constructing the API Call

Much of the structure of this section of code is adapted from [this stackoverflow post](https://stackoverflow.com/questions/50719010/google-translate-api-translate-page-using-js/51540211#51540211).

```js
// construct url to translate content in #translateText to the language selected by #targetLanguage 
var url = "https://translation.googleapis.com/language/translate/v2";
url += "/?key=" + API_KEY;
url += "&target=" + $("#targetLanguage").val(); // https://stackoverflow.com/questions/50719010/google-translate-api-translate-page-using-js
url += "&q=" + encodeURI($("#translateText").text()); // encodeURI converts strings to url-safe text
```

This script makes a POST to the the [translate endpoint](https://cloud.google.com/translate/docs/reference/rest/v2/translate) of the v2 translate API. 

As a newcomer to Javascript and `XMLHttpRequest()`, I found it easier to construct a URL manually than to add parameters with Javascript syntax. 

After concatenating the base URL and the API key parameter, the target language is included with `$("#targetLanguage").val();` 

Finally, the text to be translated, identified by the ID `#translateText`, is encoded and included. A more complete script would scan the DOM for text objects, make one API call containing all text to be translated, and replace all text objects.

### Sending & Receiving the Request

Opening and sending requests with `XMLHttpRequest()` is relatively straightforward. Accessing the data in those requests is a bit more complex. I relied heavily on [Tania Rascia's excellent API tutorial](https://www.taniarascia.com/how-to-connect-to-an-api-with-javascript/) in developing this part of the script.

```js
  var request = new XMLHttpRequest();
  request.open('POST', url);
  // after the request is complete, extract translated text and replace in the web page
  request.onload = function () {
    var data = JSON.parse(this.response);
    if (request.status >= 200 && request.status < 400) {
      $("#translateText").text(data.data.translations[0].translatedText);
    }
  }
  request.send();
```

The [`request.onload` event](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequestEventTarget/onload) occurs when the response is received from Google. At the time of `request.onload`, a function parses the response, checks to make sure the status is good, and then replaces the target text (`#translateText`) with the translated text. 

### Putting It All Together

The completed code is actually quite simple and short: 

```js
API_KEY = "your-api-key" // replace with google api key, available from google console project

// when the translate button is clicked, pull text from objects with ID "translateText" 
// and replace with a translated version.
$("#translateButton").click(function () {

  // construct url to translate content in #translateText to the language selected by #targetLanguage 
  var url = "https://translation.googleapis.com/language/translate/v2";
  url += "/?key=" + API_KEY;
  url += "&target=" + $("#targetLanguage").val(); // https://stackoverflow.com/questions/50719010/google-translate-api-translate-page-using-js
  url += "&q=" + encodeURI($("#translateText").text()); // encodeURI converts strings to url-safe text

  // POST to google translate api
  var request = new XMLHttpRequest();
  request.open('POST', url);
  // after the request is complete, extract translated text and replace in the web page
  request.onload = function () {
    var data = JSON.parse(this.response);
    if (request.status >= 200 && request.status < 400) {
      $("#translateText").text(data.data.translations[0].translatedText);
    }
  }
  request.send();
});

```
Of course, there's plenty of room for improvement. This demo is a minimal proof-of-concept for web-based translation. A more complete script would scan the DOM for text objects, make one API call containing all text to be translated, and replace all text objects. To ensure translation quality, the script could also send the source text for translation rather than the browser text, as the browser text can be translated back and forth between different languages and get a bit jumbled along the way.

Happy translating!