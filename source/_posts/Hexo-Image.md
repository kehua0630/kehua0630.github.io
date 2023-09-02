---
title: Hexo-插入圖片
date: 2022-03-27 12:46:22
categories: 
- 學習筆記
- Hexo
tags:
---

## 本機圖片
### 安裝套件
```bash
$ npm install https://github.com/CodeFalling/hexo-asset-image --save
```

### 更改 _config.yml
```bash
post_asset_folder: true
```

### 路徑
post_asset_folder為true，hexo new 生成新文章時，會在_post底下建立一個相同檔名的資料夾
```bash
![圖片描述](./圖片.jpg)
![圖片描述](./資烙夾/圖片.jpg)
![圖片描述](資烙夾/圖片.jpg)
```

### 外部圖片
```bash
![圖片描述](圖片連結)
```
