## Research App, Landing Page

We're using this to test out the product message to see if there is a fit.

* * *  


### Dependencies

This site is build with, and requires the following:

* Ruby ~> 2.1.2
* Jekyll (static-site generator) ~> 2.5.3
* Foreman ~> 0.78.0
* Node.js/NPM - ^0.12.2
* BrowserSync - ^1.3.7

It is deployed to:

* GitHub Page (using the 'gh-pages' branch)

  
* * *   


### System Setup

#### 1. Ruby
You will need to use Ruby 2.1.x.

If you don't care about managing your own Ruby versions on your system (you should), then you can just use the system version of Ruby and skip to the next step.

If you'd rather not have OS updates mess with your Ruby environment, you should manage your Ruby versions with [rbenv](https://github.com/sstephenson/rbenv) and [ruby-build](https://github.com/sstephenson/ruby-build). 

You can install each with Homebrew. Use their respective documentation for more info.

Once rbenv is set up (or if you already use it or prefer RVM instead) you just need to install the correct version of Ruby. 

As mentioned, that version is 2.1.x, so follow the documentation for your respective tool (ideally rbenv) to install it and set it as your global Ruby version. (Run ``ruby -v`` to confirm.)

#### 2. Bundler
Install [Bundler](http://bundler.io/) for the 2.1.x version of Ruby you just installed and set as your global version.
``gem install bundler``

#### 3. Node
You will need to use Node to run BrowserSync.

Install Node.js and NPM using Homebrew.


* * *   


### Building the Site
After checking out this repo (duh)...

#### 1. Install Dependencies
Use Bundler to install Jekyll and Foreman (and their dependencies):
``bundle install``

Use NPM to install BrowserSync:
``npm install -g browser-sync`` 

Or if you'd rather install BrowserSync locally (as defined in package.json):
``npm install``

#### 2. Build and Run Locally
Foreman will run the Jekyll 'build' and BrowserSync 'start' commands (as defined in the Procfile).
``foreman start``

This will give you a local server that will check for any changes to HTML and CSS files (and Jekyll will compile your Sass files to CSS). 
``http://localhost:4000``


* * *  


### Deploying the Site

Push changes to the ``gh-pages`` branch.


