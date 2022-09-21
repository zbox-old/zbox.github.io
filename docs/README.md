# zBox Development Platform

{% assign repos = site.github.public_repositories | group_by_exp: "item", "item.name | split: '-' | first" %}
{% for i in repos %}
  * [{{ i.name }}](/{{ i.name }}/)
{% endfor %}
