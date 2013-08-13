---
layout: post
title: "Install Ruby 2.0 with proper openssl and readline"
date: "Tue Aug 13 01:07:09 -0700 2013"
---

{% highlight bash %}
CONFIGURE_OPTS="--with-openssl-dir=`brew --prefix openssl` --with-readline-dir=`brew --prefix readline`" rbenv install 2.0.0-p0
{% endhighlight %}

The readline support is needed of you want to customize keyboard shortcuts for `irb` or `pry` with `.inputrc`
