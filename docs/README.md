# zBox Development Platform

{% assign groups = site.github.public_repositories | where_exp: "i", "i.name contains '-'" | group_by_exp: "i", "i.name | split: '-' | first" %}

{% for i in groups %}
  [{{ i.name }}]({{ i.name }})
{% endfor %}
