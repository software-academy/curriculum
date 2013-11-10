---
layout: rails
title: Lauchpad
categories : [lessons, beginner]
tags : [learning-rails, setup]
---

Lauchpad
===

Follow the directions below for setting up a launchpad folder.  This folder will hold the gemset that we’ll use for all the sample applications we build.  You’ll learn more about this later.

When following these directions, pay close attention to where you are when executing the lines below.  That’s important.

In a terminal window, create a `/dev` folder TODO: more info on where.

`mkdir rails40`

`cd rails40`

Next, we make a .rvmrc for the launchpad

`echo "rvm use ruby-2.0.0-p247@rails4 --create" >> .rvmrc`

Next we cd out of this folder, then back into the folder.  This will execute the .rvmrc file asking if we want to trust it.  We do.

`cd ..`

`cd rails40`

When you cd back into rails40, you’ll be asked to trust it.  Answer with a y.

Next, let’s see what the rvm info says.

`rvm info`

We will install rails 4.0

`gem install rails`

We’re going to create a new rails app in this folder.  This ensures we’re using the rails 4.0 version.

`rails new foo -d postgresql`

Next cd into the foo directory and setup a new .rvmrc file:

`cd foo`

`echo "rvm use ruby-2.0.0-p247@foo --create" > .rvmrc`

An aside, ‘>’ takes the output from the command on the left and shovels it into the thing on the right (deleting any existing file).  Using ‘>>’ instead of ‘>’ would append to an existing file (or create a new file if one doesn’t already exist).  In this case, we don’t want to append, we want to create, so that’s why we used a single ‘>’ sign.

Back out of this folder and then cd back in.

`cd ..`

`cd foo`

And then let’s bundle, which installs the gems.

`bundle`

We need to then create the postgres user.

`createuser -s foo`

To see what user you should create (or to change it), view config/database.yml in the app you just created.

This assumes Postgres is running.  You can see the command for starting Postgres by running `rvm info postgres`

We then create the database.

`rake db:create`

And make sure we can run this app.

`rails s`

If this works, you’re awesome.  You can delete the foo directory now that you know the process we’ll use to create new apps.

If not, consider deleting the foo folder and starting from scratch.  If you have other troubles, either google your errors, post in our forum, or email us and we’ll help you work through any sticking points.
