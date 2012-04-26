---
layout: page
title: Oilbeater's Home!
---
{% include JB/setup %}
<head>
  <link rel="stylesheet" href="/css/main.css" type="text/css" />
</head>
<body class = "main">
  <p>
    <a href="http://www.baidu.com">This is my first page</a>
  </p>
  <ul class = "main">
  {% for post in site.posts %}
      <li>
          <h2>
            <a href="{{ post.url }}">{{ post.title }}</a>
          </h2>
          <span>{{ post.description }}</span>
      </li>
  {% endfor %}
  </ul>
</body>