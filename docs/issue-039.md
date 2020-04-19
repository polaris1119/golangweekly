# Go语言爱好者周刊：第 39 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue039/guyu.png)

题图：今日谷雨，春的尾巴，夏天就要到来了。（图来自网络）

## 刊首语

优惠购书活动：[目前 Go 语言中文书籍都在这，满400减230！总有你需要的](https://mp.weixin.qq.com/s/vYdO1PIKmWmA4NFF3hvnnQ)，有效期截止 4 月 23 日。不限于文中列出的图书，其他图书也可以。

Playground 先上线了一个新功能：预置了一些常用代码模板。为了方便使用，我搭建了一个完整镜像，同步了官方最新的功能，欢迎试用，地址：<https://play.studygolang.com>。

## 资讯

1、[go-micro 2.5.0 发布](https://github.com/micro/go-micro/releases/tag/v2.5.0)

最近更新有点频繁啊！

2、[Ebiten 1.11.0 发布](https://ebiten.org/blog/v1.11.0.html)

Go 2D 游戏开发库。Ebiten 是项目中的真正瑰宝之一。

3、[TiDB 3.1.0 发布](https://www.oschina.net/news/114972/tidb-3-1-0-released)

这是一个分布式 NewSQL 数据库。

## 文章

1、[Go Vet 命令：超出预期的强大](https://mp.weixin.qq.com/s/EPfsrWxPWIO8OpbNncugbw)

Go vet 命令在编写代码时非常有用。它可以帮助您检测应用程序中任何可疑、异常或无用的代码。该命令实际上由几个子分析器组成，甚至可以与您的自定义分析器一起工作。让我们首先回顾一下内置的分析器。

2、[Go 的泛型真的要来了—如何使用以及它们是怎么工作的](https://mp.weixin.qq.com/s/_2O7QF8fvTKFL5Zvo8lb5w)

你没看错，这里讲的就是 Go 中的泛型。只不过还没有正式发布，是基于草案设计的，已经是实现了可运行的版本。所以，泛型到来真的不远了！

3、[Go 监控模式（Monitor Pattern）](https://mp.weixin.qq.com/s/IBzOPxNI6Z7MlnQXA9EXmA)

Go 能实现监控模式，归功于 sync 包和 sync.Cond 结构体。监控模式允许 goroutine 在进入睡眠模式前等待一个定特定条件，而不会阻塞执行或消耗资源。

4、[Go 的 Channel 很强大，理解其内在概念会让它更强大](https://mp.weixin.qq.com/s/QYY4Z6umM5wn7U5Idwb8PA)

Go 中的通道（channel）机制十分强大，但是理解内在的概念甚至可以使它更强大。实际上，选择缓冲通道或无缓冲通道将改变应用程序的行为和性能。

5、[Golang 爬虫快速入门 | 获取B站全站的视频数据](https://imagician.net/archives/92/)

提到爬虫，总会联想到Python。似乎Python是爬虫的唯一选择。爬虫只是完成一个访问页面然后收集数据的任务，用任何语言来写都能实现。相比较Python快速实现但是庞大的体型，Golang来写爬虫似乎是更好的又一选择。

6、[Go 语言踩坑记——panic 与 recover](https://juejin.im/post/5e97263c6fb9a03c97754ab7)

Go 语言自发布以来，一直以高性能、高并发著称。因为标准库提供了 http 包，即使刚学不久的程序员，也能轻松写出 http 服务程序。不过，任何事情都有两面性。一门语言，有它值得骄傲的有点，也必定隐藏了不少坑。新手若不知道这些坑，很容易就会掉进坑里。《 Go 语言踩坑记》系列博文将以 Go 语言中的 panic 与 recover 开头，给大家介绍笔者踩过的各种坑，以及填坑方法。

7、[轻量级 Kubernetes k3s 初探](https://www.infoq.cn/article/0c7viUfLrxOZeh7qlRBT)

k3s 是 rancher® 开源的一个 Kubernetes 发行版，从名字上就可以看出 k3s 相对 k8s 做了很多裁剪和优化，二进制程序不足 50MB，占用资源更少，只需要 512MB 内存即可运行。

8、[3 个减小 Docker 镜像的简单技巧](https://mp.weixin.qq.com/s/UCm27by8Ro7NzFflsPISCQ)

当涉及到建造Docker containers问题的时候，你应该尽力获得较小的镜像。文件层既共享又小的镜像能够更快的进行传输和部署。

9、[2020 Golang 字节面试经验分享](https://studygolang.com/articles/28066)

2020 年 4 月份字节跳动后端面试经验。

10、[微服务项目讲解](https://studygolang.com/articles/28074)

详细介绍微服务。

## 开源项目

1、[broccoli](https://github.com/aletheia-icu/broccoli)

使用谷歌 Brotli 压缩的，在 Go 中嵌入静态文件。这个需求，Go 官方官方什么时候能支持呢？

![](imgs/issue039/broccoli.png)

2、[3mux：受 i3 启发的终端多路复用器](https://github.com/aaronjanse/3mux)

想象一下像 tmux 这样的东西，但是更易于学习并且具有合理的默认值。另外，它是用 Go 语言编写的，因此你可以根据需要进行任意调整。

![](imgs/issue039/3mux.gif)

3、[GeoDB: 支持持久化的地理空间数据库](https://github.com/autom8ter/geodb)

使用 Badger gRPC 和 Google Maps API 构建。跨边界或相对于其他对象跟踪对象的地理位置。

4、[gocorona](https://github.com/ayoisaiah/gocorona)

冠状病毒终端统计信息显示板。

5、[gosql](https://github.com/eatonphil/gosql)

一个 PostgreSQL 的早期实现版本。

6、[what](https://appliedgo.net/what/)

仅给 Go 开发人员使用调试级别 log 包。

7、[dbq](https://github.com/rocketlaunchr/dbq)

号称是 database/sql 包的替代品。

8、[edwood](https://github.com/rjkroege/edwood)

Go 版本 Plan9 Acme 编辑器。

9、[golisp](https://github.com/mattn/golisp)

Go Lisp 解析器。

10、[testcase](https://github.com/adamluzsi/testcase)

一款 Go TDD 测试框架。

11、[earthly](https://github.com/vladaionescu/earthly)

容器化时代的自动化构建工具。

## 资源&&工具 

1、[播客：和 Erik St. Martin 聊聊 Go](https://6figuredev.com/podcast/episode-139-talking-go-with-erik-st-martin/)

Erik St. Martin 是 GopherCon组织者、Go In Action 联合作者。

2、[播客: gotime 125](https://changelog.com/gotime/125)

谈 Go 社区组织经验。

3、[数据结构和算法：Go语言实现](https://goa.lenggirl.com/)

数据结构和算法在计算机科学里，有非常重要的地位。此系列文章尝试使用 Golang 编程语言来实现各种数据结构和算法，并且适当进行算法分析。

4、[Go Web 开发开源书](https://thewhitetulip.gitbooks.io/webapp-with-golang-anti-textbook/content/)（英文）

又一本开源的 Go Web 图书。

5、[电子书: The BlockChain way of programming](https://web3coach-public.s3.eu-central-1.amazonaws.com/the-blockchain-way-of-programming-newsletter-version.pdf)

目前只公开了前 6 章。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
