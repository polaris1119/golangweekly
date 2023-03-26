# Go语言爱好者周刊：第 182 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue182/cover.jpeg)

题图：Go 项目布局

## 资讯

1、[Ebitengine 2.5 发布](https://ebitengine.org/en/documents/2.5.html)

2D 的游戏引擎。

2、[participle 2.0 发布](https://github.com/alecthomas/participle)

Go 的解析库。

3、[v8go 0.9.0 发布](https://github.com/rogchap/v8go)

在 Go 中执行 JavaScript。

4、[chroma 2.7 发布](https://github.com/alecthomas/chroma)

纯 Go 实现的通用语法高亮库。

5、[listmonk 2.4 发布](https://github.com/knadh/listmonk)

具有现代仪表板的高性能，自托管通讯和邮寄列表管理器。Go + Vue 构建。

6、[micro v4.10 发布](https://github.com/go-micro/go-micro)

微服务框架。

7、[Gitea 1.19 发布](https://blog.gitea.io/2019/07/gitea-1.9.0-is-released/) 

Gitea 是一个开源社区驱动的轻量级代码托管解决方案，后端采用 [Go](https://golang.org/) 编写，采用 [MIT](https://github.com/go-gitea/gitea/blob/master/LICENSE) 许可证。

8、[wish 1.1 发布](https://github.com/charmbracelet/wish)

让在 Go 中构建基于 SSH 的应用变得更容易。

9、[log 0.2](https://github.com/charmbracelet/log)

一个小巧、色彩丰富的 Go 日志库。

## 文章

1、[Go每日一库之Pie ：一个高性能、类型安全的slice操作库](https://mp.weixin.qq.com/s/vdVZYEy5LznQSHI6klaCIg)

在Go语言中，对slice和map是我们最常用的数据结构。比如，计算两个切片的交集、差集；判断切片中的元素是否都满足某个条件的等。我推荐大家使用这个包。

2、[Go是一门面向对象编程语言吗](https://mp.weixin.qq.com/s/anZrAc7Ir4QoUeID919VxQ)

很多人第一次接触Go，他们中的很多是来自像Java, Ruby这样的OO(面向对象)语言阵营的，他们学习Go之后的第一个问题便是：Go是一门OO语言吗？在这篇博文中，我们就来探讨一下。

3、[聊聊Go语言的全局变量](https://tonybai.com/2023/03/22/global-variable-in-go/)

C语言是Go语言的先祖之一，Go继承了很多C语言的语法与表达方式，这其中就包含了全局变量，虽然Go在其语法规范中并没有直接给出全局变量的定义。

4、[唯一的、必须的、永恒的 Go 项目布局](https://appliedgo.com/blog/go-project-layout)

是否有借鉴作用？

## 开源项目

1、[go-openai](https://github.com/sashabaranov/go-openai)

OpenAI 的 Golang SDK，包括 ChatGPT、GPT-3、GPT-4 等。

2、[sse](https://github.com/r3labs/sse)

服务器事件发送服务端和客户端。

3、[go-nostr](https://github.com/nbd-wtf/go-nostr)

nostr 协议的 Go 实现。

4、[dynamicgo](https://github.com/cloudwego/dynamicgo)

基于原始字节流的高性能+动态化 Go 数据处理。

## 资源&&工具

1、[betteralign](https://github.com/dkorunic/betteralign)

一个检测结构体是否可以占用更少内存的工具。

2、[hot-reload](https://github.com/dkfbasel/hot-reload)

基于 Docker 的热重载开发。

3、[go-testdeep](https://github.com/maxatome/go-testdeep)

极度灵活的 golang 深度对比，扩展 go 测试包，测试 HTTP APIs，提供测试套件.

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
