# Dependency Management
The hardest part of learning web development/programming has been managing dependencies. This repo is in the hopes that I make sense of this mess. For more details on anything, see QIFA below.


### Ruby
**Problem: I need Ruby**

Solution: You may have Ruby already if your OS has a native package management system and comes with Ruby installed.

This means if you type:
`ruby -v`
in whatever command line you have, you will see the version your OS has. This version is usually not the latest.

Package Managers: OS X, Ubuntu, CentOS, ... but if you have Windows, you will have a bad time.

**Problem: I need Ruby 2.3.0**

Solution:
To get Ruby, you need an installer. 
**In Ruby, you can install more than one version at a time.** 

You have a few options: ruby-build, ruby-install, RubyInstaller (Windows)

If you go with ruby-install:
`brew install ruby-install`

Now use the installer to install the version you want:
`ruby-install ruby 2.3.0`

Now you need a manager. 
**A manager manages which version you are using.** 
You have a few options: chruby, rbenv, RVM, uru
If you go with RVM:
`\curl -sSL https://get.rvm.io | bash -s stable --ruby`

Now you want to tell your manager which version to use.
`rvm use ruby 2.3.0`

If you want to make this the default version everywhere:
`rvm use ruby 2.3.0 --default`

Now you have Ruby. Always beware of which version you are using.
Sanity check with `ruby -v`

### Rails

### Javascript

### AngularJS

AngularJS is a toolset for building the framework most suited to your application development.

npm install -g grunt-cli bower yo generator-karma generator-angular

yo angular didactic-funicular
used grunt not gulp
gem install compass
npm install grunt-karma --save-dev
npm install karma-phantomjs-launcher --save-dev
npm install karma-jasmine --save-dev
npm install generator-karma
npm install jasmine-core
npm install grunt
npm install phantomjs-prebuilt
until finally
`grunt`
succeeded
`grunt serve` brought up a webpage

### ReactJS

### Python

### Testing
Karma

Spectacular Test Runner for JavaScript.

### Frameworks
HTML5 Boilerplate

HTML5 Boilerplate is a professional front-end template for building fast, robust, and adaptable web apps or sites.



##QIFA
(Questions I Frequently Asked)

*Should I use grunt or gulp?*

*Should I use Bower or NPM?*

*How do I test that my web app can run on a server and not just my local setup without actually pushing it and breaking the live app?*

