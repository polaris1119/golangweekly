# Go语言爱好者周刊：第 143 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![母亲节](imgs/issue143/cover.png)

题图：填下母亲节日快乐！

## 刊首语

本期的题目，你能做对吗？以下代码输出什么？

```go
package main

import "fmt"

func main() {
	var a = 0.0
	const b = 0.0
	fmt.Println(a / b)
}
```

A：编译错误；B：Panic；C：NaN

## 资讯

1、[Go GUI 开发者调查结果](https://fynelabs.com/2022/05/03/go-gui-developer-survey-results/)

Fynelabs 出品。

2、[tinygo 0.23.0 发布](https://github.com/tinygo-org/tinygo/releases/tag/v0.23.0)

支持 Go1.18。

3、[go-mysql 1.5](https://github.com/go-mysql-org/go-mysql)

纯 Go 实现 MySQL 网络协议的库。

4、[Go 1.19 将支持 typed atomic value](https://github.com/golang/go/commit/ffe48e00adf3078944015186819a1ed5c6aa8bec)

这样就不需要 Uber 的 <https://github.com/uber-go/atomic> 了。

## 文章

1、[Golang中常用的代码优化点](https://mp.weixin.qq.com/s/QONfbKioFf6VqJE2OwP7Kw)

和大家分享一下我个人在开发过程中看到和使用到的一些常用的代码写法。

2、[开发常用的 10 个通用函数](https://mp.weixin.qq.com/s/tvy9L-pb_8WFWAmA9u-bMg)

以下是一些平时开发常用的通用函数，赶紧收藏起来，一定可以用得上。

3、[GoLand 中提高研发效率的5个使用技巧](https://mp.weixin.qq.com/s/N_4LTvJH1PNvD53PteDiQQ)

给大家介绍几个开发工具使用技巧，以提高研发效率。

4、[Go 单体服务开发最佳实践](https://mp.weixin.qq.com/s/yPeqr1Uin3YvNHBna_M1xA)

本文详细跟大家分享一下如何快速开发一个有多个模块的单体服务。

5、[教妹子学 Go 并发原语：啥是 Semaphore ？](https://mp.weixin.qq.com/s/mJOTKl6pZLxT4_4T-ZkghQ)

信号量是并发编程中常见的同步机制，在标准库的并发原语中使用频繁，比如 Mutex、WaitGroup 等，这些并发原语的实现都有信号量的影子，所以我们很有必要学好弄清楚信号量的实现原理。

## 开源项目

1、[generic](https://github.com/zyedidia/generic)

各种数据结构的 Go 泛型实现。

2、[arcticDB](https://github.com/polarsignals/arcticdb)

Go 实现的用于可观察性的数据库。

3、[logkit](https://github.com/qiniu/logkit/blob/master/READMECN.md)

七牛智能日志管理平台开发的一个配套的日志收集工具，支持海量的数据源，这是社区版。

## 资源&&工具

1、[使用 Go 生成 x86 汇编](https://github.com/WojciechMula/presentations/blob/main/avo-intro/avo-intro.pdf)

PDF（PPT） 文件下载。

2、[NeoAlgo](https://github.com/TesseractCoding/NeoAlgo/blob/master/Go/README.md)

Go 算法与数据结构。

3、[LeetCode-in-Go](https://github.com/aQuaYi/LeetCode-in-Go)

LeetCode 的 Go 解答。

4、[Go 播客第 227 期](https://changelog.com/gotime/227)

解析 Go 静态分析。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
