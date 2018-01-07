---
layout: page
title: Projects
---
<section class="list">
    {% for post in site.posts %}
        {% if post.projects %}
            <div class="item {% if post.star %}star{% endif %}">
                <a class="url" href="{% if post.externalLink %}{{ post.externalLink }}{% else %}{{ site.url }}{{ post.url }}{% endif %}">
                    <aside><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d %Y" }}</time></aside>
                    {{ post.jemoji }}<h3 class="title">{{ post.title }}</h3>
                    <div class="description"><p>{{ post.description }}</p></div>
                </a>
            </div>
        {% endif %}
    {% endfor %}
</section>