

# Ruby On Rails# What is Ruby On rails?
Rails is a development tool which gives web developers a framework, providing structure for all the code they write. The Rails framework helps developers to build websites and applications, because it abstracts and simplifies common repetitive tasks.
# Installation of Railshere there is the steps given below for installing Ruby on Rails.

- Step 1: Check Ruby VersionFirst, check if you already have Ruby installed. Open the command prompt and type ruby -v. If Ruby responds, and if it shows a version number at or above 2.2.2, then type gem --version. If you don't get an error, skip Install Ruby step. Otherwise, we'll install a fresh Ruby.

- Step 2: Install RubyIf Ruby is not installed, then download an installation package from rubyinstaller.org. Follow the download link, and run the resulting installer. This is an exe file rubyinstaller-2.2.2.x.exe and will be installed in a single click. It's a very small package, and you'll get RubyGems as well along with this package. 

- Step 3: Install RailsInstall Rails − With Rubygems loaded, you can install all of Rails and its dependencies using the following command through the command line −
C:\> gem install rails
- Note − The above command may take some time to install all dependencies. Make sure you are connected to the internet while installing gems dependencies make sure if you have Good network.

- Step 4: Check Rails VersionUse the following command to check the rails version.
C:\> rails -v- OutputRails 4.2.4

# Rails Installation on Linux
We are installing Ruby On Rails on Linux using rbenv. It is a lightweight Ruby Version Management Tool. The rbenv provides an easy installation procedure to manage various versions of Ruby, and a solid environment for developing Ruby on Rails applications.

# Follow the steps given below to install Ruby on Rails using rbenv tool.

- Step 1: Install Prerequisite DependenciesFirst of all, we have to install git - core and some ruby dependences that help to install Ruby on Rails. Use the following command for installing Rails dependencies using yum.
tp> sudo yum install -y git-core zlib zlib-devel gcc-c++ patch readline readline-devel libyaml-devel libffi-devel openssl-devel make bzip2 autoconf automake libtool bison curl sqlite-devel

- Step 2: Install rbenvNow we will install rbenv and set the appropriate environment variables. Use the following set of commands to get rbenv for git repository.
tp> git clone git://github.com/sstephenson/rbenv.git .rbenvtp> echo 'export PATH = "$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profiletp> echo 'eval "$(rbenv init -)"' >> ~/.bash_profiletp> exec $SHELL
tp> git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-buildtp> echo 'export PATH = "$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' << ~/.bash_profiletp> exec $SHELL

- Step 3: Install RubyBefore installing Ruby, determine which version of Ruby you want to install. We will install Ruby 2.2.3. Use the following command for installing Ruby.
tp> rbenv install -v 2.2.3Use the following command for setting up the current Ruby version as default.
tp> rbenv global 2.2.3Use the following command to verify the Ruby version.
tp> ruby -vOutput

ruby 2.2.3p173 (2015-08-18 revivion 51636) [X86_64-linux]Ruby provides a keyword gem for installing the supported dependencies; we call them gems. If you don't want to install the documentation for Ruby-gems, then use the following command.
tp> echo "gem: --no-document" > ~/.gemrcThereafter, it is better to install the Bundler gem, because it helps to manage your application dependencies. Use the following command to install bundler gem.
tp> gem install bundler

- Step 4: Install RailsUse the following command for installing Rails version 4.2.4.
tp> install rails -v 4.2.4Use the following command to make Rails executable available.
tp> rbenv rehashUse the following command for checking the rails version.
tp> rails -vOutput
tp> Rails 4.2.4

- Step 5: Install JavaScript RuntimeLet us install Node.js from the Yum repository. We will take Node.js from EPEL yum repository. Use the following command to add the EPEL package to the yum repository.
tp> sudo yum -y install epel-releaseUse the following command for installing the Node.js package.
tp> sudo yum install nodejs

- Step 6: Install DatabaseBy default, Rails uses sqlite3, but you may want to install MySQL, PostgreSQL, or other RDBMS. This is optional; if you have the database installed, then you may skip this step and it is not mandatory that you have a database installed to start the rails server. For this tutorial, we are using PostgreSQL database. Therefore use the following commands to install PostgreSQL.
tp> sudo yum install postgresql-server postgresql-contribAccept the prompt, by responding with a y. Use the following command to create a PostgreSQl database cluster.
tp> sudo postgresql-setup initdbUse the following command to start and enable PostgreSQL.
tp> sudo systemctl start postgresqltp> sudo systemctl enable postgresql
# NB:
if you are using Linux you should follow all steps above without jump to any one stepsthen you will be successful in environment of ruby on rails.
# Creating Staging and other Environment in Rails

Ruby on Rails come with three environments by default – development, testing and production. But sooner or later one has a need for staging environment.
# To create a new environment you need to create:

