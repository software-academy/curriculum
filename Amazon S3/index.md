---
layout: default
title: Amazon AWS/S3
---

Amazon AWS/S3
===

One service provided by Amazon Web Services (AWS) is [Amazon S3](http://aws.amazon.com/s3/).  S3 allows developers to store and retrieve data (such as images) in the cloud.


Why important
---

Because [Heroku](/Heroku) does not allow the storage of files on a server, Ruby on Rails applications hosted on Heroku typically store files (user profile images, uploaded files, documents) on Amazon S3.


How we teach it
---

We have a specific module for helping you connect a rails application to S3 storage.  This is often done using the Paperclip gem, which is what we use to teach this process.

Learn more
---

Heroku has an excellent article on [uploading files to s3 using Paperclip](https://devcenter.heroku.com/articles/paperclip-s3), written by Harlow Ward, from [thoughtbot](http://thoughtbot.com) the developers of the paperclip gem.
