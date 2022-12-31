# Go语言爱好者周刊：第 172 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue172/cover.jpeg)

题图：2023 元旦快乐

## 刊首语

停更了两期，这次赶在 2022 年最后一天更新下。大家 2023 年元旦快乐！

## 资讯

1、[提案：slices 将加入标准库](https://github.com/golang/go/issues/57433)

具体会在 Go1.21，终于要加入了。

2、[Go 中可以使用 Chat API？](https://altafino.com/blog/how-to-use-the-openai-chat-api-in-golang/)

具体库：<https://github.com/openai/go-openai>。

3、[用爱发电太难：招募不到维护者，Go流行的Web工具包归档了](https://mp.weixin.qq.com/s/5tfAHD3lYbktJ6Cy93CpCw)

流行的开源 Go 语言 Web 工具包 Gorilla 宣布已正式归档。

## 文章

1、[一起用Go做一个小游戏（上）](https://mp.weixin.qq.com/s/5HfZ2TrnUl2pfBft5-CAJg)

一共三篇，另两篇：

- [一起用Go做一个小游戏（中）：飞机大战](https://mp.weixin.qq.com/s/UXpekTlUcK6nxKOYGZfP2A)

- [一起用Go做一个小游戏（下）](https://mp.weixin.qq.com/s/Hw2GFSTY9Sgv2SPgYypreQ)

2、[一文彻底理解Go语言栈内存/堆内存](https://mp.weixin.qq.com/s/QQjOyYkDfuxIxHl6k6qkRA)

本文将从6个方向层层递进，帮助大家彻底理解Go语言的栈内存和堆内存。

3、[微服务税和更简单的 grpc mock](https://mp.weixin.qq.com/s/FB2hLqoJojdP7UXQfaV9jA)

现在稍微有一点规模的公司基本都上微服务了，后端工程师在大小公司打杂的话都会碰到因为是微服务。

4、[Go为什么能成功？](https://mp.weixin.qq.com/s/02Dtj94yOjy2WTLko-5JXQ)

你觉得是什么原因？

5、[Go 程序打成 rpm 包，也太简单了](https://mp.weixin.qq.com/s/TjqeSK9PNCkJAdeik2U_wA)

收藏以备不时之需。

6、[有趣的 Go HttpClient 超时机制](https://mp.weixin.qq.com/s/SA2Me6QGkzxLAfhmQ0eWmA)

我是既写 Java 又写 Go 的小楼，在写 Go 的过程中我经常对比这两种语言的特性，踩了不少坑，也发现了不少有意思的地方，今天就来聊聊 Go 自带的 HttpClient 的超时机制。

7、[官方试验日志库 slog](https://thedevelopercafe.com/articles/logging-in-go-with-slog-a7bb489755c2)

试用教程。

8、[为什么我们用 Go 开发一切](https://bitly.com/blog/why-we-write-everything-in-go/)

国外的一篇文章。

9、[Go：讲一个故事说明使用汇编语言的必要性](https://mp.weixin.qq.com/s/2_xALNnPcHgZD7smWxzPcA)

配合 ChatGPT 写成的文章。

## 开源项目

1、[go-sstables](https://github.com/thomasjungblut/go-sstables)

排序字符串表 (sst) 的 Go 实现。

2、[goal](https://codeberg.org/anaseto/goal)

Go 实现的嵌入脚本数组编程语言。

3、[d2](https://github.com/terrastruct/d2)

使用 Go 实现的图表脚本语言，可以将文本转换为图表。

4、[answer](https://github.com/answerdev/answer)

用 Go 构建知识问答社区。

5、[go-captcha](https://github.com/wenlng/go-captcha)

行为验证码生成库。

6、[plugo](https://github.com/curzodo/plugo)

Go 插件库。

## 资源&&工具

1、[Golang 1.19 标准库可视化](https://nicetomap.com/golang-1.19-standard-library)

类似思维导图。

2、[coroot](https://github.com/coroot/coroot)

微服务架构的监控与诊断工具。

3、[gobackup](https://github.com/gobackup/gobackup)

数据备份领域的“瑞士军刀”。

4、[steampipe](https://github.com/turbot/steampipe)

一个基于 Go 的用于API查询的 SQL 控制台。

5、[gokey](https://github.com/cloudflare/gokey)

Go 实现的一个简单的 vaultless 密码管理器。

6、[Go Generics cheatsheet](https://gosamples.dev/generics-cheatsheet/)

泛型速查表。

7、[开源的图解算法](https://www.hello-algo.com/)

还是基于各种常见语言的实现。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
