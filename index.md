---
layout: page
title: Oilbeater 的部落格
tagline: Use it wisely , enjoy it as long as posible , that's youth!
---
{% include JB/setup %}
<head>
  <link rel="stylesheet" href="/css/main.css" type="text/css" />
</head>
<body>
  <div class="main">
    <ul>
    {% for post in site.posts %}
        <li>
            <img src="{{ post.img }}" alt="{{ post.title }}">
            <div class="posts">
              <h3>
                <a href="{{ post.url }}">{{ post.title }}</a>
              </h3>
              <p>
                {{ post.date | date: "%B %e, %Y" }}
              </p>
              <span class="description">{{ post.description }}</span>
            </div>
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
      <li>美化theme</li>
      <li>重构底层代码结构</li>
      <li>解决图床问题</li>
      <li>写读书笔记</li>
      <li><s>写完第一篇博客</s></li>
      <li><s>加入about页面</s></li>
      <li><s>加入404</s></li>
      <li><s>fix tag bug</s></li>
      <li><s>购买域名</s></li>
      <li><s>上线</s></li>
      <li>还有…………</li>
      <li>再想一下……</li>
    </ul>
    </aside>
  </div>
</body>
