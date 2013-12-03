---
layout: default
title: Add posts#new view
---

<h1 id="main">Add posts#new view</h1>

#####Update file `app/controllers/posts_controller.rb`

Add
<pre><code>   def new
   end</code></pre>


Becomes
<pre><code> class PostsController &lt; ApplicationController
   def new
   end
 end
</code></pre>
<div class='section-break'></div>

Create file `app/views/posts/new.html.erb`

Add
<pre><code> &lt;h1&gt;New Post&lt;/h1&gt;</code></pre>


### Additional Resources

* [Changes in this step in `diff` format](https://github.com/stevenhallen/rails_getting_started_bdd/commit/70fbfd95b3bc29eac99dee41526eb1f28a8a9f1e)

