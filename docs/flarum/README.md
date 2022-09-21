# Flarum

{% assign dir = page.dir | remove: '/' %}

{% assign group = site.github.public_repositories | where: 'topics', dir %}
{% for i in group %}
  {% assign name = i.name | remove: dir | remove_first: '-' %}
  <span class="block">[{{ name }}]({{ name }})</span>
  <span class="block">{{ i.description }}</span>
  <span class="block text-gray"><small>
    [<i class="fa-brands fa-github fa-fw"></i>]({{ i.html_url }})
    [<i class="fa-solid fa-link fa-fw"></i>]({{ i.homepage }})
    <i class="fa-solid fa-copyright fa-fw"></i> `{{ i.license.spdx_id }}`
    <i class="fa-solid fa-code-fork fa-fw"></i> `{{ i.forks_count }}`
    <i class="fa-solid fa-star fa-fw"></i> `{{ i.stargazers_count }}`
    <i class="fa-solid fa-eye fa-fw"></i> `{{ i.watchers_count }}`
  </small></span>
{% endfor %}
