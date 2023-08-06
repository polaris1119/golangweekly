# Go语言爱好者周刊：第 197 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue197/cover.jpeg)

题图：go env

## 资讯

1、[Go 开发者调查开始](https://google.qualtrics.com/jfe/form/SV_4Vi4bNaMQhQdqSi?s=b)

官方的调查。

2、[goread v1.5 发布](https://github.com/TypicalAM/goread)

一个漂亮的可以在终端中阅读你的 RSS 提要！

3、[提案：database/sql 增加新的 scan](https://github.com/golang/go/issues/61637)

这个 Scan 即将整行扫描为一个值的方法。

4、[ntp v1.3 发布](https://github.com/beevik/ntp)

用于查询你选择的网络时间协议服务器的当前时间。

5、[ElasticSearch Go 8.9 发布](https://github.com/elastic/go-elasticsearch)

ElasticSearch Go 8.7 官方客户端发布。

6、[ff v3.4 发布](https://github.com/peterbourgon/ff)

该库对 flag.FlagSet 进行了扩展，支持按照命令行、配置文件、环境变量的顺序进行读取。这次的更新，支持从 yaml 配置格式读取配置。

## 文章

1、[GoLand 2023.2 发布：有 AI 助手](https://mp.weixin.qq.com/s/cidtQEAfuFWuYveKFbFvKQ)

改进了与 Go 模块的集成，添加了用于将函数参数迁移到方法接收器（反之亦然）的重构，提供了 Kafka 监控插件，并支持 error.Is 和 error.As，还有“新的 AI 助手插件”，因为毕竟是 2023 年了。

2、[得到友好的 CPU 缓存](https://www.ardanlabs.com/blog/2023/07/getting-friendly-with-cpu-caches.html)

帮助 Go 开发者理解 CPU 缓存的原理和重要性，以及如何利用它们来提升程序的性能和质量。

3、[抽丝剥茧，记一次 Go 程序性能优化之旅](https://mp.weixin.qq.com/s/Wj4Vr0W-cl79Ss5VVSDr_w)

可以看看。

4、[Go 语言 iota 的神奇力量](https://mp.weixin.qq.com/s/Hq_jF5LdaM5bOwDlLCw7uA)

本文将带着大家深入探讨 iota 的神奇力量，包括 iota 的介绍和应用场景以及使用技巧和注意事项。

5、[Go 项目分层下的最佳 error 处理方式](https://mp.weixin.qq.com/s/FkqCidcHlH2cadtsSft-ig)

本文将探讨 Go 项目分层下的最佳 error 处理方式。准备好了吗？准备一杯你最喜欢的饮料或茶，随着本文一探究竟吧。

6、[Go 每日一库之比标准库更快 hash 算法](https://mp.weixin.qq.com/s/QEBdspMhEBcCwgHouS9cKQ)

该库是 go 语言实现的 xxHash 算法，比标准库性能更高，最终生成一个 64 位的整型 hash 值。

7、[Go 语言的安全守护者](https://mp.weixin.qq.com/s/bYob9smOpmTZyrxBeIAEVg)

为了帮助开发者发现和修复这些漏洞，Go 团队在 2021 年 11 月发布了一个新的工具：Govulncheck，Go 语言的安全守护者。

## 开源项目

1、[llama2.go](https://github.com/nikolaydubina/llama2.go)

LLaMA-2 Go 接口。还有另外一个 <https://github.com/tmc/go-llama2>。

2、[imgdiet](https://godocs.io/git.sr.ht/~jamesponddotco/imgdiet-go)

imgdiet 包利用 C 的 [libvips] 图像处理库及其 Go 绑定 [govips] 提供了简单快速的图像处理和压缩解决方案。

3、[roadrunner](https://github.com/roadrunner-server/roadrunner)

一个开源（MIT 许可）高性能 PHP 应用程序服务器、负载均衡器和进程管理器。它支持作为服务运行，并且能够在每个项目的基础上扩展其功能。

4、[sqlc](https://github.com/sqlc-dev/sqlc)

从 SQL 生成类型安全代码。

5、[risor](https://github.com/risor-io/risor)

面向 Go 开发人员和 DevOps 的快速灵活的脚本语言。

6、[moss](https://github.com/deep-project/moss)（作者自荐）

一款简单轻量的内容管理系统。

7、[gws](https://github.com/lxzan/gws)（作者自荐）

高吞吐低消耗用户友好的 websocket server & client。

## 资源&&工具

1、[gonew](https://pkg.go.dev/golang.org/x/tools/cmd/gonew)

一个实验性的工具，目的是为了探索如何使用项目模板来简化 Go 开发者的工作流程。

2、[tstat](https://github.com/nickfiggins/tstat)

提供了一种友好的方式来查询 Go 测试输出和覆盖配置文件。

3、[bed](https://github.com/itchyny/bed)

Go 实现的二进制编辑器。

4、[explain-source-code-by-chatgpt（作者自荐）](https://github.com/cuishuang/explain-source-code-by-chatgpt)

让 chatgpt 讲解 go 源码中每一个文件，变量，struct 和 func 的作用。

5、[Golang-Concurrency-Pattern-Demo](https://github.com/StudyPlace-io/Golang-Concurrency-Pattern-Demo)（作者自荐）

提供各种常见的并发模式 demo。

6、[go-optioner](https://github.com/chenmingyong0423/go-optioner)（作者自荐）

一个根据结构体定义自动生成函数选项模式（functional options pattern）代码的工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
