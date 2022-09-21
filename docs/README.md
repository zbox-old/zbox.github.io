# zBox Development Platform

{% assign repos = site.github.public_repositories %}
{% for i in repos %}
  {% assign name = i.name | split: '-' | first %}
  * [{{ name }}](/{{ name }}/)
{% endfor %}
