# Debian

{% assign debian = site.github.public_repositories | where_exp: "i", "i.name contains 'debian-'" %}
{% for i in debian %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
