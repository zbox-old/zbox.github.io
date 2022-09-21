# Flarum

{% assign flarum = site.github.public_repositories | where_exp: "i", "i.name contains 'flarum-'" %}
{% for i in flarum %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
