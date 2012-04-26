---
layout: page
title: Oilbeater's Home!
---
{% include JB/setup %}
<head>
  <link rel="stylesheet" href="/css/main.css" type="text/css" />
</head>
<body>
  <div class="main">
    <ul>
    {% for post in site.posts %}
        <li class="posts">
            <h2>
              <a href="{{ post.url }}">{{ post.title }}</a>
            </h2>
            <span class="description">{{ post.description }}</span>
        </li>
    {% endfor %}
    </ul>
  </div>
  <div class="to_do_list">
    <aside>
    <h2>
      To do list
    </h2>
    <ul>
      <li>haha</li>
      <li>adsfaf</li>
      <li>dsf</li>
      <li>adsfaf</li>
    </ul>
    </aside>
  </div>
</body>