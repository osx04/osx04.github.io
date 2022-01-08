---
layout: page
title: Projects
permalink: /projects/
---
<style type="text/css" media="screen">
  .github-icon {
    fill: #111;
  }

  .projects-list {
    list-style-type: none;
    margin-left: 0;
  }
</style>

<ul class="projects-list">
{% for project in site.projects %}
  <li>
    <h2>{%- if project.hosted_url -%}<a href="{{ project.hosted_url }}">{{ project.name}}</a>{%- else -%}{{ project.name}}{%- endif -%}</h2>
    {{ project.content | markdownify }}
    {%- if project.github_url -%}
    <a href="{{ project.github_url }}"><svg class="svg-icon github-icon"><use xlink:href="/assets/minima-social-icons.svg#github"></use></svg></a>
    {%- endif -%}
  </li>
{% endfor %}
</ul>