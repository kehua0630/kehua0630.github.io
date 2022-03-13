---
title: Hexo-備份原始碼
date: 2022-03-09 16:25:05
categories:
  - 學習筆記
  - Hexo
tags:
---

GitHub 上的 master 已用來部署靜態檔案，原始碼改上到分支

## 本地端

```bash
git init
git checkout -b branch #建本地分支
git add.
git commit -m "備註"
```

## 上傳到 Github

```bash
git remote add origin 儲存庫路徑 #這裡要修改上傳的儲存庫路徑
git push -u origin branch #推到遠端分支
```

\*儲存庫路徑: git@github.com:Owner/Owner.git
→ 去 GitHub Repository 看

## 出錯問題

- 推到 Git 出錯 - 有可能是先前資料卡住，先刪記錄後再推一次
```bash
git remote rm origin
```

- 金鑰錯誤
```bash
$ ssh-keygen   #產生金鑰
Generating public/private rsa key pair.
Enter file in which to save the key (key_path)):   #金鑰存放路徑，直接按 Enter

$ cat key_path #讀取路徑金鑰檔案，複製貼到GitHub
```


- 客製主題無法上傳
git指令不成功，直接把theme底下的主題資料夾刪除，再手動新增同名資料夾，把原本的檔案搬進去
```bash
$ git rm --cache themes/主題文件名 #刪除暂存區clone下來的檔案
```
<!-- 
把 themes/hexo-theme-icarus/.git文件夹到放到位置 比方说桌面
记得把 themes/hexo-theme-icarus/.gitignore里的 _config去掉
后面再把刚刚的.git文件夹移动回去 -->

---
參考網站：
- [備份 Hexo 原始檔案至 GitHub](https://hackmd.io/@tchung/HkhnqukIS#備份-Hexo-原始檔案至-GitHub)
- [Hexo - 版本控制與發佈到 GitHub](https://skychang.github.io/2015/10/19/Hexo-Source_Control_and_Deploy/)
- [Git 版本控制筆記 - 使用 github 及 ssh 金鑰設定](https://blog.jaycetyle.com/2018/02/github-ssh/)
- [Hexo 主题 themes-文件夹无法提交到 GitHub 的解决方法](https://blog.csdn.net/liaoweilin0529/article/details/113650333)
