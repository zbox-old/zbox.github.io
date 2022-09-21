# Flarum

{% assign dir = page.dir | remove: '/' %}

{% assign group = site.github.public_repositories | where: 'topics', dir %}
{% for i in group %}
  {% assign name = i.name | remove: dir | remove_first: '-' %}
  <span class="block">
    [{{ name }}]({{ name }})
    [<i class="fa-brands fa-github fa-fw"></i>]({{ i.html_url }})
    [<i class="fa-solid fa-link"></i>]({{ i.homepage }})
  </span>
  <span class="block">{{ i.description }}</span>
{% endfor %}
