# Go语言爱好者周刊：第 188 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue188/cover.jpeg)

题图：golangweekly

## 资讯

1、[增强 http.ServeMux 路由](https://github.com/golang/go/discussions/60227)

这是一个讨论，你支持吗？

2、[FerretDB v1.2.0 发布](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。

3、[vhs v0.5.0 发布](https://github.com/charmbracelet/vhs)

CLI 屏幕录制工具。

4、[roaring v1.3 发布](https://github.com/RoaringBitmap/roaring)

位图数据结构的 Go 实现。

5、[lancet v2.2 发布](https://github.com/duke-git/lancet)

一个全面、高效、可复用的 Go 语言工具函数库。

6、[buf v1.19 发布](https://github.com/bufbuild/buf)

一种新的 Protobuf 处理库。

## 文章

1、[Go 官方 23 年 Q1 调查报告：你关心的都在这里](https://mp.weixin.qq.com/s/8Lez8I2K4F81V9wm8CvEhw)

Go 官方博客发布了 2023 年第一季度 Go 开发者调查报告。

2、[Zap 日志库综合指南](https://betterstack.com/community/guides/logging/go/zap/)

由 Uber 开发并专为 Go 应用程序设计的结构化日志记录包。

3、[Go 空结构体：零内存的魔力](https://mp.weixin.qq.com/s/Jy2wxqZYNMpQe7s1jtIR1g)

在 Go 语言中，有一种特殊的用法可能让许多人感到困惑，那就是空结构体 struct{}。在本文中，我将对 Go 空结构体进行详解，准备好了吗？准备一杯你最喜欢的饮料或茶，随着本文一探究竟吧。

4、[GoLand官博：为什么不用Go开发操作系统？](https://mp.weixin.qq.com/s/IzWFop2a2hdDBGbCzFuUjg)

本文整理自 GoLand 官方博客的一篇文章：《OS in Go? Why Not?》，探讨了为什么像 C 这样的编程语言在 OS 开发中占据优势，以及是否可以使用 Go 编写 OS。

5、[Go1.22 可能会解决循环变量的问题，你支持吗？](https://mp.weixin.qq.com/s/N7_-WNBsTpTc4X8qTQw-Nw)

Go 语言也不是完美的，它有一些设计上的缺陷或者不足，其中之一就是循环变量作用域问题。

6、[XML 处理，Go 标准库太简单了怎么办？](https://mp.weixin.qq.com/s/Neuc_hiVsVE83d47e40l6w)

今天介绍一个基于官方 xml 库的增强库：etree，它是一个轻量级的纯 Go 包，它可以用于以元素树的形式表示 XML 文档。

## 开源项目

1、[gopy](https://github.com/go-python/gopy)

将 Go 语言的包编译成 Python 模块，从而在 Python 应用中使用 Go 语言的功能。

2、[gain](https://github.com/pawelgaczynski/gain)

一个高性能的 io_uring 网络框架。

3、[dnscontrol](https://github.com/StackExchange/dnscontrol)

一个用于维护 DNS 区域的系统。

4、[openfga](https://github.com/openfga/openfga)

一个高性能和灵活的授权/权限引擎。

## 资源&&工具

1、[gitleaks](https://github.com/gitleaks/gitleaks)

保护密钥。

2、[snips.sh](https://github.com/robherley/snips.sh)

一个基于 SSH 的无密码、匿名的 pastebin 服务，可以用来分享代码片段、文本文件或命令输出。

3、[go-datastructures](https://github.com/Workiva/go-datastructures)

高性能的和线程安全的 Go 数据结构的集合。

4、[neotest](https://github.com/nvim-neotest/neotest)

用于与 NeoVim 中的测试交互的可扩展框架。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
