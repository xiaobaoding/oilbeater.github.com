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
  <div class="sidebar">
  <div class="to_do_list">
    <aside>
    <h2>
      To do list
    </h2>
    <ul>
      <li>读完python核心编程</li>
      <li>分布式和高体课本</li>
      <li>OO大作业</li>
      <li>
        <a href="http://markdown.tw" target="_blank">Markdown</a>
      </li>
      <li><a href="http://net.pku.edu.cn/~course/cs501/2012/assign/2012-Paxos_Practice.txt">Paxos_Practice</a></li>
      <li>解决图床问题</li>
      <li>还有…………</li>
      <li>再想一下……</li>
    </ul>
    </aside>
  </div>
  <div class="friendlink">
    <p><strong>乡亲们的链接</strong></p>
    <ul>
      <li>
        <a href="http://itester.me" target="_blank">iTester</a>
      </li>
      <li>
        <a href="http://pinderpeng.org" target="_blank">Pinder's Blog</a>
      </li>
    </ul>
  </div>
  </div>
  {% for post in site.posts %}
    {% if post.img != "secret" %}
      <div class="main">
        <ul>
          <li>
          <a href="{{ post.url }}">
            <img src="{{ post.img }}" alt="{{ post.title }}">
          </a>
          <div class="posts">
            <h3>
              <a href="{{ post.url }}">{{ post.title }}</a>
            </h3>
            <p>
              {{ post.date | date: "%B %e, %Y" }}
                &nbsp &nbsptag:
                {% for tag in post.tags %}
                 <a href="/tags.html#{{tag}}-ref">{{ tag }}</a>
                {% endfor %}
            </p>
            <span class="description">{{ post.description }}</span>
          </div>
          </li>
        </ul>
      </div>
    {% endif %}
  {% endfor %}
</body>
