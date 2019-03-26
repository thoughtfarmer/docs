# ThoughtFarmer developer tools

Grunt command line tools for developing and deploying ThoughtFarmer Custom cards.

### Installation

* Install Node.js and NPM [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
* Install grunt-cli [https://github.com/gruntjs/grunt-cli](https://github.com/gruntjs/grunt-cli)
* Install ruby [https://www.ruby-lang.org/en/documentation/installation/](https://www.ruby-lang.org/en/documentation/installation/) 
* Extract the [tfDevTools.zip](https://community.thoughtfarmer.com/attachment/159160200000/110457/tfDevTools.zip)
* Go to the folder and run "npm install"

### Getting started

First set up a default site. All commands will use this site unless otherwise specified by **--site=siteName** or just the flag **-siteName**

```text
grunt sites:add
```

Be sure to name the first endpoint "default".

### Commands

* [Manage sites](manage-sites.md)
* [Manage cards](manage-cards.md)
* [Develop cards](develop-cards.md)

### Example project

In the tfDevTools.zip there is a project called _**tfDevToolsSample**_. Follow the _README.md_ in that folder to get up and running with the latest tools available with this package.  


