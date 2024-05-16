---
layout: default
title: Blog
---
<hr  class="mt-2"/>
[[Home]]({{site.url}})
<hr />
### Blogs
_Trying to organize my thoughts, ideas, and discoveries._

<div class="container mx-auto my-6">
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-0">
    {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
    {% for post in sorted_posts %}
        <div class="pl-4 column">
            <hr class="mx-auto mt-5 mb-2 w-2/6" />
            <h6><a href="{{post.url}}" style="text-decoration:none"> {{post.title}} </a></h6>
            <div class="text-centered">
              {% for tag in post.tags %}
                <i>#{{ tag }} </i>
              {% endfor %}
            </div>
            <div class="text-justified">{{post.description}}</div>
        </div>
    {% endfor %}
{% include grid-end.html %}
