---
title: "Jekyll/Github 블로그 만들기"
layout: archive
permalink: categories/blog
author_profile: true
sidebar_main: true

title: "Javascript 딥다이브"
layout: archive
permalink: categories/Javascript
author_profile: true
sidebar_main: true

title: "MySql"
layout: archive
permalink: categories/Mysql
author_profile: true
sidebar_main: true

title: "Php"
layout: archive
permalink: categories/Php
author_profile: true
sidebar_main: true
---


<!-- 공백이 포함되어 있는 카테고리 이름의 경우 site.categories['a b c'] 이런식으로! -->

***

{% assign posts = site.categories.Blog %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}