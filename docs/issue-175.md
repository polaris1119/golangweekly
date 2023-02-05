# Go语言爱好者周刊：第 175 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue175/cover.jpeg)

题图：Go1.20 发布

## 刊首语

Go 2023 调查问卷，期待你的参与：<https://google.qualtrics.com/jfe/form/SV_bNnbAtFZ0vfRTH8?s=t>。

## 资讯

1、[调查显示 2023 年开发者最想学习 Go 和 Rust](https://thenewstack.io/developers-most-likely-to-learn-go-and-rust-in-2023-survey-says/)

JetBrains 发起的调查。

2、[GopherCon UK 2023 8 月举行](https://sessionize.com/gophercon-uk-2023)

演讲者已经确定。

3、[gofeed 1.1 发布](https://github.com/mmcdole/gofeed)

RSS、Atom 和 JSON Feed 解析器。

4、[goldmark 1.5.0 发布](https://github.com/yuin/goldmark)

拥有易于扩展且与 CommonMark 兼容的优势。写过一篇文章专门介绍这个库。[专为 Gopher 准备的 Markdown 教程](https://mp.weixin.qq.com/s/8wz4U2DakVsU4tMoO-ultA)。

5、[Ginkgo 2.8 发布](https://github.com/onsi/ginkgo)

现代的测试框架。

6、[tempo 2.0](https://github.com/grafana/tempo)

一个开放源代码，易于使用的大规模分布式跟踪后端。

7、[FerretDB v0.9.0](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。

8、[fq 0.3 发布](https://github.com/wader/fq)

类似 jq，但用于二进制文件。

9、[env 7.0 发布](https://github.com/caarlos0/env)

简单的 lib 可以将环境变量解析为结构体。

## 文章

1、[sourcegraph 出品的并发库 conc 详解](https://mp.weixin.qq.com/s/59cxPFHWcdnUxKyRyo8SKw)

每个公司都有类似的轮子，与以往的库比起来，多了泛型，代码写起来更优雅，不需要 interface, 不需要运行时 assert, 性能肯定更好。

2、[Go BIO/NIO探讨(4)：net/http 在 tcp conn 上的处理](https://mp.weixin.qq.com/s/8qzRRuNZSx1Diify6R4Ifw)

原文解读。

3、[为什么 Go 不支持 []T 转换为 []interface](https://mp.weixin.qq.com/s/jsdGV31yT5AR07BzRovWVw)

在 Go 中，如果 interface{} 作为函数参数的话，是可以传任意参数的，然后通过类型断言来转换。

4、[Go 1.20正式发布，最后一个支持Win7、Win8等旧系统的版本](https://mp.weixin.qq.com/s/GZ2HxJAxpZXiu_YKnzoVlw)

Go 官方正式发布了 Go1.20，相关的变化可以查看官方的 Releas Notes。

## 开源项目

1、[go-redis](https://github.com/redis/go-redis)

类型安全的 Redis Go 客户端。最新版本 V9（目前还在 RC 版本），是一个大版本。

2、[rpcx](https://github.com/smallnest/rpcx)

Go 语言的 RPC 服务治理框架，快、易用却功能强大。

3、[bob](https://github.com/stephenafamo/bob)

SQL 工具包。

4、[dex](https://github.com/dexidp/dex)

OpenID Connect（OIDC）身份和具有可插拔连接器的 OAuth 2.0 提供程序。

## 资源&&工具

1、[cupogo](https://cupogo.dev/)

一个新的 Go Weekly 新闻。

2、[cadet](https://github.com/martinrue/cadet)

创建简单的 HTTP-RPC 服务器。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
