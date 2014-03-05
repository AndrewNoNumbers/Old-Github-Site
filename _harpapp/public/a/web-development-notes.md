Front-end stuff
==============

##Markup for content
Markdown (my favorite) - Textile - reStructuredText

- - -

##HTML and templating engines [3]
Jade (most popular, Node templating engine, people need to learn Jade because simplified syntax) - EJS (more similar to plain HTML) - Mustache
HAML (HTML Abstraction Markup Language, built for Ruby, used to describe XHTML with easier and more beautiful markup, replaces inline page templating systems such as PHP, RHTML, and ASP)


- - -

##CSS for presentation + preprocessors [1]
Sass - LESS - Stylus  

- - -

##JavaScript for behavior and logic and things that extend it
jQuery/Zepto (just libraries that everybody knows)
CoffeeScript (precompiler for JavaScript)
Grunt.js (automation for JavaScript tasks)
AngularJS (HTML enhanced for web apps, interesting!)
Node.js (server solution using JavaScript so it's easy to work with)
Express.js (web application framework like Rails to Ruby)
Backbone.js (uber-light web application framework using MV*)
Ember.js (another web application framework using MVC)
Mocha (testing)

nom (the official package manager for Node.js. npm, Inc. supports the JavaScript community by providing the registry where developers publish and share packaged open-source modules.)
http://www.infoq.com/research/top-javascript-mvc-frameworks?utm_source=infoq&utm_medium=popular_links_homepage

http://www.takipiblog.com/2013/11/20/we-analyzed-30000-github-projects-here-are-the-top-100-libraries-in-java-js-and-ruby/

As JavaScript is rapidly evolving to support more types of applications, a lot of new capabilities have not yet been absorbed into the language or standard libraries. As a result we see 50% more frameworks used in JavaScript than in Ruby and Java in the top 100, echoing that fact it’s still early days for the language.

Networking is still a big problem. A large part of JavaScript libraries (7% of the top 100) focus on networking and client/server communication. That’s 3X times more than in Java and Ruby. This is most likely due to web developers having to deal with a fragmented ecosystem on the browser side, and the relative early state of the server stack.

Striving toward structure. JavaScript also features the largest number of language extensions with 844 entries. It’s interesting to see that while JavaScript is a very flexible language, developers are looking towards ways to mold it into something more structured.

###CoffeeScript (transcompiles to JS, writes in less code than JavaScript)
RoR includes it
CoffeeScript is rumored to be made by people who dislike JavaScript syntax for people who equally dislike JavaScript syntax.

"I'd imagine that I represent a large portion of the web development community. I'm very intrigued by CoffeeScript; I've even learned the syntax and used it in a few demos. However, I haven't yet taken the plunge and used it in a real project. It comes down to this one question for me: is CoffeeScript something that is truly worth investing time and effort into learning?"

https://meta.discourse.org/t/is-it-better-for-discourse-to-use-javascript-or-coffeescript/3153/12

###Grunt.js
The Grunt automation framework plays a very big role in JS development (especially for node.js) with 23% of of top 100 libraries plugging-in to it. Grunt seems to be filling the gap in the build, testing and deployment cycle in JS. This is handled externally from the project in languages such as Java by other prominent tools such as Maven or Jenkins.

###Node.js (server-side using JavaScript)
It’s the server side programming environment de rigueur for fast, lightweight development.

Is a server-side solution for JavaScript, and in particular, for receiving and responding to HTTP requests.
Is this really JavaScript? In fact, why in the world would anyone want to run JavaScript outside of a browser, let alone the server?

Node is like most technologies that are new to the masses, but old hat to the experienced few: it’s opaque and weird to most but completely usable for a small group. The result is that if you’ve never worked with Node, you’re going to need to start with some pretty basic server-side scripts. Take your time making sure you know what’s going on, because while this is JavaScript, it’s not operating like the client-side JavaScript you’re used to. In fact, you’re going to have to twist your JavaScript brain around event loops and waiting and even a bit of network theory. 

First things first: you need to realize that Node is intended to be used for running standalone JavaScript programs. This isn’t a file referenced by a piece of HTML and running in a browser.

For all of you thinking that JavaScript is a poor language in which to be writing server-side tools, you’re half right. Yes, JavaScript is not equipped to deal with operating system-level sockets and network connectivity. But Node isn’t written in JavaScript; it’s written in C, a language perfectly capable of doing the grunt work and heavy lifting required for networking. JavaScript is perfectly capable of sending instructions to a C program that can be carried out in the dungeons of your OS. Heck, a big appeal to Node is that you can actually write a server without worrying about C. That’s the point.

Yes, this is about as mundane as you can get. Well, that is, until you realize that you’ve actually written a file server in about 20 lines of code. The output you see — the actual code of the script you wrote — isn’t canned in the script itself. It’s being served from the file system. Throw an image into the same directory, and simply add the name of the image to the end of your URL, like http://localhost:8080/my_image.png:

http://radar.oreilly.com/2011/07/what-is-node.html
http://net.tutsplus.com/tutorials/javascript-ajax/learning-serverside-javascript-with-Node-js/
Excellent rationale for using Node at your web dev shop: http://venturebeat.com/2012/01/07/building-consumer-apps-with-node/

Node.js runs JavaScript by leveraging V8, Google’s fast JavaScript engine designed for Chrome. This allows Node.js to create a runtime environment that pushes content and datfrom the server to the client quickly.

Every developer also knows at least some JavaScript. Introducing Node.js, then, is relatively easy.
Everyone in a given web shop knows the basics and just has to learn about the event loop, callbacks and to how to use async flow control.
At our own agency, as people got to know Node, we actually saw that our browser-side JavaScript code improved in quality and structure.

Code re-use at every level: browser, back end & database
JavaScript is the language of the browser, but JavaScript also powers many of the new NoSQL databases. We tried a couple of them for building content management system and quick fell in love with MongoDB.
MongoDB uses JavaScript for querying data, which means at the very worst that we can copy and paste code and use it in different layers of the system. What might be written as a parser for the browser might be used to format a report executed on the database.
Taking this one step further, we are standardising the include mechanism to actually reuse code and modules across the layers. This means all layers can include the same file, massively reducing the maintenance needed of code and cutting down the time required to write tests.

Large productivity gains in HTML & CSS using Jade & Stylus
HTML and CSS guys love working on Node because using Node means we’ll be using *Jade* and *Stylus* by TJ Holowaychuck. We loved HAML and SASS before Node.js, and now we can’t imagine using anything other than Jade and Stylus.

Wealth of hosting options: No.de, Joyent’s SmartMachine, Heroku, Nodejitsu

####Express.js (Node.js web app framework)
Web application framework to help organize your web app into MVC architecture on the server side.
A Google search gets you lots of good guides: https://www.google.com/search?q=what+is+express.js
You can use a variety of choices for your templating language (like ejs, jade, dustjs).
You can then use a database like mongodb with mongoose (for modeling) to provide a backend for your node.js app. Express basically helps you manage everything, from routes, to handling requests and views.
If you've used Sinatra in the Ruby world, a lot of this will be familiar.
Like any abstraction, Express hides difficult bits and says "don't worry, you don't need to understand this part".
The de facto standard Node.js web application framework is the Sinatra inspired Express.js

####Ember.js (JS web application framework using MVC)
http://code.tutsplus.com/tutorials/getting-into-emberjs--net-30709
http://coding.smashingmagazine.com/2013/11/07/an-in-depth-introduction-to-ember-js/
http://www.infragistics.com/community/blogs/brent_schooley/archive/2013/11/07/ember-js-basics-what-is-ember.aspx
http://www.adobe.com/devnet/html5/articles/flame-on-a-beginners-guide-to-emberjs.html

####Backbone.js (uber-light web application framework using MV*)
Great explanation of when you'll want to use a framework: http://stackoverflow.com/a/7250075/2518327+
It is designed for developing single-page web applications, and for keeping various parts of web applications (e.g. multiple clients and the server) synchronized
http://backbonejs.org/#introduction
Good tech info http://coding.smashingmagazine.com/2013/08/09/backbone-js-tips-patterns/

- - -

**Back-end**

- - -

##Language running on a web application framework

Python
on (a framework to run on the cloud)
Django - Bottle - Flask 

Ruby
on (a framework to run on the cloud)
Rails - Sinatra - Padrino
https://www.openshift.com/blogs/sinatra-padrino-or-ruby-on-rails-what-ruby-framework-to-use-on-the-cloud


What does a framework do?
"they are web frameworks, i.e. they make it easier for you to create a web application."
See some micro-frameworks: http://en.wikipedia.org/wiki/Sinatra_(software)#Frameworks_inspired_by_Sinatra

- - -

##Database and SQL query language
MySQL - MongoDB

- - -

##Host
Amazon S3, Heroku, others

- - -

*Other languages*
Erlang, Scala, Haskell, Go, Python, PHP

Erlang (not many people know it, mainly used in telecommunication, can support real-time communications between millions of users, also hot swapping code, powers WhatsApp and carriers and IM)

*WTF is*
DOM (http://www.scottandrew.com/weblog/articles/dom_2)
AJAX
JSON (JavaScript Object Notation)
RESTful (representational state transfer)
MVC (Model View Controller, concept used in application)
CRUD (Create, Read, Update and Delete are the major functions that are implemented in relational database applications, http://en.wikipedia.org/wiki/Create,_read,_update_and_delete#Database_applications fascinating on HTTP/SQL)

All of webOS (framework, and ALL the built-in apps) are 100% Javascript/HTML/CSS.

##MVC
Model is part of your code that retrieves and populates the data,
View is the HTML representation of this model(views change as models change, etc)
and Controller that in this case allows you to save the state of your javascript application via a hashbang url


##AJAX (all the cool Web 2.0 things from the mid-2000's)
The name is shorthand for Asynchronous JavaScript + XML
It represents a fundamental shift in what’s possible on the Web.
Ajax isn’t a technology. It’s really several technologies, each flourishing in its own right

"The classic web application model works like this: Most user actions in the interface trigger an HTTP request back to a web server. The server does some processing — retrieving data, crunching numbers, talking to various legacy systems — and then returns an HTML page to the client."




[1] CSS Preprocessors

Excellent overview of how preprocessor features and syntaxes work: http://code.tutsplus.com/tutorials/sass-vs-less-vs-stylus-preprocessor-shootout--net-24320

An advantage is preprocessors make our CSS DRY (Don’t Repeat Yourself) by allowing us to create variables from reusable CSS properties, which makes our code more modular and scalable, so our CSS doesn’t get out of hand and become difficult to manage.

Preprocessors save us time and do a lot of the tedious stuff for us because they have all the neat features we wish plain vanilla CSS had, like nesting selectors, math functions, referencing a parent selector, even reporting errors by telling us where and why there are errors in our code.

Preprocessors might be worth incorporating into your workflow, and if you’re serious about using one, try a few out, then choose one that suits your workflow — and mindset — best and not because it’s the most talked about.

Preprocessors produce CSS that works in all browsers. They do this by compiling the code we write into regular CSS that can be used in any browser all the way back to the stone ages.

The most important part of writing code in a CSS preprocessor is understanding the syntax. Luckily for us, the syntax is (or can be) identical to regular CSS for all three preprocessors.

Sass and LESS both use the standard CSS syntax. This makes it extremely easy to convert an existing CSS file to either preprocessor. Sass uses the .scss file extension and LESS uses the .less extension. 

Using the .styl file extension, Stylus accepts the standard CSS syntax, but it also accepts some other variations where brackets, colons, and semi-colons are all optional.

Creating a mixin to handle vendor prefixes is easy and saves a lot of repetition and painful editing. 

If you've written CSS for any decent amount of time, I am sure you have reached a point where you had an error somewhere and simply could not find it. If you're anything like me you probably spent the afternoon pulling your hair out and commenting out various things to hunt the error down.
CSS preprocessors report errors. It's just that simple. If there's something wrong with your code it tells you where, and if you're lucky: why. 

When compiling with a CSS preprocessor, any double-slash comment gets removed (e.g. //comment) and any slash-asterisk comment stays (e.g. /* comment */). That being said, use double-slash for comments you want on the non-compiled side and slash-asterisk for comments you want visible after the compilation.
Just a note: if you compile minified, all comments are removed.

####Sass
Written in Ruby

The SCSS syntax was introduced as the “new main syntax” for Sass in version 3. It uses the curly brackets and colons like regular CSS — it’s actually a superset of CSS — and contains all of its same features along with those of Sass. Because of the familiar CSS syntax, SCSS provides a lower barrier to entry.

######Compass (CSS authoring framework that extends Sass)
It’s chock full of the web’s best reusable patterns.
It makes creating sprites a breeze.

####LESS (I think I prefer this, better documentation, @ for variables, JavaScript
Written in JavaScript

The LESS documentation seems more designer friendly and the syntax looks closer to pure CSS, so it’s a smoother transition into a preprocessor. 

####Stylus
Written in JavaScript (node.js)

Supports both an indented syntax and regular CSS style
Stylus can be used with Nib, an extensions library similar to Compass that provides cross-browser CSS3 mixins.
The syntax is very minimal and flexible. For example, curly brackets, colons, semicolons, and parentheses are not required.




Ruby Frameworks

Rails
------
It is said Rails is the killer-feature of Ruby because it made creating web applications so easy. Some people see it that way, some do not.

By just placing files in certain locations and following certain patterns your app "Just Works". Rails will provide you with a very simple interface to write your application. For building simple CRUD (Create, Read, Update, Delete) applications, Rails is super-fast with all the generators. 

On the other hand, as the complexity grows, developers usually stop following the conventions, and in the end it may end up in a big mess. The result can easily become a complex framework and a complex application, patched all over the place making it difficult to navigate.

Rails is awesome when you can benefit from it's conventions to speed up the development process or you want all the other bells and whistles of a large Ruby application.

Recently, I started building a very thin JSON API service in Ruby. All it would need to do is perform a set of simple create / update / get operations on one database table; it wouldn’t even need a whole set of REST operations. The catch was that it’d need to handle as much traffic as some of our busiest Ruby applications, so one of the first decisions my team needed to make was whether to build this using Rails or Sinatra.

The trade-offs between Rails and Sinatra are generally well-known in our community: Rails offers you a lot of magic and convenience while keeping you from having to worry too much about the underpinnings of your web app, while Sinatra’s claim to fame is its speed and tiny footprint. But Ruby was built on the idea that processor time is cheap while developer time is expensive, and much of the language is optimized for the human element. 

Many developers (including myself) tend to build all of their web apps in Rails, even these super-thin service apps. The justification is that “eventually, you’re going to need *XYZ Rails Feature* anyway, so you might as well use Rails from the start.” 


Sinatra (micro-framework for Ruby for simpler than Rails)
----------
Sinatra is not Rails. It is a micro-framework used for simple websites where you may need to just define a few actions. You can make a Sinatra application as complex as you want to, but you'll hit a point where you code has become a crazy mess sooner than with Rails. While not 100% accurate, Sinatra fits mostly into the Page Controller architectural pattern, and Rails is a clear MVC implementation.

Take my answer with a bit of a grain of salt (because I haven't actually deployed a sinatra application before), but sinatra's "sweet spot" is micro-apps: tiny little applications where a full MVC framework would be overkill. With Sinatra, you can build an entire web app with a single file of code.

We used Sinatra for http://tweetarium.com much like madlep's usecase the majority of the site is just AJAX calls, so the views are very simple.

In this regard Sinatra gives you much more flexibility what your application will be using, on the other hand puts all the hassle on the developer to set a complex application.

Sinatra provides the developer with DSL (Domain Specific Language) for writing web applications. The simplest application may look like:
    require 'sinatra'
     
    get '/' do
      "Hellow world!"
    end
     
    # or in the modular way
     
    require 'sinatra/base'
     
    class App < Sinatra::Base
      get '/' do
        "Hello world!"
      end
    end
     
    run App
    
Padrino
----------
Padrino is somewhere in the middle. It is build on top of Sinatra and provides glue among other frameworks to help the developer quickly set up their project. 




[3] Templating engines
http://justjs.com/ (excellent full-tutorial on developing full-stack with JS, Node.js, MongoDB)

http://stackoverflow.com/questions/16513168/is-jade-or-ejs-better-for-node-js-templating
http://en.wikipedia.org/wiki/Comparison_of_web_template_engines


So far, we've been sending web pages to the browser with the following marvelous technique:
	var s = "<title>Oh come on</title>\n";
	s += "<h1>Oh come on!</h1>\n";
	s += "<h2>You have GOT to be kidding.</h2>\n";

Yeah, not so marvelous. It's too much work, it's tough to maintain, and it's scattered all over our "app" module. Which really ought to be our "controller" layer. Not our controller and view layers all mashed up like a Reese's Peanut Butter Cup. 

Clearly, we need page templates! Folks who have programmed in almost any web framework have used templates of one sort or another. *What they all have in common is that they put HTML first and code second, allowing you to write HTML with some code in it, as opposed to the other way around.*

Really good template systems also let you have layouts. *Sure, you can write a complete HTML page - starting with the DOCTYPE, continuing through <html> and <head>, plowing through <body> and going on to that final </html> - for every single interaction. But that's a waste of effort, and it pretty much guarantees your pages will get out of sync with each other as you improve your design for one page and fail to apply it to 600 others.*

The best template systems also permit you to have partials. *Partials are snippets of HTML usually not intended to render an entire page. Instead they are responsible for some part of the page - the tabs, the breadcrumb trail, the side navigation, or a single blog post in a pageful of post summaries.*

*Good template systems also let you pass data into a template,* but don't automatically assume every variable should be visible to the template. That's because good separation of concerns is a virtue in every part of your code, whether it's part of the model layer (the database), the view layer (the templates) or the controller layer (the routes). Many developers have come to feel that it's better to be explicit rather than doing things "by magic." Things that happen by magic are also things that lead to a lot of "WTFs per minute" and "spooky action at a distance" - situations in which you can't figure out why something is happening.


####EJS

http://embeddedjs.com/getting_started.html

http://justjs.com/posts/page-templates-with-ejs-finally-we-can-have-nice-things

EJS is right for us because it makes mixing JavaScript into HTML simple. EJS has just three really important features:

1. To print the value of a JavaScript expression as part of your HTML, while escaping any markup characters like <, >, and & to prevent XSS attacks, just use <%= ... %>, like this:

	<h3><%= post.title %></h3>

As a good rule of thumb, this is the safest way to output variables in your markup.

2. To print the value of a JavaScript expression as part of your HTML without escaping markup characters (because you are intentionally printing out HTML markup), use <%- %>, like this:

	<div class="post-body">
	
		<!--- I hope you validated this HTML against XSS attacks! -->
		
		<%- post.body %>
	
	</div>

3. To simply run some JavaScript inside your template, use <% and %>, like this. Notice that we can shift back into "HTML mode" inside the callback function of our call to "_.each()". We'll switch back to "JavaScript mode" to close the _.each call:

	<% _.each(posts, function(post) { %>
	
	  <h3><%= post.title %></h3>
	
	  <div class="post-body">
	
	    <%- post.body %>
	
	  </div>
	
	<% }) %>
	
####Jade
Jade is designed primarily for server side templating in node.js
Jade can be used just as a short hand for HTML.
Jade is whitespace sensitive, so there's no need to close your tags


http://www.franz-enzenhofer.com/jade

How to use Jade compiler

Compiling is just as easy. To do that, simply execute this line of command:
	jade index.jade
	
If you would like to compile a folder of jade files, irregardless if there is any other files within it, simply execute it with the dir instead:
	jade lib/views/

	
= = =	
	
###Server and below
The site’s hosted on a machine in his house, and is served over a DSL connection.
He says Node and/or Pulsar are doing well enough (150 connections using ~50 MB of RAM and 40% CPU)- apparently he just doesn’t have enough bandwidth to get everything out to everyone.