# XenForo

{% assign xenforo = site.github.public_repositories | where_exp: "i", "i.name contains 'xenforo-'" %}
{% for i in xenforo %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
