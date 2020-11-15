# Go语言爱好者周刊：第 69 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue069/cover.jpg)

题图：Go 11 岁

## 刊首语

本周 Go 社区重要的事件不少。比如 Go 开源 11 周年，[GopherCon 2020 大会](https://www.gophercon.com/agenda)，[GopherCon 2020 TW 大会](https://gophercon.golang.tw/2020/)等。

## 资讯

1、[Go 1.15.5 和 Go 1.14.12 发布](https://mp.weixin.qq.com/s/4qua5OKwrIeRpj4YEasS7g)

解决最近报告的安全问题。

2、[使用 Go 语言编写 GitHub Action](https://github.blog/2020-10-29-github-action-hero-eyal-posener-and-go-action/)

项目地址：<https://github.com/posener/goaction>。

3、[祝贺 Go 开源 11 周年](https://mp.weixin.qq.com/s/PZW8EUIsL8PN4o4QP8sTUw)

2009.11.10 ~ 2020.11.10，官方发布了博文：<https://docs.studygolang.com/blog/11years>。

![](imgs/issue069/11-years.png)

4、[pkg.go.dev 改版上线](https://docs.studygolang.com/blog/pkgsite-redesign)

自启动 pkg.go.dev 以来，收到了很多有关设计和可用性的反馈。特别是，在浏览网站时，信息的组织方式使用户感到困惑。因此做了改版。

5、[说好的 Go1.17 支持泛型又推迟了：给你 GopherCon2020 全套 PPT 安慰下](https://mp.weixin.qq.com/s/utgObH5DvEJx66oCqZAYsg)

回顾了过去一年 Go 的发展，同时展望未来一年。

6、[gopls 0.5.3 发布](https://github.com/golang/tools/releases/tag/gopls%2Fv0.5.3)

增加了一些特性。

## 文章

1、[Micro 不能用了？关于 Go 语言微服务框架 Micro 的一些情况说明](https://mp.weixin.qq.com/s/Q2JHFcIArFP60tJIdL5bVg)

Micro 3.0 大变样了。

2、[Go 之旅：Goroutine 的开启和退出](https://mp.weixin.qq.com/s/i703SEiZVolaV4e0DhfYPw)

在 Go 中，协程就是一个包含程序运行时的信息的结构体，如栈，程序计数器，或者它当前的 OS 线程。调度器还必须注意 Goroutine 的开始和退出，这两个阶段需要谨慎管理。

3、[Go设计模式实战：并发组件](https://mp.weixin.qq.com/s/mgrn2TL8SPnHuMzXkk6qeA)

分享如何在我们的真实业务场景中使用设计模式。

4、[golang chan 最详细原理剖析，全面源码分析！看完不可能不懂的！](https://mp.weixin.qq.com/s/_mOOGOEhc8w7sbMaFuZV5w)

本文教你从源码编译器的角度全方位的剖析 channel 的用法。

5、[通过实例深入理解 sync.Map 的工作原理](https://tonybai.com/2020/11/10/understand-sync-map-inside-through-examples/)

近期在项目考虑在内存中保存从数据库加载的配置数据的方案，初步考虑采用 map 来保存。

6、[也许是最客观、全面的比较 Rust 与 Go：都想把 Rust 也学一下](https://mp.weixin.qq.com/s/CcX1ef1ZWnEgSVMpQDsVVQ)

最近一年，将 Rust 和 Go 进行比较的不少，但不少都不公正，带感情色彩。而这篇文章客观、全面的分析对比了 Rust 和 Go，让你具体项目时选择最合适的。

7、[分析字节跳动高级 Go 工程师的要求，知晓自己的努力方向](https://mp.weixin.qq.com/s/I99vnfM7pd3xo2--3UDJGA)

字节跳动的招聘信息。

8、[字节跳动面试真的也会问这样的问题？！](https://mp.weixin.qq.com/s/gUOZJiC5fTs3eMa2FESETg)

这道题出的还是很不错的。

9、[图解 Golang 实现 RSA 加密和签名（有示例）](https://mp.weixin.qq.com/s/fucLz41Q-IHd_xy8c5o2fg)

本文介绍 RSA 干了什么，以及我们怎样用 Go 实现它。	

10、[Go 中使用别名，简单且高效](https://mp.weixin.qq.com/s/auYq7XGFtYS4_uslfgu61Q)

Go 1.9 版本引入了别名，开发者可以为一个已存在的类型赋其他的名字。这个特性旨在促进大型代码库的重构，这对大型的项目至关重要。

## 开源项目

1、[go-edlib](https://github.com/hbollon/go-edlib)

字符串比较和距离算法库。

2、[tfgo](https://github.com/galeone/tfgo)

tensorflow + Go，gopher 的方式。

3、[wombat](https://github.com/rogchap/wombat)

跨平台的 gRPC 客户端。

![](imgs/issue069/wombat.png)

这个界面是使用 <https://github.com/wailsapp/wails> 开发的。

4、[LadonGo](https://github.com/k8gege/LadonGo)

一款 Go 开发的开源渗透扫描器框架。

5、[stream](https://github.com/youthlin/stream) （作者投稿）

Go Stream，类似 Java 8 的 Stream。

## 资源&&工具

1、[writefreely](https://github.com/writeas/writefreely)

构建数字化写作社区。

2、[muffet](https://github.com/raviqqe/muffet)

Go 实现的快速网站链接检查器。

![](imgs/issue069/muffet.gif)

3、[Go Time 第 155 期](https://changelog.com/gotime/155)

一直在讨论往 Go 中增加特性，这次讨论你觉得哪些应该从 Go 中移除。

4、[teler](https://github.com/kitabisa/teler)

实施 http 入侵检测。

5、[earlybird](https://github.com/americanexpress/earlybird)

源码中敏感数据的检测工具。

6、[油管视频](https://www.youtube.com/watch?v=EsSebOAD5yw)

使用 go-fuzz 和 libfuzzer 对 Go 包进行随机测试。

7、[go-audio](https://github.com/Harry-027/go-audio)

将 PDF 转换为有声读物的离线解决方案（Go 语言实现）。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
