# Flarum

{% assign group_exp = page.dir | remove: "/" | append: "-" %}

{% assign group = site.github.public_repositories | where_exp: "i", "i.name contains group_exp" %}
{% for i in group %}
  {% assign name = i.name | remove: group_exp %}
  <span class="block">[{{ name }}]({{ name }})</span>
  <span class="block"><small>{{ i.description }}</small></span>
  <span class="block">[<i class="fa-brands fa-github"></i>]({{ i.html_url }})</span>
{% endfor %}
