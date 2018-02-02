---
layout: post
title:  "Github + Jekyll 小结"
date:   2018-02-01 13:48:35 +0800
categories: jekyll update
---


Overview
--------

介绍如何在`Github`上搭建`Jekyll`轻量级博客的文章已经很多了，这里就不再狗尾续貂。只不过对于像我一样零基础的小白来说，高屋建瓴地了解这两点很重要，直接引用[Jason 陈振捷][ceyes_blog]的说法吧：

> 1. 你可以通过 yourid.github.io 的域名去访问你的名为yourid.github.io repo 的 github page。
> 2. github page 的后台是jekyll，而jekyll是一个由ruby写的静态网站生成器。

现在有很多不同的Theme可以拿来直接用。不过我都没有采用：计划太宏伟的蓝图往往没有勇气迈出第一步。个人还是比较喜欢从最基本的功能开始使用，慢慢熟悉功能，等必不得已的时候才去探索更高一级的技巧。我就是这样慢慢开始上手了mutt，screen，irssi 等工具的。


Example content
--------

小白还不太了解怎么使用特殊语法，下面罗列一些例子（恩是的，我也看不懂拉丁文）。

## Heading1
### Heading2
#### Heading3

Cum sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum. Sed posuere consectetur est at lobortis. Cras mattis consectetur purus sit amet fermentum.

> Curabitur blandit tempus porttitor. Nullam quis risus eget urna
> mollis ornare vel eu leo. Nullam id dolor id nibh ultricies vehicula
> ut id elit.

Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum. Aenean lacinia bibendum nulla sed consectetur.

### Inline HTML elements

HTML defines a long list of available inline tags, a complete list of which can be found on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

- **To bold text**, use `<strong>`.
- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup
  Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins>
  text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript
  <sub>text</sub> uses `<sub>`.

Most of these elements are styled by browsers with few modifications on our part.


### Code

Jekyll can offer powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Cum sociis natoque penatibus et magnis dis `code element` montes, nascetur ridiculus mus.

{% highlight js %}
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of
// those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
{% endhighlight %}

Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa.

### Lists

Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.

* Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
* Donec id elit non mi porta gravida at eget metus.
* Nulla vitae elit libero, a pharetra augue.

Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue.

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

Cras mattis consectetur purus sit amet fermentum. Sed posuere consectetur est at lobortis.

### Tables

Aenean lacinia bibendum nulla sed consectetur. Lorem ipsum dolor sit amet, consectetur adipiscing elit.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

Nullam id dolor id nibh ultricies vehicula ut id elit. Sed posuere consectetur est at lobortis. Nullam quis risus eget urna mollis ornare vel eu leo.

Above come from <a href="https://github.com/poole/poole/issues/new">Github poole</a>


References
--------

列一下个人觉得比较有诚意的文章：Nicholas Cerminara 的 [Getting Started with Jekyll][start_jekyll]

下面这段话是Jekyll自带的example post里面的，实在不好意思全部删掉：
Check out the [Jekyll docs][jekyll_docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll_gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll_talk].

[ceyes_blog]: http://ceyes.github.io/2014-04/Blog-on-Github-with-Jekyll/
[start_jekyll]: https://scotch.io/tutorials/getting-started-with-jekyll-plus-a-free-bootstrap-3-starter-theme
[jekyll_docs]: https://jekyllrb.com/docs/home
[jekyll_gh]:   https://github.com/jekyll/jekyll
[jekyll_talk]: https://talk.jekyllrb.com/

