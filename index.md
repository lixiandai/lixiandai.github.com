---
layout: page
title: Lixian's GIT blog welcome you!
tagline: 
---
{% include JB/setup %}

<!-- This loops through the paginated posts -->
{% for post in site.posts %}
    <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
    <p class="post-date">
        <span class="date">{{ post.date| date: "%b-%-d-%Y" }}</span>
    </p>
    <ul class="tag_box inline">
        {% assign tags_list = post.tags %}
        {% include JB/tags_list %}
    </ul>

    <div class="content">
        {{ post.excerpt }}
    </div>
    <br>
{% endfor %}


