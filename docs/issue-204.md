# Go语言爱好者周刊：第 204 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue204/cover.jpeg)

题图：Go 14 周年。

## 资讯

1、[go-redis v9.3.0 发布](https://github.com/redis/go-redis)

类型安全的 Redis Go 客户端。JSON 支持。

2、[env v10.0 发布](https://github.com/caarlos0/env)

简单的 lib 可以将环境变量解析为结构体。

3、[goleak v1.3 发布](https://github.com/uber-go/goleak)

Uber 出品的 goroutine 泄露检测器。

4、[cobra v1.8.0 发布](https://github.com/spf13/cobra)

一个构建现代 CLI APP 的框架。

5、[color v1.16 发布](https://github.com/fatih/color)

颜色文本输出包。

6、[spago v1.1 发布](https://github.com/nlpodyssey/spago)

纯 Go 的机器学习库。

## 文章

1、[为什么使用Golang而非Rust开发桌面应用？](https://mp.weixin.qq.com/s/dvZcAG1gXIbll_aQI8KYFg)

MoonGuard 团队选择 Golang 而不是 Rust 作为他们的 Krater 桌面应用程序，因为 Golang 中更容易进行内存管理、类型安全和 ORM 支持。

2、[Go1.21.4 发布了：官方图片竟然用的 loong64](https://mp.weixin.qq.com/s/uTnb9QQrFfs5jdmFmFzd7Q)

Go 官方发布了 Go1.21.4 和 Go1.20.11，这是两个小版本，主要是 2 个安全更新，涉及 path/filepath 库。

3、[最好的 Go 框架就是不用框架？](https://mp.weixin.qq.com/s/PJJjOhhhF_3mteF3gK7JCg)

许多人建议你根本不应该（在 Go 中）使用框架。他们疯了吗？

4、[必须知道的 17 个Go开发库](https://mp.weixin.qq.com/s/vlpTUltiV_ZR8Ql95h5lBQ)

随着时间的推移，Go语言爱好者已经创建并共享了许多Go框架和库。这些库有不同的功能，从微服务开发到构建web应用程序。

5、[通过实例理解Web应用用户密码存储方案](https://mp.weixin.qq.com/s/_iT9GAtn0hQXDQYW_PbPCA)

在这篇文章中，我们就来说说Web应用的各种密码存储方案的优缺点，并通过实例来理解一下当前的主流存储方案。

## 开源项目

1、[doltgresql](https://github.com/dolthub/doltgresql)

世界上第一个版本控制 SQL 数据库。

2、[tqla](https://github.com/vauntdev/tqla)

一个小型轻量级文本解析器，包装了 Go 语言 text/template 标准库。

3、[warrant](https://github.com/warrant-dev/warrant)

一种高度可扩展的集中式授权服务，用于定义、存储、查询、检查和审计应用程序授权模型和访问规则。

4、[ttlMap](https://github.com/jftuga/ttlMap)

一种 Go 语言 map，其中条目在给定时间段后过期。

## 资源&&工具

1、[oapi-codegen](https://github.com/deepmap/oapi-codegen)

从 OpenAPI 3 规范生成 Go 客户端和服务器样板。

2、[bluetuith](https://github.com/darkhz/bluetuith)

用于 Linux的 TUI 蓝牙管理器。

3、[beelzebub](https://github.com/mariocandela/beelzebub)

一个安全的低代码框架，利用 AI 进行系统虚拟化。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
