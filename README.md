
# 利用微信小程序每天赚到一顿饭钱

## 写在前面

某天下午，我正在公司认真的写着代码，突然我的手机弹了一个通知，我赶紧抓起手机看看（给自己一个摸鱼的理由）

我啪的一下打开手机，很快啊，让我看看到底是谁发消息打扰我工作。

害，原来是某个群转发了一个外卖红包，我失望的刚想放下手机，但是看了一眼电脑上的代码，算了算了，还是再看看手机吧。说不定这不是一个外卖红包这么简单呢？

满30减8，就这？？？

看着手机屏幕上的满减券，我陷入了沉思，为什么这个人要转发一个红包到群里呢，这不是让我捡便宜了吗？

不会他真的是一个好人吧，从不利己专门利人？

我把键盘推开，然后仔细看看这个红包，嗷，原来分享给别人之后，如果别人消费了，那么他就可以拿到佣金。

哦豁？

于是一个小想法在我脑子里出现

---

## 美团，饿了么联盟
这俩都是外卖平台的联盟，简单的说就是可以在这里拿到一个链接，别人用这个链接下单了，你就可以拿到一定比例的佣金

## 微信小程序
微信小程序大家应该都很熟悉了，基本每天都出现在手机，可能你没注意过，但是只要你打开微信，各种服务都是用微信小程序实现

## 想法开始实践
我要先注册每天和饿了么联盟，然后整一个微信小程序，让用户从这里领红包，然后我就能拿到佣金

我有一千个好友，如果每个人一天吃一顿外卖20块，我拿5%

```1000*20*0.05 = 1000```

那就是一千啊！那我还上什么班，还给老板写什么代码？？？

想着，我又把鼠标给扔了

---

## 具体步骤
首先，注册好美团联盟和淘宝联盟（淘宝联盟就是饿了么联盟）
美团联盟：美团联盟

淘宝联盟： 阿里妈妈

首先在上面两个链接里注册号两个账号，美团联盟里拿到美团外卖的推广链接，淘宝联盟里拿到饿了么外卖的推广链接，

美团联盟要用企业信息去注册，也就是说你需要有一个公司

淘宝联盟用个人信息就可以



## 注册微信小程序
微信公众平台：微信公众平台

注册一个微信小程序，个人资质就可以，只需要一个邮箱号



## 开发
代码非常的简单，就是列表，列表里面是跳转链接，点哪领哪个券

小程序名：先领个券
具体功能可以用微信扫码看看



这里涉及到一个更新问题，因为更新小程序的代码是需要审核的，不可能每次你搞了一个新的优惠券上去就提交一次审核，这非常的不方便，所以我们需要一个方法来动态更新优惠券

一般来说要实现这个功能，我们需要一个服务器，一个数据库，然后修改数据库里的数据就可以做到动态修改优惠券列表了

但是！我觉得这太麻烦了，而且服务器租金是很贵的，我觉得不行，所以我用另个方法

那就是云开发



## 微信云开发
云开发文档：微信开放文档

开发者可以使用云开发开发微信小程序、小游戏，无需搭建服务器，即可使用云端能力。
云开发为开发者提供完整的原生云端支持和微信服务支持，弱化后端和运维概念，无需搭建服务器，使用平台提供的 API 进行核心业务开发，即可实现快速上线和迭代，同时这一能力，同开发者已经使用的云服务相互兼容，并不互斥。
简单的说就是用了这个就不需要去搞个服务器了

直接在微信开发者工具的可视化数据库里面添加就完事，简单的一批

既然文章是为了分享，我直接开源放出全部代码

https://github.com/hedongshu/miniapp-coupons.github.com

## 最后
上传审核完之后，就是推广你的小程序，我是加了好几个外卖红包的微信群，然后每天发一发，也没有非常上心

这是昨天一天的收益，差不多够吃一顿好的了

原则上我建议所有人都尝试自己部署, 因为代码确实比较简单, 看看微信小程序的开发文档就可以

如果你觉得这些代码还是太复杂了，那么你可以直接联系我v :`he1179601966` , 有问题我能尽量帮助, 也可以选择让我直接给你部署上线(有偿, 时间成本很高的)


## 常见问题

* 怎么获取饿了么和美团的推广链接
  
  美团联盟：https://union.meituan.com/

  饿了么、双十一：https://pub.alimama.com/

  饿了么聚合页CPS推广：https://market.m.taobao.com/app/qn/toutiao-new/index-pc.html#/detail/10628647/?_k=h8emzf

  去淘宝联盟开通淘宝客权限，可以直接调用api生成

  不想写代码的话可以用api测试工具生成推广链接：api测试工具




## 效果展示

![二维码](https://github.com/hedongshu/miniapp-coupons/blob/main/IMG_7327.JPG)
![展示](https://github.com/hedongshu/miniapp-coupons/blob/main/IMG_7326.PNG)






