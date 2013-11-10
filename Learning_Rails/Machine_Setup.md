---
layout: rails
title: Machine Setup
---

Machine Setup
===

Our advice is to avoid installers. Thar be dragons.

## Machine setup on Linux
It is difficult to give step by step directions for setting up the environment on Linux, however, there are many articles on the web about Rails setup on Linux.  We also suggest connecting with a local [Rails Meetup](http://www.meetup.com/find/?keywords=rails).

## Machine setup on Mac OS X
If you're not totally familiar with the basics of the command line, please read [introduction to the Mac OS X command line](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).

Now, let’s start setting up your development environment.

### Install Xcode from the app store.

1. [https://developer.apple.com/technologies/tools/](https://developer.apple.com/technologies/tools/)

### Install Homebrew

1. [http://brew.sh/](http://brew.sh/)
2. Ensure successful install by running `brew doctor` on the command line.


### Install Postgres
1. On the command line, run `brew install postgresql`
1. Check location of psql `which psql`.  It should be `/usr/local/bin/psql`.
666. TODO: Check path?
1. View the commands you can use with psql by running `brew info postgres`.
1. Initialize the database with `initdb /usr/local/var/postgres -E utf8`
1. You should see a command to start postgres with `pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start`. Run that to start postgres.
1. Login to psql `psql template1`.  If that works, then use `/q` to exit.
1. Run `ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents` so that postgres will start automatically.

### Install RVM
RVM is a command-line tool which allows you to easily install, manage, and work with multiple ruby environments. On the command line, run `\curl -L https://get.rvm.io | bash -s stable --ruby`

### Install git
`brew install git`

### Install openssl
`brew install openssl`