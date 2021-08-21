---
title: Github Blog Hexo Hueman Theme Custom
date: 2021-08-20 23:35:02
tags: Git
categories: Git
---
# Hexo Hueman Theme Custom 방법

**1. Main Title**
* themes -> hueman-> _config.yml문서안 customize -> logo-> url: 여기에 원하는 이미지를 넣으면된다
![](source/image/hexo theme custom/1.PNG)

**2. Sub Title**
* themes -> hueman-> layout -> common -> header.ejs 문서안  < h2 >가 속해잇는 if문에 if문을 지워주고 원하는 subtitle을 적어준다
![](source/image/hexo theme custom/2.PNG)
![](source/image/hexo theme custom/3.PNG)

**3. Favicon**
* themes -> hueman-> _config.yml문서안 customize -> Favicon: 여기에 원하는 이미지를 넣으면된다 경로는 아래 사진처럼 'css/images/원하는이미지' 잡아주면된다. 
![](source/image/hexo theme custom/4.PNG)

