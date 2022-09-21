# Flarum

{% assign dir = page.dir | remove: '/' %}

{% assign group = site.github.public_repositories | where: 'topics', dir %}
{% for i in group %}
  {% assign name = i.name | remove: dir | remove_first: '-' %}
  <span class="block">[{{ name }}]({{ name }})</span>
  <span class="block">{{ i.description }}</span>
  <span class="block"><small>
    [<i class="fa-brands fa-github fa-fw"></i>]({{ i.html_url }})
    [<i class="fa-solid fa-link fa-fw"></i>]({{ i.homepage }})
    <i class="fa-solid fa-copyright"></i> `{{ i.license.spdx_id }}`
    <i class="fa-solid fa-code-fork"></i> `{{ i.forks_count }}`
    <i class="fa-solid fa-star"></i> `{{ i.stargazers_count }}`
    <i class="fa-solid fa-eye"></i> `{{ i.watchers_count }}`
  </small></span>
{% endfor %}
