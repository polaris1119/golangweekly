# Go语言爱好者周刊：第 161 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue162/cover.png)

## 刊首语

大家国庆节快乐！国庆就不出题目了。

上期是一道关于 slice 的题目。正确率 40%。

以下代码输出什么？

```go
package main

import "fmt"

func main() {
    s := []string{"A", "B", "C"}

    t := s[:1]
    fmt.Println(&s[0] == &t[0])

    u := append(s[:1], s[2:]...)
    fmt.Println(&s[0] == &u[0])
}
```

A：false false；B：true false；C：true true；D：false true

正确答案：C。这里的关键点是 `append(s[:1], s[2:]...)` 会不会导致扩容。`s[:1]` 相当于 `s[:1:3]`，即容量是也是 3，因此 append 一个元素（`s[2:]...`）并不会导致扩容，因此第一个元素还是原来 s[0] 的元素。

## 资讯

1、[Conferences](https://github.com/golang/go/wiki/Conferences)

官方 Wiki 收集的 Go 各种会议和主要事件。

2、[micro v4.9 发布](https://github.com/go-micro/go-micro)

微服务框架。

3、[rqlite v7.7.0 发布](https://github.com/rqlite/rqlite)

基于 SQLite 分布式关系数据库。

4、[sarama v1.37 发布](https://github.com/Shopify/sarama)

Sarama 是 Apache Kafka 0.8 及更高版本的 Go 库。

5、[Ebiten 2.4.5 发布](https://github.com/hajimehoshi/ebiten)

简单的 2D 游戏库。

6、[gofumpt 0.4 发布](https://github.com/mvdan/gofumpt)

一个严格的 gofmt 工具。

## 文章

1、[Go语言之道：这么玄？](https://mp.weixin.qq.com/s/jAkSB6JvUmC9uS7bqtKV-g)

Go 之道。

2、[在Go中如何正确重试请求](https://mp.weixin.qq.com/s/XRjqEtcfCmvcgNpwhd93gg)

我们平时在开发中肯定避不开的一个问题是如何在不可靠的网络服务中实现可靠的网络通信，其中 http 请求重试是经常用的技术。

3、[Go 中使用 Cookie 的完整教程](https://www.alexedwards.net/blog/working-with-cookies-in-go)

建议动手试试。

4、[Go 开发人员最佳 VSCode 插件列表](https://mp.weixin.qq.com/s/o52N_rajZFKXciP712rHiw)

VSCode 目前是最流行的编辑器，没有之一。它的插件也很多，本文介绍 Go 开发人员的插件列表。

5、[如何用Go实现一个异步网络库？](https://mp.weixin.qq.com/s/_kVaNDxJzlIIqsmVU-kSGQ)

在需要高性能、节省资源的场景下，比如海量的连接、很高的并发，我们发现Go开始变得吃力，不但内存开销大，而且还会有频繁的goroutine调度。

6、[使用viper实现yaml配置文件的合并](https://mp.weixin.qq.com/s/JlmAeqLw7sW4F8Rkk5cpQQ)

作为小厂，我们的基础设施还不够完备，项目经理中秋节通知我们的系统近期要上second-to-last stage环境和生产环境，于是从运维人员部署效率方面考量，我们紧急开发了一个一键安装脚本生成工具。

7、[你写 Go 代码写注释吗？谈谈 Go 代码注释问题](https://mp.weixin.qq.com/s/5ZDzcGqenAvtOeSU-baV9A)

每隔一段时间，网上总会突然出现一些令人讨厌的帖子，其观点是：不应该为代码写注释，它存在的唯一原因是因为代码本身不足够好。对于这些论点，我完全不能苟同。

## 开源项目

1、[chrono](https://github.com/procyon-projects/chrono)

一个调度程序库，可以定期运行任务和代码。

2、[frpc](https://frpc.io/introduction)

一个快速、灵活的 RPC 框架。

3、[go-binarytree](https://github.com/dnaeon/go-binarytree)

简单的二叉树实现。

4、[gomek](https://github.com/joegasewicz/gomek)

一个小型的 HTTP 框架。

5、[flags](https://github.com/aneshas/flags)

标准库 flag 的替代者：增加 config 和 环境变量的支持。

## 资源&&工具

1、[go mod 鲜为人知的特性](https://verdverm.com/go-mods/)

看完会有新收获。（英文）

2、[gaze](https://github.com/wtetsu/gaze)

文件和目录的监控工具。

3、[GopherCon Europe 2022](https://www.youtube.com/watch?v=6qAfkJGWsns&t=180s)

Bill Kennedy 关于 Memory Profiling 的最佳实践。

4、[whattp](https://github.com/valxntine/whattp)

一个简单的脱机 CLI 工具，用于获取 HTTP 状态代码信息。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)