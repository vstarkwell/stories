---
layout: page
title: Archive
---

{% for post in site.posts %}
	{% capture currentyear %}{{post.date | date: "%Y"}}{% endcapture %}
{% if currentyear != year %}
##{{ currentyear }}##
    {% capture year %}{{currentyear}}{% endcapture %} 
  {% endif %}
  * [{{ post.title }}]({{ post.url}})
{% endfor %}