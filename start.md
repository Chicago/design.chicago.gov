---
title: Quick Start Guide
description: A guide to using Chicago Design System visual identity, code, and methods.
permalink: /start/

layout: page
sidenav:
  - text: Everyone
    href: '/start/#everyone'
  - text: City of Chicago Employees
    href: '/start/#city-of-chicago-employees'
  - text: Developers
    href: '/start/#developers'
  - text: Designers
    href: '/start/#designers'

---

## Getting Started with the Chicago Design System

The CDS is three things, as we mentioned on the home page. It's a visual identity system, a web user interface component library with code, and a design methods guide to help use design thinking to unlock creativity in your work. Let's look at each one in turn.

## Philosophy


### Visual assets

Chicago's 

### Code

The Chicago Design System is built upon the [United States Web Design System](https://v2.designsystem.digital.gov/) code and methods as a baseline.


### Methods & practices



## Everyone

Help make your city work better for all Chicagoans!

You can review our status on much of our work on [our roadmap](https://github.com/Chicago/design-projects/projects/1). The Chicago Design System itself will soon have an [independent product roadmap](https://github.com/Chicago/chicagodesignsystem.org/projects/1).




## City of Chicago Employees

Our [City of Chicago internal style guide is available online](https://cityofchicago.frontify.com/hub/2). Check it out! 

Interested in using this work in a technology project today? Have questions? We're here to help.

Email design.system at cityofchicago.org to connect.



## Developers

Developers: Follow the instructions below to get started. For a fuller account of how to use the CDS fork of USWDS, go [here](https://github.com/uswds/uswds).

### How to contribute to the Chicago Design System.

This quick start guide will walk you through cloning the GitHub repository, as well as installing  Jekyll and Fractal so you can start contributing to the Chicago Design System. Once you've made edits to your local forks, you can submit a pull request through git/GitHub, which may be merged with the main project after review.

To use the Design System on your project, you’ll need to reference the CSS (Cascading Style Sheets) and JavaScript files in each HTML page or dynamic templates in your project.

We offer both files, the CSS and the JavaScript, in two versions — a minified version, and an un-minified one. (In the examples above, we are using the minified files.) Use the minified files in a production environment or to reduce the file size of your downloaded assets. And the un-minified files are better if you are in a development environment or would like to debug the CSS or JavaScript assets in the browser.

And that’s it — you should now be able to copy our code samples into your index.html and start using the Design System.

You can get involved by giving us feedback, [writing an issue](https://github.com/Chicago/design-system/issues/new), or [finding other ways to contribute](https://opensource.guide/how-to-contribute/).

We communicate about this project in our [CDS Slack workspace](https://chicagodesignsystem.slack.com/messages). Request an invitation by emailing us at [Chicago Design System](mailto:design.system@cityofchicago.org) or using our [shared invite link](https://join.slack.com/t/chicagodesignsystem/shared_invite/enQtMzM2OTA4MTQyNzIzLWVlOWFkOWQ4YWE0NWQ2YTAzOTFmYWFlMGVjNTEwZjA5ZWNmYjFkZTNhNDNhMmM1MTJiYmQ3MDk2NWZkNzg2Mjg).


## GitHub

GitHub is used for version control of the Chicago Design System. To contribute to the project, you will fork a version of the pattern library to edit.

1. Navigate to the Chicago Design System Design Library repository [link](https://github.com/Chicago/design-library).
2. In the top-right corner of the page, click **Fork**.
3. You now have a forked copy of the original /Chicago/design-library repository. The next step is to make a local copy to edit.
4. Go to the **code** section of your fork.
5. Clock **Clone or download**
6. Copy the URL provided.
7. Open your command line or Terminal application and enter the directory where you would like to copy the repository.
8. Clone the repository with the command below by replacing `<URL>` with the fork URL you copied in the previous step. The repository will be cloned into a new directory in this location.
```
git clone <URL>
```
9. Navigate into the directory of the repository you just created with the command below.
```
cd design-library
```

<!-- ## Fractal

Fractal is used to publish the atomic design elements of the Chicago Design System. You will need to install the CDS Fractal fork in order to edit and preview your changes to the CDS pattern library. [Go here](https://fractal.build/guide) for more information on Fractal and [here](http://bradfrost.com/blog/post/atomic-web-design/) for more information on atomic design.

1. If you haven't already, install npm. npm is a package manager for Node based projects. Below is a link to find the install method that coincides with your operating system:
    * Node v4.2.3+, [Installation guides](https://nodejs.org/en/download/)
1. Navigate to the design-library directory
2. Run
```
npm install
```
3.  Run npm start to make sure it's up and running
```
npm start
```
4. Make changes to the components in the 'src' folder
5. Run 
```
npm install
```
6. Install [fractal](https://fractal.build/guide/cli)
```
npm i -g @frctl/fractal
``` 
7. Run fractal build to generate the static site
```
fractal build
``` 
8. Open the docs folder static site to make sure it generated correctly
9. Sync with the repo
10. Make a pull request
 -->

## Designers

Check out the [Getting Started for Designers](https://designsystem.digital.gov/getting-started/designers/) information.
## How To Contribute to the Chicago Design System.

This quick start guide will walk you through cloning the GitHub repository, as well as installing  Jekyll and Pattern Lab so you can start contributing to the Chicago Design System. Once you've made edits to your local forks, you can submit a pull request through git/GitHub, which may be merged with the main project after review.

You can get involved by giving us feedback, [writing an issue](https://github.com/Chicago/design-system/issues/new), or [finding other ways to contribute](https://opensource.guide/how-to-contribute/).

We communicate about this project in our [CDS Slack workspace](https://chicagodesignsystem.slack.com/messages). Request an invitation by emailing us at [Chicago Design System](mailto:design.system@cityofchicago.org) or using our [shared invite link](https://join.slack.com/t/chicagodesignsystem/shared_invite/enQtMzM2OTA4MTQyNzIzLWVlOWFkOWQ4YWE0NWQ2YTAzOTFmYWFlMGVjNTEwZjA5ZWNmYjFkZTNhNDNhMmM1MTJiYmQ3MDk2NWZkNzg2Mjg)..


## GitHub

GitHub is used for version control of the Chicago Design System. To contribute to the project, you will fork a version of the main repository to edit.

1. Navigate to the Chicago Design System repository [link](https://github.com/Chicago/design-system).
2. In the top-right corner of the page, click **Fork**.
3. You now have a forked copy of the original /Chicago/design-system repository. The next step is to make a local copy to edit.
4. Go to the **code** section of your fork.
5. Clock **Clone or download**
6. Copy the URL provided.
7. Open your command line or Terminal application and enter the directory where you would like to copy the repository.
8. Clone the repository with the command below by replacing `<URL>` with the fork URL you copied in the previous step. The repository will be cloned into a new directory in this location.
```
git clone <URL>
```
9. Navigate into the directory of the repository you just created with the command below.
```
cd design-system
```

## Jekyll

Jekyll is used to publish the Chicago Design System. You will need to install Jekyll in order to preview your changes to the main CDS repository site.

#### Mac Install

[Go here](https://jekyllrb.com/docs/quickstart/) for instructions on how to install Jekyll.

Once Jekyll is installed, navigate to the docs folder in the design-system respository and run:

```
bundle exec jekyll serve --baseurl ''
```

You can then pull up http://localhost:4000/ in your browser to see the design standards local clone.

<!---
#### Mac Install as submodule

1. Install Node.js via a package manager ([link](https://nodejs.org/en/download/package-manager/#macos))
2. Install the Pattern Lab submodule with the commands 
```
git submodule init
git submodule update
```

#### Mac Install

1. Install Node.js via a package manager ([link](https://nodejs.org/en/download/package-manager/#macos))
2. Navigate to the Chicago Design System Pattern Lab repository [link](https://github.com/Chicago/patternlab).
3. In the top-right corner of the page, click **Fork**.
4. You now have a forked copy of the original /Chicago/patternlab repository.
5. Go to the **code** section of your fork.
6. Clock **Clone or download**
7. Copy the URL provided.
8. Open your command line or Terminal application and enter the directory where you would like to copy the repository.
9. Clone the repository with the command below by replacing `<URL>` with clone URL you copied in the previous step. The repository will be cloned into a new directory in this location.
```
git clone <URL>
```
10. Navigate to the new directory

-->

# Notes on making a project to use the Chicago Design System
# How I constructed the bundler, or any other new project you want to start with Jekyll and the Chicago Design System:

1. Follow the instructions [here](https://jekyllrb.com/tutorials/using-jekyll-with-bundler/) for setup of a default jekyll site.


1. Make a new repo in GitHub
2. Do the basic jekyll dance https://jekyllrb.com/docs/ found at the quickstart
3. Clone the repo git clone https://github.com/Chicago/alpha.chicago.gov.git
4. update your .gitignore
5. modify config file to put in cds remote theme stuff.
6. run bundle update
7. Take these lines out of your Gemfile:


```
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
gem "jekyll", "~> 3.8.5"

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "minima", "~> 2.0"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
end
```

8. Replace this with 

```
gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
  gem "jekyll-remote-theme"
end
```

9. Include the following

```
[2019-05-15 17:18:38] ERROR `/site.webmanifest' not found.
[2019-05-15 17:18:38] ERROR `/favicon-32x32.png' not found.
[2019-05-15 17:18:38] ERROR `/favicon-16x16.png' not found.

from design-cds-jekyll

copied
  android-chrome-192x192.png
  android-chrome-256x256.png
  apple-touch-icon.png
  browserconfig.xml
  favicon-16x16.png
  favicon-32x32.png
  favicon.ico
  mstile-150x150.png
  safari-pinned-tab.svg
  site.webmanifest
```

to / directory, to serve favicons in a modern and predictable way for most requests.


10. add accessibility and colophon.md statements.

*It is at this point that I am noting the need to take these steps and prepare them as a separate guide. IE– I will need to post these steps to show how to get these things running, and then I will post another guide that will be to create a basic repo that can be used for standing up a website in no time.*

