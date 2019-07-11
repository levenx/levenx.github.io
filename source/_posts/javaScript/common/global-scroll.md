---
title: 【CSS】滚动条全局样式
date: 2019-07-11 13:39:00
photos: https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1562146098475&di=d38f5a0643942cf3746caba44c106c4d&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201801%2F16%2F20180116155559_eQPGR.thumb.700_0.jpeg
categories:
- CSS
tags:
-
  Web滚动条
---

### 【CSS】滚动条全局样式

****
<pre><code>
      ::-webkit-scrollbar{
        width: 5px;/* 纵向滚动条*/
        height: 5px;/* 横向滚动条 */
        background-color: #fff;
      }

      /*定义滚动条轨道 内阴影*/
      ::-webkit-scrollbar-track{
        -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0);
        background-color: #fff;
      }

      /*定义滑块 内阴影*/
      ::-webkit-scrollbar-thumb{
        -webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0);
        background-color: #D5D5D5;
      }
</code></pre>

---
>-webkit-box-shadow: inset 0 0 6px rgba(0,0,0,0);   

box-shadow的四个参数  
x-offset x 轴偏移 0  
y-offset y轴偏移 0  
blur 模糊值 5px  
color of shadow 阴影颜色
