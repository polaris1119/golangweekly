# Go语言爱好者周刊：第 41 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue041/cover.png)

题图：来自 A Journey With Go

## 刊首语

SQLBoiler 是用于生成针对你的数据库 schema 的 Go ORM 的工具。它是“数据库优先” ORM，而不是“代码优先”（如 gorm/gorp 等是代码优先的）。这意味着你必须首先创建数据库 schema。请使用 [goose](https://bitbucket.org/liamstask/goose)，[sql-migrate](https://github.com/rubenv/sql-migrate) 之类的工具或其他一些迁移工具来管理数据库生命周期的这一部分。

不管你喜不喜欢 ORM，相关的工具的确很多！

## 资讯

1、[Go 1.15 都有哪些值得关注的变化？](https://mp.weixin.qq.com/s/FB2q4CD9XLvp3c3ilQMINA)

这是来自 4月 26 日 Go Remote Fest 会议的分享整理，原标题：《What’s coming in Go 1.15》，一起看看计划在今年 8 月份发布的 Go1.15 都有哪些值得关注的变化。本文提到的点，大部分已经 Merge，毕竟包括 8 月份只剩下 3 个月了。之前提到过，受疫情影响，这次的发布内容不会太多。

2、[Vitness 发布 v6 版本](https://vitess.io/blog/2020-04-29-announcing-vitess-6/)

Youtube 使用 Go 实现的开源分布式 MySQL 工具。

3、[改善 go module major 版本体验的 proposal](https://github.com/golang/go/issues/38762)

不断改进 module。

4、[Liftbridge 1.0 发布](https://github.com/liftbridge-io/liftbridge)

通过为 NATS 消息传递系统实施持久的流增强，Liftbridge 提供了轻量级的，容错的消息流。

## 文章

1、[如何在 3 天内使用 Go 和 Vue 创建实时患者监护系统](https://mp.weixin.qq.com/s/aDGpq_6WWGgwZRktPocJNA)

程序员为疫情做贡献。

![](imgs/issue041/go-vue-patient-monitor.png)

2、[项目中要不要使用 Go？我是这么思考的](https://mp.weixin.qq.com/s/UrTLGhPE9HaNGG6zBuAETw)

我最近决定在一个新项目中使用 GoLang 来实现一组增删改查的 API。在此之前，我较为熟悉 Java，Groovy，了解一些 Python。

3、[[典藏版\]Golang三色标记、混合写屏障GC模式图文全分析](https://mp.weixin.qq.com/s/G7id1bNt9QpAvLe7tmRAGw)

如今，GC 话题成为后端工程师面试和闲聊的主话题，今天我们就详细的来聊一聊。

4、[基于 Go 语言开发在线论坛增补篇：通过 Viper 读取配置文件并实现热加载](https://mp.weixin.qq.com/s/0UPWFvku1mts5SYL9ERFHQ)

Viper 是 Go 语言的完整配置解决方案，支持多个数据源和丰富的功能。

5、[Go、Java 和 Rust 的比较：得出了挺多结论](https://mp.weixin.qq.com/s/sH5jad9_5-QZx6X1jV_HUw)

最近这几年，Go、Rust 收到越来越多的关注，特别是 Go，在国内挺受欢迎的，很多大公司都采用它。而 Rust，作为系统编程语言收到越来越多的人关注，苹果、微软都宣称他们使用 Rust 编写部分业务。而 Java 作为老牌编程语言，长期霸占编程语言排行榜第一或第二位。这篇文章从一些角度就以上三门语言做一个对比。

6、[Dave 大神详解 Go 中的内联优化](https://mp.weixin.qq.com/s/SdGZKXCloypcCClGNDbU7Q)

本文讨论 Go 编译器是如何实现内联的以及这种优化方法如何影响你的 Go 代码。

7、[“���”引发的线上事故](https://mp.weixin.qq.com/s/xe8KXD39YlJdDG4cLT0veA)

最近遇到了一起依赖升级 + 异常数据引发的线上事故，教训惨痛，本文对此进行回故和总结。

8、[万字长文！Go 后台项目架构思考与重构](https://mp.weixin.qq.com/s/UQZGqAumYurTqbZCAbeQCQ)

本文首先介绍了架构的重要性，随后从一个实际项目的重构过程作为主线，逐步引出主流的架构设计思想以及其所解决的实际问题是什么。

9、[这是一篇实践者对 Go 语言的微吐槽](https://mp.weixin.qq.com/s/UP_Rf-x1HekU-nl7BneVyg)

本文作者最近开始在工作中将 Go 作为主力编程语言来使用，这是一种有趣的语言，带有丰富的标准库，但在标准库中交付一个生产就绪的 HTTP 服务器并非易事。因此，作者写下了这篇文章，提到了 Go 语言的一些问题。 

10、[踩坑记：Go 服务内存暴涨](https://segmentfault.com/a/1190000022472459)

为什么 go 1.12 会导致内存异常上涨呢？

11、[Rob Pike专访：“Go确实已成为云基础架构编程语言”](https://tonybai.com/2020/05/01/rob-pike-interview-go-become-the-language-of-cloud-infrastructure/)

尽管看到 Docker，Kubernetes 和用 Go 编写的云计算的许多其他组件令人欣喜和重要，但也许并不奇怪。Go 确实已经成为云基础架构的语言。- Rob Pike，Go 编程语言的联合作者。

![](imgs/issue041/rob-pike.jpg)

12、[使用 Go 开发前端 WASM 应用](https://mp.weixin.qq.com/s/cBjk4jOjX7mdsXuS4r-l-g)

Go 近些年在国内越来越流行了，特别是上云，容器化发展之后。关键的是，Go 不仅性能好，而且占用内存等也非常少，目前大部分新的后台项目也都在使用 Go 重写。这篇文章主要用来介绍，用 Go 语言如何入门前端开发。

13、[Go 中的 Goroutine + Channel 真的能减少并发 Bug 吗？](https://mp.weixin.qq.com/s/7ivK7eLA7o8lerZ19If0WA)

Go 目前正在通过新的并发原语（concurrency primitives）goroutine 和 channel 试图简化并发编程并减少报错。但是，实际情况怎么样呢？两位来自宾夕法尼亚州立大学和普渡大学的研究员 Yiying Zhang 和 Linhai Song 对 Go 中的 并发 bug 在真实场景的情况进行了研究。

14、[我使用 Golang 两年后的总结：优点和令人讨厌的怪癖](https://www.infoq.cn/article/yDMrvVr1IJAAih3eh5fW)

过去两年来，我就职于 Assembled ，一直使用 Go 工作。自公司成立以来，Go 就一直是我们的主要后端语言。在我之前的工作中，我混合着使用 Ruby 和 Scala，所以肯定有过一段适应期。总体而言，我发现 Go 的表现基本上与广告宣传的一样：尽管有些怪异，但它非常适合专业工作。

## 开源项目

1、[XLSX](https://github.com/tealeg/xlsx)

用于读取和写入 XLSX（Excel）文件的库。

2、[SQLBoiler](https://github.com/volatiletech/sqlboiler)

根据你的数据库 schema 生成 Go ORM。

3、[decimal](https://github.com/shopspring/decimal)

表示 Go 中的任意精度十进制数。不过，它只能支持小数点后最多 2^38 位的十进制数，因此请当心。

4、[redigo](https://github.com/gomodule/redigo)

Redis 6.0 已经发布了。这是一个 Redis 的 Go 语言客户端。

5、[ntp](https://github.com/facebookincubator/ntp)

Facebook 的 NTP 库。NTP 是 “网络时间协议”，进行时钟同步。

6、[grobotstxt](https://github.com/jimsmart/grobotstxt)

Google Robots.txt 解析器和 Matcher 库。现在您可以像 Google 一样抓取自己的网站

7、[compiler](https://github.com/MauriceGit/compiler)

编译成 x86-64 汇编语言的小型编译器。

8、[goneli](https://github.com/obsidiandynamics/goneli)

实现NELI分布式选主协议。

9、[skycoin](https://github.com/SkycoinProject/skycoin)

又一以 Go 为主要实现语言的币项目。

10、[errlog](https://github.com/snwfdhmp/errlog)

可改善错误日志格式并加快调试速度的 log 包。

![](imgs/issue041/errlog.png)

11、[sftpgo](https://github.com/drakkan/sftpgo)

全功能且高度可配置的 SFTP 服务器。

12、[gout](https://github.com/guonaihong/gout)

http client 领域的瑞士军刀，小巧，强大，犀利。

## 资源&&工具 

1、[播客：gotime 第 127 期](https://changelog.com/gotime/127)

使用 Go 实现 WebRTC 应用。

2、[GoRemoteFest 2020 会议视频全集](https://www.youtube.com/watch?v=OZSJ2fwSSUM&list=PLdeYrDm3hJTh21xi3rezgsSqrZl_Xs0VA)

记得上周周刊提到的这个大会吗？完整视频放送。

3、[Go-sword](https://github.com/sunshinev/go-sword)

可视化 Web 管理后台生成工具。

4、[开源电子书](https://github.com/miguelmota/ethereum-development-with-go-book)

使用 Go 进行以太坊开发。

5、[Super Graph](https://github.com/dosco/super-graph)

快速将 PostgreSQL 应用升级为 GraphQL 接口。

6、[shotizam](https://github.com/bradfitz/shotizam)

分析 binary 文件 size 的工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
