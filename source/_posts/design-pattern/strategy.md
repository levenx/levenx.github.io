---
title: 【设计模式】策略模式
date: 2019-07-03 16:31:44
photos: https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1562146098475&di=d38f5a0643942cf3746caba44c106c4d&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201801%2F16%2F20180116155559_eQPGR.thumb.700_0.jpeg
categories:
- 设计模式
tags:
- 设计模式
- 策略模式
---

### 策略模式
  **&emsp;&emsp;定义了一系列算法，并将每一个算法封装起来，使得每个算法都可以相互替代，使算法本身和使用算法的客户端互相独立。**

  *分离算法,选择实现*

  >体现开闭原则，里氏替换原则

  > 策略模式是一个扁平的结构，各个策略实现都是兄弟关系，实现了同一个接口或者继承了同一个抽象类，这样只要使用策略的客户端保持面向抽象编程，就可以动态的切换不同的策略实现以进行替换。
