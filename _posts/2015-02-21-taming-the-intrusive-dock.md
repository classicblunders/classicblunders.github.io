---
layout: post
type:
title: Taming The Intrusive Mac Dock
description:
headline:
category: productivity
tags:
  - mac osx
imagefeature: gratisography-ryan-mcguire-arm-wrestling.jpg
comments: true
mathjax:
---

The Mac Dock is the gossipy busybody of the OSX neighborhood. Anyone who has ever had their mouse cursor stray too close to the bottom of the screen, knows the Dock well. Some say to accept the Dock for what it is, while others advise to just keep your cursor from trespassing onto its land. I have another suggestion: slap it with a restraining order and take control of the Dock.

If you are completely unfamiliar with the Mac terminal, I suggest you first learn the basics. [Treehouse has a good tutorial for beginners](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line).

You can delay how long it takes for the Dock to appear by issuing the following terminal command (don't type the `$`):

{% highlight powershell %}
$ defaults write com.apple.dock autohide-delay -float 1; killall Dock
{% endhighlight %}

After running this command, your Dock will restart, which will cause any minimized windows to reappear. Don't freak out. Your computer is not possessed. Now the Dock will only appear when you leave the mouse cursor motionless at the bottom of the screen for 1 second. If 1 second is too long, you can use a floating-point number (I currently use 0.5). Experiment with values and pick one that works for you (feel free to pick a value above 1 second as well).

If you want the Dock to go back to its default behavior, just set the delay back to zero:

{% highlight powershell %}
$ defaults write com.apple.dock autohide-delay -float 0; killall Dock
{% endhighlight %}

You can also prevent the Dock from automatically hiding. This can be done in `System Preferences > Dock`.

![Dock System Preferences]({{ site.url }}/images/posts/Dock-autohide.png)

Why would you want the Dock to always be present? Combined with a long delay time, you can effectively make the Dock appear on command (a keyboard command that is). In `System Preferences > Keyboard > Shortcuts > Launchpad & Dock` double-click the `Turn Dock Hiding On/Off` keyboard shortcut to change it if you want. I have mine set to `⌃⌥⌘Space` (`⌘Space` is for [Alfred](http://www.alfredapp.com) and `⌥⌘Space` is for Spotlight [I use Spotlight mainly when I want to make a FaceTime or phone call from my Mac]).

![Dock System Preferences]({{ site.url }}/images/posts/Dock-keyboard-shortcut.png)

Got any other productivity tips? Let me know!