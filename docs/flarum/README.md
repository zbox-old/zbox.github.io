# Flarum

{% assign dir = page.dir | remove: "/" %}
{{ dir }}

{% assign group = site.github.public_repositories | where_exp: "i", "i.name contains 'flarum-'" %}
{% for i in group %}
  {% assign name = i.name | remove: "flarum-" %}
  <span class="block">[{{ name }}]({{ i.html_url }})</span>
  <span class="block"><small>{{ i.description }}</small></span>
  <span class="block">[README]({{ name }})</span>
{% endfor %}
