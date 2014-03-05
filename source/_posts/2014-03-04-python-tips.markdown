---
layout: post
title: "Python Tips"
date: 2014-03-04 16:44:44 +0800
comments: true
categories: Python
---

## enumerate ##
[enumerate](http://docs.python.org/2/library/functions.html#enumerate) 用于遍历, 与for in相比, 可同时返回index和element

    >>> seasons = ['Spring', 'Summer', 'Fall', 'Winter']
    >>> for i, elem in enumerate(seasons):
    ...   print i, elem
    ... 
    0 Spring
    1 Summer
    2 Fall
    3 Winter
    >>> 


## Counter ##
[collection.Counter](http://docs.python.org/2/library/collections.html#counter-objects) 专用于计数

    >>> from collections import Counter
    >>> c = Counter('ABBEDDAD')
    >>> c.keys()
    ['A', 'B', 'E', 'D']
    >>> c.values()
    [2, 2, 1, 3]
    >>> c.items()
    [('A', 2), ('B', 2), ('E', 1), ('D', 3)]


## map & reduce ##
[map](http://docs.python.org/2.7/library/functions.html#map) & [reduce](http://docs.python.org/2/library/functions.html#reduce) 是Map-Reduce中的map(注意不是C++ STL中的树容器map)和reduce

map用于对每一个元素执行一个函数/lambda

reduce用于对初值或当前结果与每一个元素执行一个函数, 得到下一个结果

[参考](http://www.cnblogs.com/zhoujinyi/archive/2013/06/07/3121976.html):

    >>> map(lambda x:x+x,range(5))   #lambda 函数，各项+本身
    [0, 2, 4, 6, 8]
    >>> reduce(add,range(11))        #1+2+3+...+10
    55

