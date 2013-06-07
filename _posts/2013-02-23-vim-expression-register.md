---
layout: post
title: Vim expression register
tags: [vim]
---

Use vim's expression register to give more firepower to macros

Say you want to generate the numbers 1 through 100, one can do this with vim

{% highlight vim %}
:let i = 1
qq
i<C-r>=i<CR><CR>
<Esc>
:let i += 1
q
99@q
{% endhighlight %}
