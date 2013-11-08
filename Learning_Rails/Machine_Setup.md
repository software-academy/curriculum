---
layout: default
title: Machine Setup
---

Machine Setup
===

Our advice is to avoid installers. Thar be dragons.

Machine setup on Linux
--
It is difficult to give step by step directions for setting up the environment on Linux, however, there are many articles on the web about Rails setup on Linux.  We also suggest connecting with a local [Rails Meetup](http://www.meetup.com/find/?keywords=rails).

Machine setup on Mac OS X
--
If you're not totally familiar with the basics of the command line, please read [introduction to the Mac OS X command line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).

Now, let’s start setting up your development environment.

1. Install Xcode from the app store.
[https://developer.apple.com/technologies/tools/](https://developer.apple.com/technologies/tools/)

2. Install Homebrew [http://brew.sh/](http://brew.sh/)


3. Install Postgres
$ brew install postgresql

run the init.db command
$ initdb /usr/local/var/postgres -E utf8

Install RVM
$ \curl -L https://get.rvm.io | bash -s stable --ruby

Install git
$ brew install git

Install openssl
$ brew install openssl