- a new config/environments/YOUR_ENVIRONMENT.rb file
- a new database configuration entry in config/database.yml if your application uses database
- a new secret key base entry in config/secrets.yml for apps on Rails 4.1 and higher
As I mentioned first we would need a new file in config/environments/. A short example for staging environment could be config/environment stagingrb:
-----------------------------------------------------------------------------------------------
require File.expand_path('../production.rb', __FILE__)
Rails.application.configure do 
# Here override any defaults 
config.serve_static_files = true
end
-----------------------------------------------------------------------------------------------
You might actually want to copy the production.rb environment file, but I am making it short.
To make a new entry in config/database.yml just edit the file and include a new database:
------------------------------------------------------------
# Production settings for local development and profiling
staging: database: db_profile 
...
------------------------------------------------------------
To make a new entry in config/secrets.yml you can use the following Rake command to get a new key base:
--------------------------------------------------------------------------------------------------------- rake secretc975f1417b60097ecfc17e308f0d8fc502f1e2534b14ef41527d703923db9e875ad4eeb779a74c732bb6c5747c3b56d84fe7f38554089522a2f557c587766fcc
---------------------------------------------------------------------------------------------------------
...
test:
  secret_key_base: 40bf0f5019e785b6b44a29f1680febbcb06db8dd64f835986c6686bebddf304b67f8a9a6dffcc862f2586edc60921d0b736e3e0b1833eea2431767d2a0d1f9cc

# Add this new entry with the generated key base
staging:
  secret_key_base: c975f1417b60097ecfc17e308f0d8fc502f1e2534b14ef41527d703923db9e875ad4eeb779a74c732bb6c5747c3b56d84fe7f38554089522a2f557c587766fcc
...
---------------------------------------------------------------------------------------------------------Also don’t forget on various initializers that might be configured for specific environments. For instance this might be a change you want to do for a rack-mini-profiler initializer inside 
config/initializers/rack_profiler.rb file:
---------------------------------------------------------------------------------------------------------
if Rails.env.development? || Rails.env.staging?
  require 'rack-mini-profiler'

  # Initialization is skipped so trigger it
  Rack::MiniProfilerRails.initialize!(Rails.application)

  # Needed for staging env
  Rack::MiniProfiler.config.pre_authorize_cb = lambda { |env| true }
  Rack::MiniProfiler.config.authorization_mode = :allowall
end

As you can see some gems for development don’t assume you want to use them elsewhere.

---------------------------------------------------------------------------------------------------------
Now you can go ahead and prepend your commands with a new RAILS_ENV values:
- $ RAILS_ENV=staging rake db:createThe same way you can then add other environments. The nice thing is that you can use same databases if you want, just different settings (asset management, logging, 3rd party services) or the same config with a different database.
# Configuring Rails Application
- 1. Locations for Initialization 
CodeRails offers four standard spots to place initialization code:

- config/application.rb
- Environment-specific configuration files
- Initializers
- After initializers

- 2. Running Code Before Rails

In the rare event that your application needs to run some code before Rails itself is loaded, put it above the call to require 'rails/all' in config/application.rb

- 3 Configuring Rails Components

In general, the work of configuring Rails means configuring the components of Rails, as well as configuring Rails itself. The configuration file config/application.rb and environment-specific configuration files (such as config/environments/production.rb) allow you to specify the various settings that you want to pass down to all of the components.

For example, you could add this setting to config/application.rb file:
config.time_zone = 'Central Time (US & Canada)'
This is a setting for Rails itself. If you want to pass settings to individual Rails components, you can do so via the same config object in config/application.rb:

config.active_record.schema_format = :ruby
Rails will use that particular setting to configure Active Record
# Getting started with Model,View,Controller
As already mentioned, Rails relies on the MVC pattern. Model-View-Controller has some benefits over traditional concepts:
it keeps your business logic separated from your (HTML-based) viewskeeps your code clean and neat in one place.
# Model
The model represents the information and the data from the database. It is as independent from the database as possible (Rails comes with its own O/R-Mapper, allowing you to change the database that feeds the application but not the application itself). The model also does the validation of the data before it gets into the database. Most of the time you will find a table in the database and an according model in your application.
- Rails contains a model generator, which you can use via your command line, as long as you're in a Rails app already.- rails generate model User username:string password:string

# View
The view is the presentation layer for your application. The view layer is responsible for rendering your models into one or more formats, such as XHTML, XML, or even Javascript. Rails supports arbitrary text rendering and thus all text formats, but also includes explicit support for Javascript and XML. Inside the view you will find (most of the time) HTML with embedded Ruby code. In Rails, views are implemented using ERb by default.
By convention, Rails will automatically route Controller methods to specifically named Views.- For example, add the following route to your routes.rb file:# get "articles", to: "articles#index", as: :articles Next add the following Controller:
class ArticlesController < ApplicationController def index end end 
# Notice 
we aren’t calling the View in the index method.Now if you fire up your Rails application and visit /articles in the browser you should see Rails complaining that the View file does not exist.Given this scenario, Rails will expect that there should be a View file under views/articles called index.html.erb

# Controller

The controller connects the model with the view. In Rails, controllers are implemented as ActionController classes. The controller knows how to process the data that comes from the model and how to pass it onto the view. The controller should not include any database related actions (such as modifying data before it gets saved inside the database). This should be handled in the proper model.

- The process for creating a controller is very easy, and it's similar to the process we've already used for creating a model. We will create just one controller here 

# library\> rails generate controller Book

- Notice that you are capitalizing Book and using the singular form. This is a Rails paradigm that you should follow each time you create a controller.This command accomplishes several tasks, of which the following are relevant here −It creates a file called app/controllers/book_controller.rbIf you look at book_controller.rb, you will find it as follows −
class BookController < ApplicationControllerend