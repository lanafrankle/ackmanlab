---
layout: page  
title: Notes  
---

<ul class="post-list">
<li>
<span class="post-meta">{{ site.time | date: "%b %-d, %Y" }}</span>
<h2>
{% include icon-bananaslug.html %}
</h2>
</li>

{% for post in site.posts %}
<li>
<span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
<h2>
<a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
</h2>
</li>
{% endfor %}
</ul>
