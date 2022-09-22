# zBox Development Platform

{% assign groups = site.github.public_repositories | where_exp: "i", "i.name contains '-'" | group_by_exp: "i", "i.name | split: '-' | first" %}

<ul>
{% for i in groups %}
  <li>[{{ i.name }}](/{{ i.name }}/)</li>
{% endfor %}
</ul>
