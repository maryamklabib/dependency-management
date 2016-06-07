# FAQ

#### Why does my chef run bomb out? Why can't I get my recipe to converge?

Make sure you're using system ruby, not rvm or rbenv ruby.  If you're not sure, run the following command and check that the output is `/usr/bin/ruby`:

```
$ which ruby
/usr/bin/ruby
```

Longer answer:  We test against system ruby, which is a good common denominator.  Also, using system ruby will bypass ownership issues (i.e. gems owned by root but installed under one's home directory).

#### Why do my edits keep getting reverted?  I change the recipe, but every time I run soloist it's changed back.

You're editing the recipe under `sprout-wrap/cookbooks`.  That is a directory that is checked-out from the sources (as defined in `Cheffile`) every chef run&mdash;overwriting your changes.

Make your changes under `sprout-wrap/site-cookbooks` instead; those changes won't be overwritten.

#### Why does sprout-wrap install an older version of RubyMine even though sprout's RubyMine recipe specifies a newer one?

You need to update the git SHAs specified in sprout-wrap's `Cheffile.lock`.  Run the following command in the root of your copy of the sprout-wrap repo:

```
librarian-chef update
```

#### Why not use the standalone Command Line Tools for XCode instead of XCode?

There are primarily 2 reasons that we install XCode in sprout-wrap:
    
1. System Ruby on OS X Mountain Lion uses `xcrun` to detect `cc`. `xcrun` is [not designed](http://stackoverflow.com/questions/13041525/osx-10-8-xcrun-no-such-file-or-directory) to work with the standalone Command Line Tools.
2. sprout-wrap is used to build workstations for iOS development. Having XCode available is handy in this situation.

------------------------

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

Many developers automate including files in gemspec with Hoe,Jeweler, Rake, Bundler, or just a dynamic gemspec 