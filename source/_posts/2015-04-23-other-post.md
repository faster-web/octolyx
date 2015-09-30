---
layout: post
title:  "My First Post"
subtitle: "My First Post My First Post"
date:   2015-04-23 17:43:25
categories: jekyll post
published: false
---

Thank you for `Madhur` for creating `PortableJekyll-master` for Windows. Finally, a portable jekyll without `hassles` to install. Ok, back to the post. What I'm gonna say here? Hmm. Let's see. I think I'll try to write `code snippets` here to test Jekyll's capability in `syntax` highlighting.

<!--more-->

First code is `HTML` code:

{% highlight html %}
<div class="info">
    <h1>YO! Someone turned the lights off!</h1>
    <p>Sorry, but the page you were trying to view does not exist.</p>
    <p>It looks like this was the result of either:</p>
    <ul>
      <li>a mistyped address</li>
      <li>an out-of-date link</li>
    </ul>
    <p><a href="/">Try going back to the site</a></p>
  </div>
{% endhighlight %}

Next one is `Jade`:

```jade
.row
  .column.small-12
    dl.sub-nav.nav-ruled
      dd.active: a(href="") Home
      dd: a(href="") Projects
      dd: a(href="") Academic
      dd: a(href="") Skills
      dd: a(href="") About
      dd: a(href="") Contact
```

Below is `Sass`:

``` sass
.top-actions
  margin-top: 10px
  margin-bottom: -20px

.sub-nav
  background-color: #f2f2f2
  padding: 0.8em

.crimson-box
  background: blue
  border-radius: 5px
  color: white
  display: inline-block
  padding: 3px 0.5em
```

# Codes
``` ruby
class Float
  def number_decimal_places
    self.to_s.length-2
  end
  def to_fraction
    higher = 10**self.number_decimal_places
    lower = self*higher
    gcden = greatest_common_divisor(higher, lower)
 
    return (lower/gcden).round, (higher/gcden).round
  end
```
