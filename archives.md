---
id: 1068
title: Archives
date: 2014-12-17T15:13:13+00:00
author: bitcoinkn
layout: page
guid: http://podcast.runtogold.com/?page_id=1068
bitcointips_address:
  - 174e2jBktiY6Fa4aYPXCPaUQoh91gWWQfq
views:
  - "17763"
permalink: /archives/
type: archive
---


<h3 id="archive">Archive of all episodes of The Bitcoin Knowledge Podcast:</h3>

<input type="text" id="search-input" placeholder="Search blog posts..">
<div id="search-index">
<ul id="results-container">
    
</ul>
</div>

<div id="post-index">
{% for post in site.posts %}
   {% assign currentDate = post.date | date: "%Y" %}
   {% if currentDate != myDate %}
       {% unless forloop.first %}</ul>{% endunless %}
       <h1>{{ currentDate }}</h1>
       <ul>
       {% assign myDate = currentDate %}
   {% endif %}
   <li><a href="{{site.baseurl}}{{ post.url }}"><span>{{ post.date | date: "%B %-d, %Y" }}</span> - {{ post.title }}</a></li>
   {% if forloop.last %}</ul>{% endif %}
   {% endfor %}
</div>