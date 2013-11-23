---
layout: rails
title: Ruby and Rails Basics
---

Ruby and Rails Basics
===

###Naming Conventions

Rails makes assumptions about what you want to do and how you're going to do it, rather than requiring you to specify every little thing through endless configuration files. If you haven't built many web applications, this might not mean much to you, but for others, the beauty (and magic) will be obvious.

Some specific naming conventions:

1. **Singular Model names, Plural Controller names** Class names are singular, controllers plural, database tables are plural. A **User** class utilizes a **Users** table in the database, is called with the **Users Controller** and has views in the **/app/views/users** folder. Rails can figure out the relationships for even the hard ones, so if you have a person class, Rails knows this is the People table and the People Controller with views in the /app/views/people folder.  Crazy cool eh?

1. Class names are MixedCase - no underscores.  File names are lower case with underscore.  SO, in the above scenario, we'd have a people_controller.rb file as the PeopleController class.

1. **Primary keys** in database tables are just id. This might not seem like a big deal, but in the past some people would have a column person_id or personID in the People table.  When integrating with non rails systems with different names for the primary key, this becomes noticeably difficult.

1. **Foreign keys** are simply the singular version of the target table, with _id added.  So, if another table (eg: Orders) was holding records related to a person, there would be a person_id column in the Orders table.  And if that was done, rails would 'just work', which is always a great thing.

###DRY - Don't repeat yourself

You'll hear this often.  Basically what it means is that if you have a piece of code that exists in several parts of a program, consider extracting it to a central place, and then using it from there.

###MVC Framework
Rails is an MVC framework, which is a modern way web applications are built.

![mvc](http://gmoeck.github.io/images/rails_mvc.png)

1. The browser sends a request to the web server.
1. The web server processes the request, determines which route it belongs to and dispatches that request to the corresponding controller method.
1. The controller then asks the model layer for all the necessary information in order to be able to complete the request.
1. The model layer collects all the information and returns it to the controller
1. The controller gives the appropriate information to the view, and asks it to render
1. The view renders itself and gives the rendered html to the controller
1. The controller assembles the total page's html and gives it to the web server
1. The web server returns the page to the browser

###Gems

Gems are programs written by other developers and teams, which package up a specific functionality to be used by other people and systems.  They are normally open source and they make the world a better place and your life easier. Examples would be gems for interacting with [Twitter Oauth](https://github.com/intridea/omniauth, a gem such as [paperclip](https://github.com/thoughtbot/paperclip) for uploading files, or a gem like [Devise](https://github.com/plataformatec/devise) for user registration.

Much of modern programming is knowing what other software is availalbe (such as gems or APIs), knowing how to choose these well, and knowing how to integrate. People don't write everything from scratch.  Think of web application development work as putting together a bunch of building blocks.

###Object Oriented

Modern programming is based on a concept of Objects and Inheritance.  Here's a quick example.

In Rails, there is a class called [ActiveRecord](http://api.rubyonrails.org/classes/ActiveRecord/Base.html) which *inherits* from Object.  **ActiveRecord** is important because it's what we use to interact (easily) with the database.  The ActiveRecord class contains a lot of code to perform these database related functions.  So when we create a new class, like the **Person** class above, we don't have to put all the code in this new class to access the database. What we do is have Person inherit from ActiveRecord, like this:

`class Person < ActiveRecord::Base`

The < is saying Person **is a** ActiveRecord object.  So, anything ActiveRecord can do, so can Person.  AND, we don't have to write a single line of code!! Eventually you'll learn more about OO and inheritance.  For now, just keep in mind DRY and that much of the code that allows our classes to do what they do is **not* stored in that class, but inherited from other classes.  That's part of the magic.


