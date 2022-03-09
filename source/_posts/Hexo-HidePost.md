---
title: Hexo-隱藏文章
date: 2022-03-09 15:14:07
categories: 
- 學習筆記
- Hexo
tags:
---

## 下載套件
``` bash
$ npm install hexo-hide-posts --save
```

## _config.yml增加設定
``` bash
# hexo-hide-posts
hide_posts:
  # 可以改成其他你喜欢的名字
  filter: hidden
  # 指定你想要传递隐藏文章的 generator，比如让所有隐藏文章在存档页面可见
  # 常见的 generators 有：index, tag, category, archive, sitemap, feed, etc.
  public_generators: []
  # 为隐藏的文章添加 noindex meta 标签，阻止搜索引擎收录
  noindex: true
```

## 文章設定
``` bash
hidden: true
```

---
參考網站：
- [hexo 隐藏文章插件 hexo+next-hidden-post](https://www.0412.cyou/type/heyc.html)

