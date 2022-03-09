---
title: Hexo-新增文章
date: 2022-03-09 11:38:28
categories: 
- 學習筆記
- Hexo
tags:
---

# 基本指令
``` bash
$ hexo new [layout] "Article Title"
```
- Article Title若含空白鍵，需用引號包覆

## layout (draft, page, post)
- scaffolds 資料夾內有layout
1. post: 新增文章
- 未指定layout的預設值，可從_config.yml修改default_layout: post
- 可在_posts內找到文章

2. draft: 草稿
- 預設不會包含在靜態檔案內，部署後看不到此文章，要查看草稿可用
1. 從_config.yml修改render_drafts: false
2. hexo g --draft or hexo s --draft
- 草稿完成，準備發佈可用，文章會從_drafts移至_posts
``` bash
$ hexo publish draft xxx.md
```

3. page
- 會在source下生成一個資料夾(目錄)，作為網址路徑(文章分類使用)
