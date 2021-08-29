---
layout: post
title:  "Learning Ruby"
date:   2021-08-05 22:00:00 +0800
---

## Install Ruby
`Ruby` is pre-installed in Mac and it's better to install or manage different version with `RVM`

```{bash}
\curl -sSL https://get.rvm.io | bash -s stable
```

## Data Types

- Range

```{bash}
>> a = 1...9
>> a.include?(9)
false

>> a = 1..9
>> a.include?(9)
true
```
- String

> The essential difference between using `single` or `double` quotes is that `double quotes` **allow** for escape sequences while single quotes do not.


## Classes

![tree is not for this.use things properly]({{site.baseurl}}/resources/ruby-what-is-a-class.png)

## Reference

1. [Ruby Documentation](https://www.ruby-lang.org/en/documentation/)
2. [Ruby Version Manager: RVM](https://en.wikibooks.org/wiki/Ruby_Programming/Overview)
3. [Ruby Learning Resources](https://github.com/EbookFoundation/free-programming-books/blob/master/books/free-programming-books.md#ruby)
4. [Learn Ruby First](https://essenceofchaos.gitbooks.io/learn-ruby-first/content/)
5. [rubymonk:Learn Ruby Interactively](https://rubymonk.com/)