---
layout: page
title: Oilbeater 的部落格
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
            <p>
              {{ post.date | date: "%B %e, %Y" }}
            </p>
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
      <li><s>写完第一篇博客</s></li>
      <li>加入about页面</li>
      <li>加入404</li>
      <li>美化theme</li>
      <li>购买域名</li>
      <li>上线</li>
      <li>还有…………</li>
      <li>再想一下……</li>
    </ul>
    </aside>
  </div>
</body>
