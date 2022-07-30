# Go语言爱好者周刊：第 153 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue153/cover.png)

题图：gum

## 刊首语

上期的题目比较简单，正确率也比较高。一起看看。

以下代码输出什么？

```go
package main

import "fmt"

func main() {
	const c = 8
	a := &c
	*a = 12
	fmt.Println(*a)
}
```

A：8；B：不能编译；C：12

正确答案：B。报的错是：`invalid operation: cannot take address of c (untyped int constant 8)`。

看下本期题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	a := []int{7, 8, 9}
	fmt.Println(a[real(2)])
}
```

A：0；B：7；C：9；D：不能编译

## 资讯

1、[sqlite 1.18.0 发布](https://gitlab.com/cznic/sqlite)

一个自包含，无服务器，零配置的事务型 SQL 数据库引擎的进程内实现。

2、[Go Micro 4.8 发布](https://github.com/asim/go-micro)

分布式系统框架。

3、[sonic 1.3.4 发布](https://github.com/bytedance/sonic)

字节开源的高性能 json 编解码库。

4、[bud 0.2.3 发布](https://github.com/livebud/bud)

一个全栈框架。

5、[chromedp 0.8.3 发布](https://github.com/chromedp/chromedp)

驱动浏览器的 Go 语言库，支持 Chrome DevTools 协议。抓取动态网页利器。

6、[milvus 2.1 发布](https://github.com/milvus-io/milvus)

一个开放源码的矢量数据库，用于嵌入相似性搜索和人工智能应用程序。

7、[Buf 1.7 发布](https://github.com/bufbuild/buf)

一种新的 Protobuf 处理库。

8、[fq 0.0.8 发布](https://github.com/wader/fq)

用于检查二进制数据的工具、语言和解码器，类似 jq。

9、[imgproxy 3.7 发布](https://github.com/imgproxy/imgproxy)

一个 Go 语言写的图片代理网关，可以代理远程图片，并且提供格式转换和大小缩放功能。

## 文章

1、[Go 新版内存模型](https://tip.golang.org/ref/mem)

Go 1.19 的这个改变是去年由 Russ Cox [在一篇文章](https://research.swtch.com/gomm)中首次提出的，对 Go 内存模型的一些修改，使其与其他语言（例如C、C++ 和 Rust）更为一致，以及 sync/atomic 包中的一些新类型。

2、[GoLand 2022.2 正式发布](https://mp.weixin.qq.com/s/aIdPtX2M4CNs-boHh4nORQ)

为**泛型**和 `go.work` 提供了更好、全面的支持，同时还添加了对**模糊测试**的支持。

3、[Go每日一库之一个好玩的 Go 语言 REPL 工具](https://mp.weixin.qq.com/s/RXoDet9_W2l4TZzw4F96zQ)

一个很好玩的 Go 语言的 REPL（read-eval-print-loop）工具。

4、[带你彻底击溃跳表原理及其Golang实现！（内含图解）](https://mp.weixin.qq.com/s/XEIrp1oTsBYDCv3b-m_11g)

本文是基于我个人对跳表原理的深入探究，并通过golang实现了一个基础跳表的理解和实践。

5、[Golang DES 加解密如何实现？](https://mp.weixin.qq.com/s/yxK6y3EirIzafS4l9LnLfQ)

本文介绍了 DES 加密原理和作用，和 golang 中 DES 加密解密机制的相应实现。

6、[3万字长文手把手带你从0搭建一个Go ORM框架！](https://mp.weixin.qq.com/s/fk__wCp-r60FJwYPkZpmFQ)

本文主要从基础原理开始介绍，到一步一步步骤实现，继而完成整个简单且优雅的MySQL ORM。

7、[如何使用 Elastic APM Go 代理为 Go 应用装载测量工具](https://mp.weixin.qq.com/s/tB8glQ0hxrj-QpweI4HUDw)

在本文中，我们将研究如何使用 Elastic APM 为 Go 应用程序装载测量工具，以便捕获详细的响应时间性能数据（跟踪）、捕获基础架构和应用程序指标，以及与日志集成 — 实现可观察性三要素。

8、[掌握了这一招，Go版本的管理不用愁](https://mp.weixin.qq.com/s/OGNetZZW7aTr8s6BlW-KIw)

今天带来一篇关于Go版本管理器 gvm 的小短文。

## 开源项目

1、[hlive](https://github.com/SamHennessy/hlive)

HLive 是一个基于服务器端 WebSocket 的动态无模板视图层。

2、[gin-rate-limit](https://github.com/JGLTechnologies/gin-rate-limit)

Gin 框架的 rate limit。

3、[drafts](https://github.com/rafaeldtinoco/drafts)

Go 开发 ebpf 程序的应用骨架。

## 资源&&工具

1、[speedbump](https://github.com/kffl/speedbump)

用于模拟可变网络延迟的 TCP 代理。

2、[gobackup](https://github.com/huacnlee/gobackup)

用于将数据库、文件备份到 FTP/SCP/S3 存储的简单工具。

3、[Go Time 第 240 期](https://changelog.com/gotime/240)

Go1.19 包含哪些新特性？

4、[gum](https://github.com/charmbracelet/gum)

一款用于制作迷人 shell 脚本的工具。

5、[litefs](https://github.com/superfly/litefs)

Go 实现的 sqlite 复制工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
