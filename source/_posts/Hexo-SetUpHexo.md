---
title: Hexo-建立Hexo Blog
date: 2022-03-09 14:56:27
categories:
  - 學習筆記
  - Hexo
tags:
---

# 前置作業

### 1. 安裝[Node.js](https://nodejs.org/en/)

查看版本

```bash
$ node -v
$ npm -v
```

### 2. 安裝 Hexo Git

```bash
$ npm install hexo-deployer-git --save
```

### 3. 安裝 Hexo

```bash
$ npm install hexo-cli -g
```

查看版本

```bash
$ hexo version
$ hexo v
```

---

# 建立專案

```bash
$ hexo init blog       # 初始化 blog
$ cd blog              # 移動到剛創建的 blog 資料夾裡
$ npm install		# 安裝相關套件
```

---

# 連接 GitHub

### [GitHub](https://github.com)設定

- 登入並建立 new repository，Repository name 設為 Owner.github.io

### \_config.yml deploy 設定

```bash
# Deployment
deploy:
  type: git
  repo: https://github.com/Owner/Owner.github.io.git
  branch: master
```
\*Owner 為 GitHub 帳號


---
# 本機端開啟
```bash
$ hexo server
$ hexo s -p=3600 # 預設port=4000，可換其他port
```

# 部署
```bash
$ hexo clean # hexo cl 清除public檔案，第一次部署可不用
$ hexo generate # hexo g 產生靜態檔案(public)
$ hexo deploy # hexo d 部署至 https://Owner.github.io/ 
```

