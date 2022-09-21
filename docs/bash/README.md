# Flarum

{% assign bash = site.github.public_repositories | where_exp: "i", "i.name contains 'bash-'" %}
{% for i in bash %}
  {% assign name = i.name | remove: "bash-" %}
  * [{{ name }}]({{ name | remove: "bash-" }}/)  
  <small>[GitHub]({{ i.html_url }})</small>
{% endfor %}
