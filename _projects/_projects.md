---
layout: page
title: Projects
permalink: /projects/
---
<section class="list">
    {% for project in site.projects %}
        {% if project.hidden != true %}
            <div class="item {% if project.star %}star{% endif %}">
                <a class="url" href="{{ site.url }}{{ project.url }}">
                    <aside><time datetime="{{ project.date | date:"%Y" }}">{{ project.date | date: "%Y" }}</time></aside>
                    <h2 class="title">{{ project.title }}</h2>
                </a>
            </div>
        {% endif %}
    {% endfor %}
</section>
