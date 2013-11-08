---
layout: default
title: Machine Setup
---

Machine Setup
===

Our advice is to avoid installers. Thar be dragons.

## Machine setup on Linux
--
It is difficult to give step by step directions for setting up the environment on Linux, however, there are many articles on the web about Rails setup on Linux.  We also suggest connecting with a local [Rails Meetup](http://www.meetup.com/find/?keywords=rails).

## Machine setup on Mac OS X
If you're not totally familiar with the basics of the command line, please read [introduction to the Mac OS X command line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).

Now, let’s start setting up your development environment.

### Install Xcode from the app store.

1. [https://developer.apple.com/technologies/tools/](https://developer.apple.com/technologies/tools/)

### Install Homebrew

1. [http://brew.sh/](http://brew.sh/)
2. Ensure successful install by running <code>brew doctor</code> on the command line.


### Install Postgres
1. On the command line, run <code>brew install postgresql</code>
1. Check location of psql <code>which psql</code>.  It should be <code>/usr/local/bin/psql</code>.
666. TODO: Check path?
1. View the commands you can use with psql by running <code>brew info postgres</code>.
1. Initialize the database with <code>initdb /usr/local/var/postgres -E utf8</code>
1. You should see a command to start postgres with <code>pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start</code>. Run that to start postgres.
1. Login to psql <code>psql template1</code>.  If that works, then use <code>/q</code> to exit.

### Install RVM
RVM is a command-line tool which allows you to easily install, manage, and work with multiple ruby environments. On the command line, run <code>\curl -L https://get.rvm.io | bash -s stable --ruby</code>

### Install git
<code>brew install git</code>

### Install openssl
<code>brew install openssl</code>