
# Notes on making a project to use the Chicago Design System


1. Make a new repo in GitHub
2. Do the basic jekyll dance https://jekyllrb.com/docs/ found at the quickstart
3. Clone the repo git clone https://github.com/Chicago/alpha.chicago.gov.git
4. update your .gitignore
5. modify config file to put in cds remote theme stuff.
6. run bundle update
7. Take these lines out of your Gemfile:


```# This will help ensure the proper Jekyll version is running.
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

``` gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
  gem "jekyll-remote-theme"
end
```

9. Include the following

```
```[2019-05-15 17:18:38] ERROR `/site.webmanifest' not found.
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

  to / directory, to serve favicons in a modern and predictable way for most requests.


  10. add accessibility and colophon.md statements.

  *It is at this point that I am noting the need to take these steps and prepare them as a separate guide. IE– I will need to post these steps to show how to get these things running, and then I will post another guide that will be to create a basic repo that can be used for standing up a website in no time.

  
