---
layout: post
title: Customizing Your Site
date: "2016-02-14 14:40:40 -0600"
categories: jekyll
published: true
---

## Customizing Your Site

### Data

If you want to make use of additional data in your site, create a folder named `_data`. Jekyll will automatically look in this folder when it generates your site and load any `.yml`, `.json`, and `.csv` files stored there.

This site has two authors, so we created a `_data/authors.yml` file to store their information. Our file looks like this:

<pre>
<code class="filter">
{% raw %}- name: Brian Rosenblum
  email: brianlee@ku.edu
  github: blros
  twitter: blros

- name: Matt Menzenski
  email: menzenski@ku.edu
  github: menzenski
  twitter: menzenski{% endraw %}
</code>
</pre>

Each entry is signaled by a hyphen `-`, and we can iterate over the authors using a for loop:

{% for author in site.data.authors %}
**name:** {{ author.name}}

**twitter:** [@{{ author.twitter }}](https://twitter.com/{{ author.twitter }})
{% endfor %}

<pre>
<code class="filter">
{% raw %}{% for author in site.data.authors %}
**name:** {{ author.name}}

**twitter:** [@{{ author.twitter }}](https://twitter.com/{{ author.twitter }})
{% endfor %}{% endraw %}
</code>
</pre>
