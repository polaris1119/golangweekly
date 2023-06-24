# Go语言爱好者周刊：第 191 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue191/cover.jpeg)

题图：父亲节快乐！！！

## 资讯

1、[gocv v0.33.0 发布](https://github.com/hybridgroup/gocv)

使用 OpenCV 4+ 的计算机视觉包。

2、[gocryptfs v2.4 发布](https://github.com/rfjakob/gocryptfs)

Go 编写的加密 overlay 文件系统。官方网站：https://nuetzlich.net/gocryptfs

3、[bloom v3.5 发布](https://github.com/bits-and-blooms/bloom)

Go 的 Bloom filters 实现。

4、[mockery v2.29 发布](https://github.com/vektra/mockery)

提供了轻松为 Go 接口生成 mock 的功能。它删除了使用 mock 所需的样板代码。

5、[certmagic v0.18 发布](https://github.com/caddyserver/certmagic)

为任意 Go 程序自动加上 HTTPS，Caddy 使用的一个库。

6、[gdu v5.25 发布](https://github.com/dundee/gdu)

带控制台接口的磁盘使用分析器。

## 文章

1、[Go 1.21.0 带来了什么新特性？min 和 max 内置函数解析](https://mp.weixin.qq.com/s/VRASxwbNbz4ZvpPspXTdww)

Go 1.21.0 是 Go 语言的最新版本，它将在 2023 年 8 月发布，会带来了一些语言和工具的变化。其中一个值得关注的变化是增加了两个新的内置函数 min 和 max，用来对任意可比较类型进行最小值和最大值的操作。

2、[Go协程池(1): 线程vs协程](https://mp.weixin.qq.com/s/rgecHCCgBEpSC3lOQMn9Lg)

Goroutine(也叫协程)运行在用户态，由Go runtime管理。而操作系统线程同时处于用户态和内核态。

3、[写给go开发者的gRPC教程-错误处理](https://mp.weixin.qq.com/s/ghJiTvJxYzLKTFs5gZga5w)

系列教程。

4、[Go语言反射编程指南](https://mp.weixin.qq.com/s/9OjvKLEei9HjmGcsA4fq7w)

反射是一种编程语言的高级特性，它允许程序在运行时检视自身的结构和行为。

5、[Gin 框架是如何处理 panic 的？](https://mp.weixin.qq.com/s/dUqK0-1RYtZTadHWf0s3sw)

本文我们介绍下recover在gin框架中的应用。

6、[Go GC：了解便利背后的开销](https://tonybai.com/2023/06/13/understand-go-gc-overhead-behind-the-convenience/)

Go语言的垃圾回收机制（Garbage Collection，简称 GC）是其重要的运行机制之一，它可以帮助开发人员避免手动管理内存的复杂性和错误，为开发者带来开发上的便利，使开发者可以更专注于业务逻辑的实现。然而，GC的便利性背后也带来了一定的系统开销，作为成熟的Go开发者，我们需要了解GC带来的开销和优化方法，以帮助我们更好的了解和使用Go语言。

7、[从源码分析 Go 语言使用 cgo 导致的线程增长](https://www.cnblogs.com/t102011/p/17457120.html)

TDengine Go 连接器 https://github.com/taosdata/driver-go，使用 cgo 调用 taos.so 中的 API，使用过程中发现线程数不断增长，本文从一个 cgo 调用开始解析 Go 源码，分析造成线程增长的原因。

## 开源项目

1、[geziyor](https://github.com/geziyor/geziyor)

一个快速的网络爬虫框架。

2、[rapid](https://github.com/flyingmutant/rapid)

一个现代的基于属性的测试库。

3、[spectagular](https://github.com/matt1484/spectagular)

结构体标签解析。

## 资源&&工具

1、[gotestsum](https://github.com/gotestyourself/gotestsum)

一个 ’go test’ 的运行器，它可以输出适合人类阅读的格式，也可以输出 JUnit XML 格式用于 CI 集成，还可以输出测试结果的摘要。它既适合本地开发，也适合自动化测试。

2、[fractals](https://github.com/joweich/fractals)

一个使用 goroutines 的快速曼德博集合渲染器。

3、[go-websocket-benchmark](https://github.com/lesismal/go-websocket-benchmark)

Golang Websocket 百万连接测试。作者自荐，<https://github.com/polaris1119/golangweekly/issues/103>。

4、[SolidUI](https://github.com/CloudOrc/SolidUI)（作者自荐），非 Go 项目

AI生成可视化原型设计和编辑平台，支持2D，3D模型，结合LLM(Large Language Model) 快速编辑。

5、[tc-filter](https://github.com/JamesYYang/tc-filter)（作者自荐）

一个基于ebpf tc实现的linux网络包过滤器。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
