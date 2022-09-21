# PowerShell

{% assign pwsh = site.github.public_repositories | where_exp: "i", "i.name contains 'pwsh-'" %}
{% for i in pwsh %}
  * [{{ i.name }}]({{ i.html_url }})
{% endfor %}
