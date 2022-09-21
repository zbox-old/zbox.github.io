# Flarum

{% assign mediawiki = site.github.public_repositories | where_exp: "i", "i.name contains 'mediawiki-'" %}
{% for i in mediawiki %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
