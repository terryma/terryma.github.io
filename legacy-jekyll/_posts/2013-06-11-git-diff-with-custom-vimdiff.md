---
layout: post
title: "Git diff with custom vimdiff"
date: "Tue Jun 11 18:50:51 -0700 2013"
---

Traditionally vimdiff puts the newer revision on the right side. I'm quirky and like it the other way around. With git, you can achieve that by adding the following in your .gitconfig:

{% highlight kernel-config %}
[diff]
  tool = myvimdiff
[difftool "myvimdiff"]
  cmd = vimdiff \"$REMOTE\" \"$LOCAL\"
{% endhighlight %}

I also have `gd` aliased to `git difftool` to invoke the above config.


