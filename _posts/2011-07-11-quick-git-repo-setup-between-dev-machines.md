---
layout: post
title: Quick git repo setup between dev machines
---

I needed to create a quick private git repo to share some projects among a few folks. I wanted people to be able to push and pull from it without having to enter their ssh password or have ssh keys set up, I also didn&#39;t want to go through the trouble of setting up a web server (A quick node.js app didn&#39;t appear to work). [git-daemon](http://www.kernel.org/pub/software/scm/git/docs/git-daemon.html) came to the rescue nicely. For my case, I had the project in a local git repo on a Windows machine, I wanted to create a private repo on my Linux box. Here&#39;re the steps I took:

On Linux machine (foobar.com):

{% highlight bash %}
mkdir /workplace/gitrepos
cd /workplace/gitrepos
mkdir HelloWorld.git
cd HelloWorld.git
git init --bare
cd ..
git daemon --reuseaddr --base-path=. --export-all --enable=receive-pack
{% endhighlight %}

On Windows machine, in the project git root, assuming that the project has already been committed to branch master:

{% highlight bash %}
git remote add origin git://foobar.com/HelloWorld.git
git push origin master
{% endhighlight %}
