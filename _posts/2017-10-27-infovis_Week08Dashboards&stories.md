---
layout: article
title:  "仪表板和故事"
date:   2017-10-27 21:14:24 +0800
categories: posts infovis
image:
  teaser: DashboardsStories.jpg
  feature: DashboardsStories.jpg
---
Week08笔记_仪表板和故事

{% include toc.html %}

## 可用网址
- [天善智能问答社区](https://www.hellobi.com/)
- [Tableau Public](https://public.tableau.com/s/)-->点GALLERY-->点搜索图标搜索故事（有好有坏自己甄别）

## 打开学习网站的方法：
**打开cmd**
1. 输入ipconfig，回车
2. 输入nsloopup，回车
3. 输入e.nfu.edu.cn,回车
4. 打开notepad（用管理员打开）
5. 查windows 8 hosts的位置
6. 打开这个位置（用notepad打开hosts）
7. 改e.nfu.edu.cn 为 10.10.240.80

## Pandas_Bokeh_
输入两个csv档，输出tsv档

#### Step1 制作工作表
1. 用tableau打开GDP_POP_pct_change_rank
2. 用POP_增长率、GDP_增长率做散点图
   地区：详细信息、标签
3. 把“年”拉到页面-->智能显示
4. 建两个工作表：
    a.散点-时间最近
    b.散点-时间最远

#### Step2 创建仪表板
5. 建仪表板：整合两个工作表
6. 工作表3：地区、GDP_增长率排行、[年]->确定（重命名排序）
7. 创建计算字段

#### Step3 写故事
**工作表5：**
1. “年”（离散值）、"地区"
2. GDP增长率：颜色（可根据正负编辑颜色）、标签、方形
3. 只能显示右上角
4. 右键->设置格式



转载请注明：[黎婵的博客](https://cherrylichan.github.io/) » [点击阅读原文](https://cherrylichan.github.io/posts/infovis/Week08_仪表板和故事/)









