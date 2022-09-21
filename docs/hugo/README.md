# Flarum

{% assign hugo = site.github.public_repositories | where_exp: "i", "i.name contains 'hugo-'" %}
{% for i in hugo %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
