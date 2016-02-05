---
layout: page
title: Corporate Engineering Blogs
---

### with Github repos and career/jobs link
<section class="techblogs-flex-layout">
<div class="flex-container">
{% assign sorted_techblogs = (site.data.techblogs | sort: 'desc') %}
{% for techblog in sorted_techblogs %}
<div class="DataSpec"><a class="DataSpec-blog" href="{{ techblog.url }}">{{ techblog.desc }}</a>
<a class="DataSpec-repo" href="https://github.com/{{ techblog.github }}"><span class="octicon-mark-github small-octicon"></span>/{{ techblog.github }}</a>
<a class="DataSpec-jobs" href="{{ techblog.jobs }}">Jobs</a>  
</div>
{% endfor %}
</div>
</section>