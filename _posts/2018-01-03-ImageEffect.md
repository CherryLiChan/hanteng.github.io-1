---
layout: article
title:  "头像效果"
date:   2018-01-03 21:14:24 +0800
categories: posts rwd
image:
  teaser: ImageEffect.jpg
  feature: ImageEffect.jpg
---

此文是我原fork的博客的头像效果的说明，效果暂时无法在此博客呈现，因此制作了下面的动图
![头像效果动图](/images/头像效果动图.gif)

{% include toc.html %}

## html对应代码
```
        <!-- 头像效果-start -->
        <div class="ih-item circle effect right_to_left">            
            <a href="/#blog" title="前往 {{ site.title }} 的主页" class="blog-button">
                <div class="img"><img src="/images/猫猫.jpg" alt="img"></div>
                <div class="info">
                    <div class="info-back">
                        <h2> 
                            {% if site.avatarTitle %}
                                {{site.avatarTitle}}
                            {% endif %}
                        </h2>
                        <p>
                           {% if site.avatarDesc %}
                                {{site.avatarDesc}}
                            {% endif %}
                        </p>
                    </div>
                </div>
            </a>
        </div>
        <!-- 头像效果-end -->
```

## css对应代码
```
html {
    font-family: sans-serif;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%
}

body {
    margin: 0
}

.ih-item.circle.effect {
    margin: 0 auto;
    -webkit-perspective: 900px;
    -moz-perspective: 900px;
    perspective: 900px;
}
.ih-item.circle.effect .img {
    z-index: 11;
    -webkit-transition: all 0.5s ease-in-out;
    -moz-transition: all 0.5s ease-in-out;
    transition: all 0.5s ease-in-out;
}

.ih-item.circle.effect .info {
    -webkit-transform-style: preserve-3d;
    -moz-transform-style: preserve-3d;
    -ms-transform-style: preserve-3d;
    -o-transform-style: preserve-3d;
    transform-style: preserve-3d;
}

.ih-item.circle.effect .info .info-back {
    opacity: 1;
    border-radius: 50%;
    width: 100%;
    height: 100%;
    background: #333333;
}

.ih-item.circle.effect .info h2 {
    color: #fff;    
    position: relative;
    font-size: 18px;
    margin: 0 auto;
    padding-top: 30px;
    height: 30px;
    text-shadow: 0 0 1px white, 0 1px 2px rgba(0, 0, 0, 0.3);
}

.ih-item.circle.effect .info p {
    color: #bbb;
    padding: 0px 0px 0px 0px;
    font-style: italic;
    padding-left: 0px;
    font-size: 10px;
}

.ih-item.circle.effect.bottom_to_top .img {
    -webkit-transform-origin: 50% 0;
    -moz-transform-origin: 50% 0;
    -ms-transform-origin: 50% 0;
    -o-transform-origin: 50% 0;
    transform-origin: 50% 0;
}

.ih-item.circle.effect.bottom_to_top a:hover .img {
    -webkit-transform: rotate3d(1, 0, 0, 180deg);
    -moz-transform: rotate3d(1, 0, 0, 180deg);
    -ms-transform: rotate3d(1, 0, 0, 180deg);
    -o-transform: rotate3d(1, 0, 0, 180deg);
    transform: rotate3d(1, 0, 0, 180deg);
}

.ih-item.circle.effect.top_to_bottom .img {
    -webkit-transform-origin: 50% 100%;
    -moz-transform-origin: 50% 100%;
    -ms-transform-origin: 50% 100%;
    -o-transform-origin: 50% 100%;
    transform-origin: 50% 100%;
}

.ih-item.circle.effect.top_to_bottom a:hover .img {
    -webkit-transform: rotate3d(1, 0, 0, -180deg);
    -moz-transform: rotate3d(1, 0, 0, -180deg);
    -ms-transform: rotate3d(1, 0, 0, -180deg);
    -o-transform: rotate3d(1, 0, 0, -180deg);
    transform: rotate3d(1, 0, 0, -180deg);
}

.ih-item.circle.effect.left_to_right .img {
    -webkit-transform-origin: 100% 50%;
    -moz-transform-origin: 100% 50%;
    -ms-transform-origin: 100% 50%;
    -o-transform-origin: 100% 50%;
    transform-origin: 100% 50%;
}

.ih-item.circle.effect.left_to_right a:hover .img {
    -webkit-transform: rotate3d(0, 1, 0, 180deg);
    -moz-transform: rotate3d(0, 1, 0, 180deg);
    -ms-transform: rotate3d(0, 1, 0, 180deg);
    -o-transform: rotate3d(0, 1, 0, 180deg);
    transform: rotate3d(0, 1, 0, 180deg);
}

.ih-item.circle.effect.right_to_left .img {
    -webkit-transform-origin: 0% 50%;
    -moz-transform-origin: 0% 50%;
    -ms-transform-origin: 0% 50%;
    -o-transform-origin: 0% 50%;
    transform-origin: 0% 50%;
}

.ih-item.circle.effect.right_to_left a:hover .img {
    -webkit-transform: rotate3d(0, 1, 0, -180deg);
    -moz-transform: rotate3d(0, 1, 0, -180deg);
    -ms-transform: rotate3d(0, 1, 0, -180deg);
    -o-transform: rotate3d(0, 1, 0, -180deg);
    transform: rotate3d(0, 1, 0, -180deg);
}

.ih-item a {
    color: #333;
}

.ih-item a:hover {
    text-decoration: none;
}

.ih-item img {
    width: 100%;
    height: 100%;
}

.ih-item.circle {
    position: relative;
    width: 120px;
    height: 120px;
    border-radius: 50%;
}

.ih-item.circle .img {
    position: relative;
    width: 120px;
    height: 120px;
    border-radius: 50%;
}
.ih-item.circle .img:before {
    position: absolute;
    display: block;
    content: '';
    width: 100%;
    height: 100%;
    border-radius: 50%;
    -webkit-transition: all 0.35s ease-in-out;
    -moz-transition: all 0.35s ease-in-out;
    transition: all 0.35s ease-in-out;
}

.ih-item.circle .img img {
    border-radius: 50%;
}

.ih-item.circle .info {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    text-align: center;
    border-radius: 50%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
}
@media all and (max-width: 780px) {
   .ih-item.circle .img {
      position: relative;
      width: 100px;
      height: 100px;
      /*margin-top: 20px;*/
      border-radius: 50%;
  }
  .ih-item.circle {
      position: relative;
      width: 100px;
      height: 100px;
      border-radius: 50%;
  }
  .ih-item.circle .info .info-back h2{
    font-size: 0.9em;
  }
}
```

如果你想要我博客里的头像效果，你只需要拿 CherryLiChan.github.io-/_includes/side-panel.html 文件里面 `头像效果` 和 CherryLiChan.github.io-/css/main.css 里面最后面 `头像效果` 部分就行了。

<br>

转载请注明：[黎婵的博客](https://cherrylichan.github.io) » [点击阅读原文](https://cherrylichan.github.io/posts/rwd/头像效果/)