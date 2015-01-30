---
layout: post
type:
title: When you assume, you make an ASCII out of UTF-8 and me
description:
headline:
category: programming
tags:
  - fountainhead
  - character sets
  - python
  - sublime text
imagefeature: new-old-stock-children-classroom.jpg
comments: true
mathjax:
---
Recently, a user of [Fountainhead](/fountainhead) let me know that writing accented letters broke syntax highlighting and autocompletions. This surprised me for two reasons: I've managed localization departments in the past so I should have remembered that there are more letters in heaven and earth than 26, and Python 3 (which Sublime Text 3 packages use) defaults to encoding strings in UTF-8.

Solving the syntax highlighting was relatively painless, though I did learn something interesting while testing out that letters are converted between lowercase and uppercase: ß (sharp s) is the only letter in the Latin alphabet that [has no traditional uppercase form](http://en.wikipedia.org/wiki/Capital_ẞ).

Looking at Sublime Text's console, and seeing:
`UnicodeEncodeError: 'ascii' codec can't encode character...`,
it became apparent that while the text strings are using UTF-8 character mapping, the file they were being written to is being encoded as ASCII. My mistake was thinking that just because a certain character set is used to display a string of text, it doesn't mean that it will automatically be encoded as such when written to a file. The solution was to make sure that files are always encoded as UTF-8. Luckily [Python](https://docs.python.org/3.4/library/codecs.html) (and [Stack Overflow](http://stackoverflow.com/a/1207836)!) makes this easy:
{% highlight python %}
import codecs
f = codecs.open('path/to/file.txt','w','utf8')
f.write(my_unicode_string)  # Stored on disk as UTF-8
{% endhighlight %}

For a great primer on character sets and the differences between ASCII and UTF-8, read Joel Spolsky's "[The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!)](http://www.joelonsoftware.com/articles/Unicode.html)".