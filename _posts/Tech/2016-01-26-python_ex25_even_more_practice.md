---
layout: post
title: 函数以及变量python练习
category: Tech 
tags: Python
keywords: python
description:
---

以下将对函数和变量的学习做更多的练习，以便很好的理解它们是如何使用的。

####程序源代码
{% highlight python %}
# -*- coding: utf-8 -*-
def break_words(stuff):
    """This function will break up words for us"""
    words = stuff.split(' ')
    return words

def sort_words(words):
    """Sorts the words."""
    return sorted(words)

def print_first_word(words):
    """Prints the first word after popping it off"""
    word = words.pop(0)
    print word

def print_last_word(words):
    """Prints the last word after popping it off"""
    word = words.pop(-1)
    print word
    
def sort_sentence(sentence):
    """Takes in a full sentence and returns the sorted words"""
    words = break_words(sentence)
    return sort_words(words)

def print_first_and_last(sentence):
    """Prints the first and last words of the sentence"""
    words = break_words(sentence)
    print_first_word(words)
    print_last_word(words)

def print_first_and_last_sorted(sentence):
    """Sorted the words the prints the first and last one"""
    words = sort_sentence(sentence)
    print_first_word(words)
    print_last_word(words)
{% endhighlight %}

####运行方式以及结果
```
fantasy@fantasy:~/python_src$ python
Python 2.7.6 (default, Jun 22 2015, 17:58:13) 
[GCC 4.8.2] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import ex25_even_more_practice
>>> sentence = "All good things come to those who wait"
>>> words = ex25_even_more_practice.break_words(sentence)
>>> words
['All', 'good', 'things', 'come', 'to', 'those', 'who', 'wait']
>>> sorted_words = ex25_even_more_practice.sort_words(words)
>>> sorted_words
['All', 'come', 'good', 'things', 'those', 'to', 'wait', 'who']
>>> ex25_even_more_practice.print_first_word(words)
All
>>> ex25_even_more_practice.print_last_word(words)
wait
>>> words
['good', 'things', 'come', 'to', 'those', 'who']
>>> ex25_even_more_practice.print_first_word(sorted_words)
All
>>> ex25_even_more_practice.print_last_word(sorted_words)
who
>>> sorted_word
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'sorted_word' is not defined
>>> sorted_words
['come', 'good', 'things', 'those', 'to', 'wait']
>>> sorted_words = ex25_even_more_practice.sort_sentence(sentence)
>>> sorted_words
['All', 'come', 'good', 'things', 'those', 'to', 'wait', 'who']
>>> ex25_even_more_practice.print_first_and_last(sentence)
All
wait
>>> ex25_even_more_practice.print_first_and_last_sorted(sentence)
All
who
>>> 

```
