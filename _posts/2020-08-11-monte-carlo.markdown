---
title: "Research"
layout: post
date: 2020-01-23 22:10
tag: jekyll
image: /assets/images/MonteCarlo.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "This is a simple and minimalist template for Jekyll for those who likes to eat noodles."
category: project
author: Sian Lee Kitt
externalLink: false
---



[Simulation Details!][1]

{% assign orderedRepos = site.github.public_repositories | sort: 'stargazers_count' | reverse %}
{% for repository in orderedRepos %}
{% assign homepageLength = repository.homepage | size %}
{% if homepageLength > 0 %}
### {{repository.name}} | [repo]({{ repository.html_url }}) | [pages]({{ repository.homepage }}) 
{% else %}
### {{repository.name}} | [repo]({{ repository.html_url }})
{% endif %}
<div style="border-left: 3px solid #CCC; padding-left: 10px; margin-bottom: 30px">
<i>{{repository.description}}</i>
<p style="margin-top: 5px"><span style="margin-right:10px">{% octicon repo-forked size:small%} {{repository.forks_count}}</span> {% octicon star size:small %} {{repository.stargazers_count}} </p>
</div>

{% endfor %}

---



[1]: https://github.com/Siaan/MonteCarloSimulation

