# News-Horizon
Make it easier for you to get useful information...

# Why ?
## Demand Analysis

**1**.随着互联网的飞速发展，信息化时代的到来，人们每天都受到海量互联网资讯的冲击，有些可能正符合人们对外界新鲜事的"摄取"需求，然而更多的是一些垃圾信息，只会浪费时间。

我们并非难以改变现状。问题的关键在于，如何使用户获得他们想要的资讯？

在此，我们强调 “选择权”的反转。

我们希望，用户能够自己选择需要的信息，只在必要的时候，向他们推送资讯。

**2**.阅读过的新闻，存在的价值大大降低；过多阅过的信息占据页面，总会降低体验。我们不希望它们占着有用的资讯版面的太多空间，怎么办？

我们选择让新闻 “阅后即焚”。

而相较于新闻，技术好文、新鲜视点 即使阅读过，它们的价值并不会因此降低太多，我们让用户能够保留自己喜欢文章，未收藏的，同样的“阅后即焚”。

遇到喜欢的文章忘了点收藏，新闻没看完不小心退出了？我们保留了最近的几篇被“焚”的文章，您可以在回收站找回它们。

# Aim

- [ ] 热点新闻的实时更新
- [ ] 用户可根据自己喜好点赞或收藏(技术文章)
- [ ] 根据用户的足迹和喜好, 推荐资讯
- [ ] 用户也可撰写文章（单独一个板块[被踩过多则会折叠]）
- [ ] 阅后即焚 与 回收站

# How to achieve

## 如何实现实时更新？

1.后台爬虫定时自动重爬 <br>
2.管理员点击"获取最新资讯",启动爬虫爬取 <br>
3.用户下拉新闻列表进行刷新 <br>

## 如何推断用户的喜好？

0.用户注册成功时, 让用户选择自己喜爱的分类标签(根据此选择进行初始推荐) <br>
1.将不同的文章分类, 一篇文章可以属于多个分类 <br>
2.记录用户的点击情况, 点击一篇文章, 文章相应的分类的权重 +1 <br>
3.当用户点击收藏时, 相应的分类的权重 +n <br>
4.当用户点击 "踩" 时, 相应的文章的分类的权重 -2 <br>
 
## 如何根据用户的喜好推荐相关内容？

## 如何实现"阅后即焚"？

# Tech-Stack
 - Dva (React-Redux-Saga)
 - Express
 - Scrapy
 - MongoDB

# LICENSE
 FROM [MIT](https://tldrlegal.com/license/mit-license)
