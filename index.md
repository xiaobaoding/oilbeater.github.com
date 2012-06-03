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
    <div class="to_be_continue">
    <h2>即将推出</h2>
    <ul>
      <li>
        栈溢出和堆溢出
      </li>
      <li>
        历史的忧思
      </li>
      <li>
        Learn it the hard way
      </li>
    </ul>
  </div>
  <div class="to_do_list">
    <aside>
    <h2>
      要种的地
    </h2>
    <ul>
      <li>
        <a href="http://markdown.tw" target="_blank">Markdown</a>
      </li>
      <li><a href="https://github.com/oilbeater/ACT" target="_blank">重构编译优化器代码</a></li>
      <li>再想一下……</li>
    </ul>
    </aside>
  </div>
    <div class="doing_list">
    <aside>
    <h2>
      正在种的地
    </h2>
    <ul>
      <li><a href="http://book.douban.com/subject/1984303/" target="_blank">Computer Architecture</a></li>
      <li>
        <a href="http://book.douban.com/subject/2343820/" target="_blank">Distributed System</a>
      </li>
      <li><a href="http://book.douban.com/subject/3112503/" target="_blank">Python核心技术</a></li>
    </ul>
    </aside>
  </div>
      <div class="done_list">
    <aside>
    <h2>
      种过的地
    </h2>
    <ul>
      <li><a href="https://github.com/oilbeater/Paxos" target="_blank">Paxos C实现</a></li>
      <li><a href="https://github.com/oilbeater/Tournament-Predictor">分支预测器 C++实现</a></li>
      <li>
        <a href="https://github.com/oilbeater/ACT" target="_blank">编译优化器</a>
      </li>
      <li><a href="https://github.com/oilbeater/oilbeater.github.com" target="_blank">简陋的部落</a></li>
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
