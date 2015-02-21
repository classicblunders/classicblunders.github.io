---
layout: post
type:
title: Fountainhead Version 1 Released
description:
headline:
category: screenwriting
tags:
  - fountainhead
  - fountain
imagefeature: angelic-contrast-tiber-rome-tom-eversley.jpg
comments: true
mathjax:
---

The first official release of Fountainhead has been focused on providing a great screenwriting environment to extract what is in one's head onto the page. I have tried my best to only include the features that will help with this goal, and to resist adding something just because I think it'd be neat. I also realize that many people work differently than me, so I've tried my best to keep Fountainhead's settings easily customizable.

One of the things that existing Fountainhead users will notice, are that character and scene autocompletions are no longer converted to lowercase. I originally decided to convert the completions to lowercase in order to provide better autocompletion suggestions (since characters and scenes are written in lowercase), but I've found that Sublime Text is smart enough to not make this an issue. Additionally, keeping character and scene autocompletions in uppercase makes it much easier to edit (you no longer have to press `Return` to convert the line to uppercase, only to then have to delete the extraneous line).

But what if you want to change a character or scene heading to one that hasn't been entered before? Would you then have to do the lowercase, `Return`, delete dance? Previously, if you wanted to make text either all lowercase or uppercase, you would have to highlight the text, and then press the appropriate commands: ⌘K,⌘L or ⌘K,⌘U (Windows/Linux: ⌃K,⌃L or ⌃K,⌃U)\*. Now you can convert an entire line to uppercase using ⌘K,K (⌃K,K). This works no matter where the cursor is and you no longer have to highlight the desired text.

Support for the Fountain syntax has been improved, and should be completely up to date with the latest version, 1.1. Lyrics are now fully supported: start any line with a `~`(tilde). You can see a complete guide to the Fountain syntax on [Fountain.io](http://fountain.io/syntax).

Lastly, users are now able to take full advantage of all of Sublime Text's non-Fountainhead color schemes (dialogue no longer looks so out of place). [Colorsublime](https://github.com/Colorsublime/Colorsublime-Plugin) provides a cornucopia of color schemes and an easy way to browse and install them.

Hopefully you find Fountainhead a valuable tool in your screenwriting workflow. In the near future, I plan on bringing the ability to preview screenplays and save them as PDFs. If you have any suggestions or issues, feel free to tweet me ([@derickety](https://twitter.com/derickety)) or [submit an issue](https://github.com/derickc/Fountainhead/issues) in GitHub.

For a full list of changes, please view the [CHANGELOG](https://github.com/derickc/Fountainhead/blob/master/CHANGELOG.txt).

\* *⌘K,⌘L means "Press `⌘K` followed by pressing `⌘L`"*
