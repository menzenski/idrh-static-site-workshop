---
layout: post
title: The Liquid Templating Language
date: "2016-02-13 14:40:40 -0600"
categories: jekyll
published: true
---

## The Liquid templating language

The [Liquid templating language][liquid] ([source][shop]) has roots in e-commerce. It was designed to allow [Shopify][shopify] vendors to customize the appearance of their web storefronts without presenting a security risk to the servers those sites are hosted on.

Jekyll layouts and included elements use Liquid to render HTML using the markdown that a site's author provides.

### Variable tags

Double curly braces <code class="filter">{% raw %}{{ }}{% endraw %}</code> are used to put the contents of a variable or expression into the HTML output. Something will always be put into the HTML at the location of these tags.

Here's a simple example: {{ site.baseurl }}

<pre>
<code class="filter">
{% raw %}Here's a simple example: {{ site.baseurl }}{% endraw %}
</code>
</pre>

### Logic tags

Curly braces with percent signs <code class="filter">{% raw %}{%  %}{% endraw %}</code> are used to direct logical flow.

A logic tag sometimes results in content being added to the page: the line <code class="filter">{% raw %}{% include footer.html %}{% endraw %}</code> in the `_layouts/default.html` template adds all of the code for the footer below into this post.

Logic tags are also used for things like **if statements** and **for loops**. These are powerful customization tools, if you're ready to dive a little deeper into Jekyll.


[liquid]: http://liquidmarkup.org/
[shop]: https://github.com/Shopify/liquid
[shopify]: https://www.shopify.com/
