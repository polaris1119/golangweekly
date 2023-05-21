# Go语言爱好者周刊：第 187 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue187/cover.jpeg)

题图：Go 2023 Q1 调查结果

## 资讯

1、[gobot v2.0 发布](https://github.com/hybridgroup/gobot)

使用 Go 编程语言的 IOT 框架（机器人框架）。

2、[Mage v1.15 发布](https://github.com/magefile/mage)

Mage 是使用 Go 的类似 make/rake 的构建工具。您编写普通的 go 函数，Mage 会自动将它们用作类似于 Makefile 的可运行目标。

3、[Stackoverflow 2023 用户调查开启](https://stackoverflow.blog/2023/05/08/the-2023-developer-survey-is-now-live/)

Go 爱好者可以为 Go 参与调查。

4、[Go 官方 2023 Q1 调查结果](https://go.dev/blog/survey2023-q1-results)

果然泛型不是讨论的焦点。

## 文章

1、[使用增强版 singleflight 合并事件推送，效果炸裂！](https://mp.weixin.qq.com/s/KUkzHS4Yfad3l_CnU49lLg)

最近在工作中对 Go 的 singleflight 包做了下增强，解决了一个性能问题，这里记录下，希望对你也有所帮助。

2、[从一次 PR 经历谈谈 Go 和 MySQL 的时区问题](https://mp.weixin.qq.com/s/ohpshzrYkERbpioPfb-CvA)

你有遇到吗？

3、[使用Go实现traceroute工具](https://colobu.com/2023/05/03/write-the-traceroute-tool-in-Go/)

traceroute 是一种用于诊断网络连接问题的实用程序，它可以确定两台计算机之间的网络路径和网络时延。

4、[几种使用Go发送IP包的方法](https://colobu.com/2023/05/13/send-IP-packets-in-Go/)

本文尝试介绍几种收发IP packet的方式。

## 开源项目

1、[dinero.go](https://github.com/DustinJSilk/dinero.go)

这是一个将 dinero.js 移植到 Go 语言的库。dinero.js 是一个用于创建、计算和格式化货币值的 JavaScript 库，它提供了一些方便的方法来处理不同的货币和精度。

2、[barf](https://github.com/opensaucerer/barf)

一个构建 RESTful API 的框架。

3、[lingoose](https://github.com/henomis/lingoose)

一个 Go 框架，用于使用管道开发基于 LLM 的应用程序。

## 资源&&工具

1、[bodyclose](https://github.com/timakin/bodyclose)

检查 http Response.Body 是否关闭的 linter。

2、[wzprof](https://github.com/stealthrocket/wzprof)

一个基于 [Wazero](https://github.com/tetratelabs/wazero) 的 WebAssembly 的性能分析工具，它可以收集 CPU 和 内存 的使用情况，并生成与 pprof 兼容的分析报告。

3、[faktory](https://github.com/contribsys/faktory)

这是一个语言无关的持久化后台任务服务器。它可以用于将后台任务分发到一个或多个机器上，并提供了一个简单的 API 来推送和获取任务。

4、[vale](https://github.com/errata-ai/vale)

这是一个语法感知的文本校对工具，它可以用于检查文本的拼写、风格和语法错误，并提供了快速和可扩展的特性。

5、[mods](https://github.com/charmbracelet/mods)

命令行中的 AI。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
