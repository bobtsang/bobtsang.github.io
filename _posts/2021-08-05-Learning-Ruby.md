---
layout: post
title:  "Learning Ruby"
date:   2021-08-05 22:00:00 +0800
---

## Ruby Fundamentals

### Install Ruby

`Ruby` is pre-installed in Mac and it's better to install or manage different version with `RVM`

```{bash}
\curl -sSL https://get.rvm.io | bash -s stable
```

### Naming convention of variables

> Ruby uses a convention to help it distinguish the usage of a name: the first characters of a name indicate how the name is used. Local variables, method parameters, and method names should all start with a lowercase letter or with an underscore. Global variables are prefixed with a dollar sign ($), while instance variables begin with an \``at'' sign (@). Class variables start with two ``at'' signs (@@). Finally, class names, module names, and constants should start with an uppercase letter.

### Data Types

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


### Classes

![tree is not for this.use things properly]({{site.baseurl}}/resources/ruby-what-is-a-class.png)


## Ruby on Rails

### MVC: Model View Controller

- `Active Record`

## Reference

1. [Ruby Documentation](https://www.ruby-lang.org/en/documentation/)
2. [Ruby Version Manager: RVM](https://en.wikibooks.org/wiki/Ruby_Programming/Overview)
3. [Ruby Learning Resources](https://github.com/EbookFoundation/free-programming-books/blob/master/books/free-programming-books.md#ruby)
4. [Learn Ruby First](https://essenceofchaos.gitbooks.io/learn-ruby-first/content/)
5. [rubymonk:Learn Ruby Interactively](https://rubymonk.com/)
6. [Ruby on Rails: a web-application framework](https://rubyonrails.org/)