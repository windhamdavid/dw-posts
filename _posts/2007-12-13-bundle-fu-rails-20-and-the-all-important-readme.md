---
ID: 693
post_title: >
  Bundle Fu, Rails 2.0, Django containers
  , the Unix-Demiurge, and the all
  important Readme..
author: David
post_date: 2007-12-13 15:01:49
post_excerpt: ""
layout: post
permalink: >
  https://macs.local/david/bundle-fu-rails-20-and-the-all-important-readme/
published: true
---
A good thing to note..<a href="http://www.mediatemple.net/labs/grid/gc-django-prebeta.htm">Media temple put Django containers into beta testing</a> and i'm guessing <a href="http://mediatemple.net/labs/cs/">they'll release with their cluster server</a> and a bad thing to note.. <a href="http://kb.mediatemple.net/article.php?id=787"> there's a trick to running rails 2.0 on the gridserver...</a> work <a href="http://kb.mediatemple.net/article.php?id=279">with this </a>and prey for no <a href="http://en.wikipedia.org/wiki/Fsck">fsck..</a>
<a href="http://en.wikipedia.org/wiki/Dennis_Ritchie">Dennis Ritchie</a> has claimed "The second letter was originally different."  <a href="http://groups.google.com/group/net.unix-wizards/msg/1c9d2e4c341f9b41">Who also gives rise to What??? - the Unix Demiurge?</a>The basic Unix idea -- a hierarchical file system with simple operations on it (create/open/read/write/delete with I/O operations based on just descriptor/buffer/count) -- wasn't <a href="http://www.itworld.com/Comp/3380/lw-12-ritchie/">new even in 1970.</a>"Things that began as neat but small tools, like Perl or Python, say, are suddenly more central in the whole scheme of things. The kind of programming that C provides will probably remain similar absolutely or slowly decline in usage, but relatively, JavaScript or its variants, or XML, will continue to become more central"...dmr.. <a href="http://www.itworld.com/Comp/3380/lw-12-ritchie/">LinuxWorld.com 12/4/00 </a>and I'll have to agree on xml.
<img src="http://davidawindham.com/org/images/ruby6.png" alt="old ruby" />
<img src="http://davidawindham.com/org/images/ruby3.png" alt="ruby error" />
<img src="http://davidawindham.com/org/images/ruby5.png" alt="ruby version" />
<img src="http://davidawindham.com/org/images/ruby4.png" alt="ruby update" />
<a href="http://wiki.rubyonrails.com/rails/pages/Calendar+Helper+Plugin">So i've built two apps to use google apps since</a> i already set up Gapps most the time..<a href="http://spinstudentlife.com/event">(to emulate this one of the awesome-est calendars)</a>..... <a href="http://weblog.commandlinejunkie.com">(as i like to keep up with my brother who seems to think he's the smart one)</a> and i updated my rails today.. <a href="http://www.demiurgicdesign.com/ruby.html">(i like to take screen captures when i do it.. my connection seems to be jammed with holiday shoppers)</a>..and i realized something that i do often.. i don't follow directions.. never have..including updating my ruby to .6 but I like to take it all apart and figure it out myself.. when i first saw rails, it was shoved into my face and took the app apart figured out how it worked and moved on.. we'll same goes for as and js.. i cut it up and figure out how the parts go together.. we'll.. having been using eclipse for flex i just went with <a href="http://locomotive.raaum.org/">locomotive</a> first and then <a href="http://www.aptana.com/rails/">rad rails</a>.. bad move if you ever plan on deploying because you'll have a time with server configuration, so go with a custom install on your machine..and understand the fundamentals before you go playing around with applications or code and take this advice .....always read the readme.
<a href="http://hivelogic.com/narrative/articles/ruby-rails-mongrel-mysql-osx">this tutorial will get you going easier than any other..</a>
OH.. and  <a href="http://code.google.com/p/bundle-fu/">Bundle Fu </a>

and where to start right..

== Welcome to Rails
Rails is a web-application and persistence framework that includes everything
needed to create database-backed web-applications according to the
Model-View-Control pattern of separation. This pattern splits the view (also
called the presentation) into "dumb" templates that are primarily responsible
for inserting pre-built data in between HTML tags. The model contains the
"smart" domain objects (such as Account, Product, Person, Post) that holds all
the business logic and knows how to persist themselves to a database. The
controller handles the incoming requests (such as Save New Account, Update
Product, Show Post) by manipulating the model and directing data to the view.
In Rails, the model is handled by what's called an object-relational mapping
layer entitled Active Record. This layer allows you to present the data from
database rows as objects and embellish these data objects with business logic
methods. You can read more about Active Record in
link:files/vendor/rails/activerecord/README.html.
The controller and view are handled by the Action Pack, which handles both
layers by its two parts: Action View and Action Controller. These two layers
are bundled in a single package due to their heavy interdependence. This is
unlike the relationship between the Active Record and Action Pack that is much
more separate. Each of these packages can be used independently outside of
Rails.  You can read more about Action Pack in
link:files/vendor/rails/actionpack/README.html.

