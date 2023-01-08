# Go语言爱好者周刊：第 173 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue173/cover.png)

题图：晚上学习 Golang

## 资讯

1、[vscode-go 0.37.0 发布](https://github.com/golang/vscode-go/releases/tag/v0.37.0)

可报告你的依赖项中的已知漏洞，基于官方的这个数据库：<https://go.dev/security/vuln/>。

2、[wish 1.0 发布](https://github.com/charmbracelet/wish)

让在 Go 中构建基于 SSH 的应用变得更容易。

3、[gopher-lua 1.0 发布](https://github.com/yuin/gopher-lua)

一个 Go 实现的  Lua  VM 和编译器。

4、[graphql-go 1.5.0](https://github.com/graph-gophers/graphql-go)

注重易用性的 GraphQL 服务器。

5、[fyne 2.3.0 发布](https://github.com/fyne-io/fyne)

基于 Material Design 的 Go 跨平台 GUI。

6、[miller 6.6 发布](https://github.com/johnkerl/miller)

文本数据处理的瑞士军刀，Go 实现。

7、[FerretDB v0.8.0](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。

8、[progressbar 3.13 发布](https://github.com/schollz/progressbar)

线程安全的 process bar。

9、[fiber 2.41.0 发布](https://github.com/gofiber/fiber/releases/tag/v2.34.0)

一种 Express 风格的、基于 fasthttp 的 HTTP web 框架。

10、[fq 0.2 发布](https://github.com/wader/fq)

类似 jq，但用于二进制文件。

## 文章

1、[2022 年 Go 语言盘点](https://mp.weixin.qq.com/s/VrfqAB4LKCaPpQ1djgN5cg)

泛型落地，无趣很好，稳定为王。

2、[详解全网最快 Go 泛型跳表](https://mp.weixin.qq.com/s/lgHVrhZ5GVJ65FrQDsRgow)

一套类似 C++ 中 STL 的容器和算法库。其中有序的 Map 用跳表实现，并优化到极致性能。

3、[Go1.20 RC2 发布：正式版快要来了](https://mp.weixin.qq.com/s/V9MqbVFSQqkMdEthuEcKdQ)

Go 1.20 正式版本预计将于 2023 年 2 月份发布。

4、[最全Go select底层原理，一文学透高频用法](https://mp.weixin.qq.com/s/n-2T7Bzj-Yr5Pfz6ns5gHg)

本文基于 Go1.18.1 版本的源码，讲解 select 访问 Channel 在编译期和运行时的底层原理。

5、[Go BIO/NIO探讨(1)：Gin框架中如何处理HTTP请求](https://mp.weixin.qq.com/s/VjP9Bv46x7NP6uQ7cbsqmg)

最近看到字节跳动开源了 Go 语言的 Hertz，声称使用了 Non-blocking IO 网络库 Netpoll，所以性能非常强大。

## 开源项目

1、[conc](https://github.com/sourcegraph/conc)

结构更佳的 Go 并发库。

2、[pushup](https://github.com/adhocteam/pushup)

用于在 Go 中开发面向页面的现代 Web 框架。

3、[go-sstables](https://github.com/thomasjungblut/go-sstables)

排序字符串表(sst)的 Go 实现。

4、[goal](https://codeberg.org/anaseto/goal)

Go 实现的嵌入脚本数组编程语言。

## 资源&&工具

1、[passit](https://tomthorogood.net/writing/announcing-passit/)

一个设计精良的 Go 密码生成工具包。

2、[slashbase](https://github.com/slashbaseide/slashbase)

一个 Go 实现的运行于浏览器内的数据库 IDE 和 CLI，支持 PostgreSQL 和 MongoDB。

3、[GopherCon 2022 大会演讲视频全集](https://www.youtube.com/playlist?list=PL2ntRZ1ySWBfiSJSt-zPRbVSMDfK0EwQC)

YouTube 视频。

4、[coroot](https://github.com/coroot/coroot)

微服务架构的监控与诊断工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
