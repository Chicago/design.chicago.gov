

## How To Contribute to the Chicago Design System.

This quick start guide will walk you through cloning the GitHub repository, as well as installing both Jekyll and Pattern Lab so you can start contributing to the Chicago Design System.


## GitHub

GitHub is used for version control of the Chicago Design System. To contribute to the project, you will fork a version of the main repository to edit.

1. Navigate to the Chicago Design System repository [link](https://github.com/Chicago/design-system).
2. In the top-right corner of the page, click **Fork**.
3. You now have a forked copy of the original /Chicago/design-system repository.
4. Go to the **code** section of your fork.
5. Clock **Clone or download**
6. Copy the URL provided.
7. Open your command line or Terminal application and enter the directory where you would like to copy the repository.
8. Clone the repository with the command below by replacing <URL> with clone URL you copied in the previous step. The repository will be cloned into a new directory in this location.
```
git clone `<URL>`
```
9. Navigate into the directory of the repository you just created with the command below.
```
cd design-system
```

## Jekyll

Jekyll is used to publish the Chicago Design System. You will need to install Jekyll in order to preview your changes to the CDS repository.

#### Mac Install

[Go here](https://jekyllrb.com/docs/quickstart/) for instructions on how to install Jekyll.

Once Jekyll is installed, navigate to the docs folder in the design-system respository and run:

```
bundle exec jekyll serve --baseurl ''
```

You can then pull up http://localhost:4000/ in your browser to see the design standards local clone.

## Pattern Lab

Pattern Lab is used to publish the atomic design elements of the Chiago Design System. You will need to install the CDS Pattern Lab fork in order to edit and preview your changes to the CDS.

#### Mac Install as submodule

1. Install Node.js via a package manager ([link](https://nodejs.org/en/download/package-manager/#macos))
2. Install the Pattern Lab submodule with the commands 
```
git submodule init
git submodule update
```

#### Mac Install independently

1. Install Node.js via a package manager ([link](https://nodejs.org/en/download/package-manager/#macos))
2. Navigate to the Chicago Design System Pattern Lab repository [link](https://github.com/Chicago/patternlab-node).
3. In the top-right corner of the page, click **Fork**.
4. You now have a forked copy of the original /Chicago/design-system repository.
5. Go to the **code** section of your fork.
6. Clock **Clone or download**
7. Copy the URL provided.
8. Open your command line or Terminal application and enter the directory where you would like to copy the repository.
9. Clone the repository with the command below by replacing <URL> with clone URL you copied in the previous step. The repository will be cloned into a new directory in this location.
```
git clone `<URL>`
```
10. Navigate to the new directory
11. Install dependencies using the command:
```
npm install
```

<!---
## To delete:
1. treehouse install stuff for each
2. npm install stuff
3. gulp install stuff https://github.com/gulpjs/gulp/blob/4.0/docs/getting-started.md
4. Hey, you don't need to install Gulp.... so...
5. "npm install @pattern-lab/core" from https://github.com/pattern-lab/patternlab-node/tree/master/packages/core


Install Node.
Install Gulp.

You could probably avoid installing Gulp, to be honest.

Then I tried to npm install @pattern-lab/core. That worked so long as I was in the root of my user directory. Elsewhere, like in a folder to start a github repo, not so much.

So, instead I forked https://github.com/pattern-lab/patternlab-node

npm i @pattern-lab/core
npm i @pattern-lab/uikit-workshop
npm i @pattern-lab/engine-mustache


I removed Gulp.

## Attempt 37

0. Install homebrew.
1. Install node: brew install etc.

-->