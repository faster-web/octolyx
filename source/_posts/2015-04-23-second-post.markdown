---
layout: post
title:  "Next Post"
date:   2015-04-24 18:26:25
categories: jekyll post
---

Ok. Here's my second post. Hmm. This time I'll trying to write about poems. Code is poetry, right? 

<!--more-->

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}

Such a `beautiful` output. This is one of the reason why I really love [using this piece of generator][Jekyll] to writing my blog. If stucked, you'll be helped by [community's members][Jekyll helper] that gladly to help. 

[Jekyll]: https://jekyllrb.com
[Jekyll helper]: https://github.com/jekyll/jekyll-help
