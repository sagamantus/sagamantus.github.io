{% include grid.html %}
    {% for project in site.data.projects %}
        {% include col.html heading=project.heading subheading =project.subheading content=project.content %}
   {% endfor %}
{% include grid-end.html %}
