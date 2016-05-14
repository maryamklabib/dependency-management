# Dependency Management


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

build: grunt vs gulp 
package manager: bower and npm

### ReactJS

### Python