== Getting Started
1. At the command prompt, start a new Rails application using the <tt>rails</tt> command
   and your application name. Ex: rails myapp
   (If you've downloaded Rails in a complete tgz or zip, this step is already done)
2. Change directory into myapp and start the web server: <tt>script/server</tt> (run with --help for options)
3. Go to http://localhost:3000/ and get "Welcome aboard: You’re riding the Rails!"
4. Follow the guidelines to start developing your application

== Web Servers
By default, Rails will try to use Mongrel and lighttpd if they are installed, otherwise
Rails will use WEBrick, the webserver that ships with Ruby. When you run script/server,
Rails will check if Mongrel exists, then lighttpd and finally fall back to WEBrick. This ensures
that you can always get up and running quickly.
Mongrel is a Ruby-based webserver with a C component (which requires compilation) that is
suitable for development and deployment of Rails applications. If you have Ruby Gems installed,
getting up and running with mongrel is as easy as: <tt>gem install mongrel</tt>.
More info at: http://mongrel.rubyforge.org
If Mongrel is not installed, Rails will look for lighttpd. It's considerably faster than
Mongrel and WEBrick and also suited for production use, but requires additional
installation and currently only works well on OS X/Unix (Windows users are encouraged
to start with Mongrel). We recommend version 1.4.11 and higher. You can download it from
http://www.lighttpd.net.
And finally, if neither Mongrel or lighttpd are installed, Rails will use the built-in Ruby
web server, WEBrick. WEBrick is a small Ruby web server suitable for development, but not
for production.
But of course its also possible to run Rails on any platform that supports FCGI.
Apache, LiteSpeed, IIS are just a few. For more information on FCGI,
please visit: http://wiki.rubyonrails.com/rails/pages/FastCGI

== Debugging Rails
Sometimes your application goes wrong.  Fortunately there are a lot of tools that
will help you debug it and get it back on the rails.
First area to check is the application log files.  Have "tail -f" commands running
on the server.log and development.log. Rails will automatically display debugging
and runtime information to these files. Debugging info will also be shown in the
browser on requests from 127.0.0.1.
You can also log your own messages directly into the log file from your code using
the Ruby logger class from inside your controllers. Example:
  class WeblogController < ActionController::Base
    def destroy
      @weblog = Weblog.find(params[:id])
      @weblog.destroy
      logger.info("#{Time.now} Destroyed Weblog ID ##{@weblog.id}!")
    end
  end
The result will be a message in your log file along the lines of:
  Mon Oct 08 14:22:29 +1000 2007 Destroyed Weblog ID #1
More information on how to use the logger is at http://www.ruby-doc.org/core/
Also, Ruby documentation can be found at http://www.ruby-lang.org/ including:
* The Learning Ruby (Pickaxe) Book: http://www.ruby-doc.org/docs/ProgrammingRuby/
* Learn to Program: http://pine.fm/LearnToProgram/  (a beginners guide)
These two online (and free) books will bring you up to speed on the Ruby language
and also on programming in general.

== Debugger
Debugger support is available through the debugger command when you start your Mongrel or
Webrick server with --debugger. This means that you can break out of execution at any point
in the code, investigate and change the model, AND then resume execution! Example:
  class WeblogController < ActionController::Base
    def index
      @posts = Post.find(:all)
      debugger
    end
  end
So the controller will accept the action, run the first line, then present you
with a IRB prompt in the server window. Here you can do things like:
  >> @posts.inspect
  => "[#<post:0x14a6be8 @attributes={"title"=>nil, "body"=>nil, "id"=>"1"}>,
       #<post:0x14a6620 @attributes={"title"=>"Rails you know!", "body"=>"Only ten..", "id"=>"2"}>]"
  >> @posts.first.title = "hello from a debugger"
  => "hello from a debugger"
just thought i throw this in.. :)
<img src="http://davidawindham.com/org/images/Atari800.jpg" alt="Atari 800" />
...and even better is that you can examine how your runtime objects actually work:
  >> f = @posts.first
  => #<post:0x13630c4 @attributes={"title"=>nil, "body"=>nil, "id"=>"1"}>
  >> f.
  Display all 152 possibilities? (y or n)
Finally, when you're ready to resume execution, you enter "cont"
== Console
You can interact with the domain model by starting the console through <tt>script/console</tt>.
Here you'll have all parts of the application configured, just like it is when the
application is running. You can inspect domain models, change values, and save to the
database. Starting the script without arguments will launch it in the development environment.
Passing an argument will specify a different environment, like <tt>script/console production</tt>.
To reload your controllers and models after launching the console run <tt>reload!</tt>


== Description of Contents
app
  Holds all the code that's specific to this particular application.
app/controllers
  Holds controllers that should be named like weblogs_controller.rb for
  automated URL mapping. All controllers should descend from ApplicationController
  which itself descends from ActionController::Base.
app/models
  Holds models that should be named like post.rb.
  Most models will descend from ActiveRecord::Base.
app/views
  Holds the template files for the view that should be named like
  weblogs/index.erb for the WeblogsController#index action. All views use eRuby
  syntax.
app/views/layouts
  Holds the template files for layouts to be used with views. This models the common
  header/footer method of wrapping views. In your views, define a layout using the
  <tt>layout :default</tt> and create a file named default.erb. Inside default.erb,
  call <% yield %> to render the view using this layout.
app/helpers
  Holds view helpers that should be named like weblogs_helper.rb. These are generated
  for you automatically when using script/generate for controllers. Helpers can be used to
  wrap functionality for your views into methods.
config
  Configuration files for the Rails environment, the routing map, the database, and other dependencies.
db
  Contains the database schema in schema.rb.  db/migrate contains all
  the sequence of Migrations for your schema.
doc
  This directory is where your application documentation will be stored when generated
  using <tt>rake doc:app</tt>
lib
  Application specific libraries. Basically, any kind of custom code that doesn't
  belong under controllers, models, or helpers. This directory is in the load path.
public
  The directory available for the web server. Contains subdirectories for images, stylesheets,
  and javascripts. Also contains the dispatchers and the default HTML files. This should be
  set as the DOCUMENT_ROOT of your web server.
script
  Helper scripts for automation and generation.
test
  Unit and functional tests along with fixtures. When using the script/generate scripts, template
  test files will be generated for you and placed in this directory.
vendor
  External libraries that the application depends on. Also includes the plugins subdirectory.
  This directory is in the load path.
