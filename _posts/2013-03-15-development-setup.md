---
layout: post
title: Development setup
tags: [productivity]
published: false
---

I work exclusively in OSX now. I use slate to do windows management. At work I
plug in Macbook to a Bookarc dock and connect it to my 30in display. So I have
two monitors defined in slate with two resolutions, and slate is able to detect
resolution changes and resize my windows.

My default layout configured using slate is to put my iTerm window to the right
half of my screen, and my Chrome window to teh left half. Adium contact list is
pushed to the right, and the conversation window is pushed to the bottom left
corner.

I map Hyper-Enter (double pinky) to have slate activate my default layout. It
also focuses Chrome and iTerm so they appear in front.

In Chrome, I have two profiles, one for work and one for personal stuff. I can
easily switch between them using the default shortcut of Cmd-`

In iTerm, I have two tabs running, the first one is called desktop, and the
second one laptop. In the first tab, I always run the command 'work', which ssh
into my work desktop and attaches to the tmux session there named 'work'. This
is where I do my development. One the tab 'laptop', I also a tmux session
locally to work on personal projects and take notes. I used to use Google Docs,
and nvALT for a while before I decided that I should just use Vim for all my
text editing need. I have two windows in this tmux session, the first is
running vim for my personal notes, and second running Vim for my work notes. I
have two corresponding sessoins in Vim set up using Unite-Sessions that I can
easily switch to my note environment. My personal note is saved in Dropbox, and
my work notes are saved in Google Drive associated with my work account. 

I have a keyboard shortcut set up using BetterTouchTools that whenever I press
Hyper-N, it focuses my iTerm window, sends Cmd-2, then Alt-1. This effectively
places the focus on my personal notes tab running in tmux. I have a similar
mapping Hyper-M for work notes. This makes taking quick notes extremely simple.

I work more with markdown files now, so I have vim set up with
vim-instant-markdown, which gives me a preview window in Chrome of the markdown
file I'm editing. nvALT had this feature, but never worked very well. For
example, if I'm working on a long document that requires scrolling, the popup
window that displays the rendered html always goes back to the top whenever a
edit happens. The current setup with Vim works perfectly.

A little more about the hyper key, I bind it to ctrl-shift-option-cmd on the Mac
using the trick Steve Losh mentioned in his blog post. Note that the timeout
settings in KeyRemap4MacBook is very important. For Key Overlaid Modifier
Initial Modifier Wait, I have a setting of 100ms, this is to prevent my rapid
press of Capslock + ; (which in Vim will exit insert mode and open command line
prompt) to be registered as Hyper + ; which will accidentally switch my tmux
window around. I also have a setting. The setting tells the keyboard that only
aftering holding the key for more than 100ms, should the overload functionality
be considered (in this case it's the hyper key mapping)

Other productivity tips:

A combination of Caffenine and NoSleep on the Mac means I can keep my Mac
running all the time, no matter if the screen is on or off. If I ever need to
sleep my Mac, I have two shortcuts defined in BetterTouchTools. Ctrl-Option-Cmd
will sleep my display, and Hyper+Delete will sleep my computer

I use teamocil to manage my initial tmux sessions. For my laptop, I have a
session cleverly named 'laptop' that starts my personal and work notes in vim.
So I run tmux followed by 't laptop' to get everything started

