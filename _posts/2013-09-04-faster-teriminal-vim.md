---
layout: post
title: "Faster teriminal vim"
date: "Wed Sep 04 16:50:51 -0700 2013"
---

Few quick tips on getting Vim to be lighting fast again in iTerm2. MacVim doesn't suffer from the below problems.

I was using vim-powerline, have cursorline turned on and scrolljump defaulted to 1. Moving my cursor left and right were painfully slow. I'm a much happier man once again.

{% highlight bash %}
NeoBundle 'bling/vim-airline'
set nocursorline
set nocursorcolumn
set scrolljump=5
{% endhighlight %}

