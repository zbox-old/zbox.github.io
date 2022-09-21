# Drupal

{% assign drupal = site.github.public_repositories | where_exp: "i", "i.name contains 'drupal-'" %}
{% for i in drupal %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
