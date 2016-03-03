---
layout: post
title: The Liquid Templating Language
date: "2016-02-13 14:40:40 -0600"
categories: jekyll
published: true
---

The [Liquid templating language][liquid] ([source][shop]) has roots in e-commerce. It was designed to allow Shopify vendors to customize the appearance of their web storefronts without presenting a security risk to the servers those sites are hosted on.

Jekyll layouts and included elements use Liquid to render HTML using the markdown that a site's author provides.

## There are two basic types of Liquid **tags**:

#### Variables

Double curly braces are used to put the contents of a variable or expression into the HTML output. Something will always be put into the HTML at the location of these tags.

Here's a simple example: {{ site.baseurl }}

<pre>
<code class="filter">
Here's a simple example: {{ site.baseurl }}
</code>
</pre>

#### Logic

Curly braces with percent signs are used to direct logical flow.

[liquid]: http://liquidmarkup.org/
[shop]: https://github.com/Shopify/liquid
