# Go语言爱好者周刊：第 170 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue170/cover.jpeg)

题图：Gopher 图片集

## 刊首语

本期是一道关于 math 包的 Inf 的题目。以下代码输出什么？

```go
package main

import (
    "fmt"
    "math"
)

func main() {
    // Inf returns positive infinity if sign >= 0, negative infinity if sign < 0.
    x := math.Inf(1)
    switch {
    case x < 0, x > 0:
        fmt.Println(x)
    case x == 0:
        fmt.Println("zero")
    default:
        fmt.Println("something else")
    }
}
```

A：+Inf； B：zero； C：something else； D：doesn't compile

## 资讯

1、[1.20 将支持 Wrap 多个错误](https://github.com/golang/go/issues/53435)

一起的还有 Unwrap 的支持。

2、[HN 热议](https://news.ycombinator.com/item?id=33757306)

你喜欢或不喜欢 Go 什么？

3、[listmonk 2.3 发布](https://github.com/knadh/listmonk)

具有现代仪表板的高性能，自托管通讯和邮寄列表管理器。Go + Vue 构建。

4、[miller 6.5 发布](https://github.com/johnkerl/miller)

文本数据处理的瑞士军刀，Go 实现。

5、[zap 1.24 发布](https://github.com/uber-go/zap)

Uber 出品的日志库。

6、[fibratus 1.8 发布](https://github.com/rabbitstack/fibratus)

Windows 内核勘探和追踪的现代工具。

7、[FastHTTP 1.43 发布](https://github.com/valyala/fasthttp)

Go 快速的 HTTP 包。为高性能而调优。 热路径中的零内存分配。 比 net/http 快 10 倍。有兴趣可以研究为什么能做到快这么多。

## 文章

1、[快收藏！最全Go语言实现设计模式（下）](https://mp.weixin.qq.com/s/-VOPPLP48b0NOdysjNs4ZA)

本文继续列出Go语言实现的经典设计模式示例，每个示例都精心设计，力求符合模式结构，可作为日常编码参考，同时一些常用的设计模式融入了开发实践经验总结，帮助大家在平时工作中灵活运用。

2、[用 Go 语言，如何编写一个能玩的国际象棋引擎？](https://mp.weixin.qq.com/s/yohyILv2d9-qrhqtoM5gvQ)

2016 年，AlphaGo 一连战胜多位人类职业围棋选 手，从此一炮而红，各种下棋机器人近几年也层出不穷。那么，你是否想过要自己做一个呢？

3、[盘点那些 Go 的最佳应用场景](https://mp.weixin.qq.com/s/fRfpBTWt4dwqfQJ0cWizIA)

如果你想知道什么样的应用程序可以使用 Golang，请按照本文了解 Golang 开发的最佳场景。

4、[Go 服务自动收集线上问题现场](https://mp.weixin.qq.com/s/vB9ElJCfgZeQHtB596XHpA)

对于 `pprof`，相信熟悉 Go 语言的程序员基本都不陌生，一般线上的问题都是靠它可以快速定位。但是实际项目中，很多时候我们为了性能都不会开启它，但是出了问题又要靠它来分析。

5、[从鹅厂实例出发！分析Go Channel底层原理](https://mp.weixin.qq.com/s/nQ2SxT8dtRWjbDQccBaY1Q)

本文是基于 Go1.18.1源码的学习笔记。

6、[GoLand 迎来五周年，同时发布 2022.3：有彩蛋](https://mp.weixin.qq.com/s/IvL24_7iuuRp9Y3dljHaHQ)

GoLand 2022.3 是 2022 系列的最后一个版本，提供了性能增强以及针对泛型和 Go 工作区的新功能。

## 开源项目

1、[ecoji](https://github.com/keith-turner/ecoji)

将数据编码（和解码）为表情符号。

2、[casnode](https://github.com/casbin/casnode)

Go 和 React 驱动的论坛系统。

## 资源&&工具

1、[otto](https://github.com/robertkrimen/otto)

一个 JavaScript 解释器。

2、[skeema](https://github.com/skeema/skeema)

MySQL/MariaDB 的声明式纯 SQL 模式管理。

3、[semver](https://github.com/Masterminds/semver)

分析、排序和检查语义版本号。

4、[free-gophers-pack](https://github.com/MariaLetta/free-gophers-pack)

Gopher 图片合集。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
