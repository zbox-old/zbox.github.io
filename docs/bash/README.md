# Flarum

{% assign bash = site.github.public_repositories | where_exp: "i", "i.name contains 'bash-'" %}
{% for i in bash %}
  * [{{ i.name }}]({{ i.html_url }})  
  {{ i.name | remove: "bash-" }}
{% endfor %}
