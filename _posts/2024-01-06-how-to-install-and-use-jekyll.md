---
layout: post
author: shawn phy 
--- 

# Introduction 
[jekyll](https://jekyllrb.com/) is a static site generator which is used by most organistions including github pages.It is written in the [ruby programming language](https://www.ruby-lang.org/en/) In this post we will look at how to use jekyll to host some of your static pages. 

## static site generators
These are tools used by web developers to generate "static content". Static web pages sometimes also called flat pages, are pages which display the same content to all users in contrast to a [dynamic web page](https://en.wikipedia.org/wiki/Dynamic_web_page) which is served from a web application.

The content of static web pages remain stationary irrespective of the number of times it is viewed. Such web pages are suitable for the contents that rarely need to be updated, though modern web template systems are changing this. Maintaining large numbers of static pages as files can be impractical without automated tools, such as static site generators. This is where jekyll comes in.

Other static site generators include hugo, next.js, angular, gatsby.js. 

## Jekyll
![](/assets/images/jekyll.png)
Jekyll renders [Markdown](https://www.markdownguide.org/) or Textile and [Liquid templates](https://shopify.github.io/liquid/), and produces a complete, static website ready to be served by Apache HTTP Server, Nginx or another web server. If you are interested in creating your own jekyll themes you can study how the [liquid templating engnine](https://shopify.github.io/liquid/basics/introduction/) works. 

By default, Jekyll uses the [kramdown](https://kramdown.gettalong.org/) Markdown processor with stock settings, but you can enable other kramdown options or even switch Jekyll to another Markdown processor.

## Installing jekyll 
jekyll is a [ruby gem](https://jekyllrb.com/docs/ruby-101/#gems) and can be installed on nearly every system out there. 

There are independent installation instructions for every platform and this article will cover installation on windows and Ubuntu. Regardless of the platform or operating system you want to use jekyll on, the following requirements must be installed:
- [Ruby](https://www.ruby-lang.org/en/downloads/) version 2.5.0 or higher, including all development headers (check your Ruby version using `ruby -v`)
- [RubyGems](https://rubygems.org/pages/download) (check your Gems version using `gem -v`)
- GCC and Make (check versions using `gcc -v`,`g++ -v`, and `make -v`)

### Installing on windows
The documentation mentions that windows is not an ideal platform for development because it is not an officially supported platform. However, it can be used with the proper tweaks. 

Like most other software on windows, both ruby and jekyll can be installed using a single installer. The [ruby installer](https://rubyinstaller.org/) is a self-contained Windows-based installer that includes the Ruby language, an execution environment, important documentation, and more. 
