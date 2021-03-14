# Go语言爱好者周刊：第 85 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs//issue085/cover.png)

题图：女神节快乐

## 刊首语

以下程序输出什么？（来自 Go101 作者）

```go
package main

func main() {
  var x chan<-chan error   // nil
  var y chan(<-chan error) // nil
  println(x == y)
}
```

A：true；B：false；C：无法编译；D：运行时 panic

## 谁在招 Gopher

整理近期的 Go 职位。有招聘需求可以到「Go招聘」发布！

1、[你可能不了解，这两年跨境电商很火的：招 Go 了](https://mp.weixin.qq.com/s/UKAPNHGbWoCPzFirFfWJ5g)

2、[鹅厂游戏业务招Go这要求，你符合吗？](https://mp.weixin.qq.com/s/Vzeo6YKSArYq29d4WrDflw)

3、[360 加大 Go 招聘，Go 形势大好！你来吗？](https://mp.weixin.qq.com/s/gjx3gz6ngTN1d6Sew1nc-w)

4、[想跟Gorm作者做同事嘛？一起来字节做性能分析平台吧！](https://mp.weixin.qq.com/s/r_0C9q-Tl7VPW-gyQ6ivuQ)

5、[【上海招聘】数据隐私很重要：招 gopher 保驾护航](https://mp.weixin.qq.com/s/NZmCcj5Pf2PvPCEP4Lsj-Q)

6、[【内推】一大波 Go 相关职位涌来：金山办公 wps 招聘](https://mp.weixin.qq.com/s/zt2RJwCst7Back7k8IKZfg)

## 资讯

1、[gosec 2.7 发布](https://github.com/securego/gosec)

Go 代码安全检查器。

2、[Inlets 3.0 发布](https://github.com/inlets/inlets)

ngork 的替代品。轻松将服务暴露到公网或其它网络，穿透内网、代理和 NAT。

3、[sqlc 1.7.0 发布](https://github.com/kyleconroy/sqlc)

从 SQL 产生类型安全的 Go 代码。

4、[955 不加班公司名单](https://mp.weixin.qq.com/s/DfrwMYrTWsQaB9RQKHwySg)

招聘季，选工作挺重要。

5、[Redmonk 2021.1月编程语言排行榜](https://redmonk.com/sogrady/2021/03/01/language-rankings-1-21/)

Go 排名第 16。

## 文章

1、[Uber 的 zap 库是如何做到高性能的？](https://mp.weixin.qq.com/s/y8XH4gTo_7l0FkMJe9zxiA)

Go 生态系统有许多流行的日志库，选择一个可以在所有项目中使用的日志库对于保持最小的一致性至关重要。易用性和性能通常是我们在日志库中考虑的两个指标。

2、[那些 Go 语言实现的语言现在发展怎么样了？](https://mp.weixin.qq.com/s/jIdBxFlNnJ_XaGOOsUf_3w)

Go 是一门通用编程语言，Go1.5 实现了自举，也就是说，Go 语言是用它自身实现的。经过十来年的发展，开源界使用 Go 语言实现的编程语言不少，那它们发展的怎么样？本文进行一下梳理。

3、[惊！Go 编写的恶意软件剧增 2000%](https://mp.weixin.qq.com/s/JtX9ltxHjBm7u3f4h9Nk9Q)

网络安全公司 Intezer 在近日发布的一份报告中称，自 2017 年以来，用 Go 编程语言编写的恶意软件数量在过去几年中急剧增加了约 2000% 。

4、[构建微服务的十大 Go 框架/库](https://mp.weixin.qq.com/s/_i31PW_lhuYxKbRM-a8wEA)

现在，很多开源库都支持构建应用程序。我应该向你推荐一些库，它们可以帮助启动具有简单设计、干净代码和良好性能的项目。

5、[一文快速了解 Go+，还有机会和创始人面基](https://mp.weixin.qq.com/s/wL4GQGTdgGzhtgCVsqnS_Q)

七牛 Go+，想要进军数据科学领域。

6、[Goroutine 的切换过程涉及了什么](https://mp.weixin.qq.com/s/r0y4Fweq-YGo1FZrsNsl3A)

Goroutine 很轻，它只需要 2Kb 的内存堆栈即可运行。另外，它们运行起来也很廉价，将一个 Goroutine 切换到另一个的过程不牵涉到很多的操作。在深入 Goroutine 切换过程之前，让我们回顾一下 Goroutine 的切换在更高的层次上是如何进行的。

7、[Go：使用 Delve 和 Core Dump 调试代码](https://mp.weixin.qq.com/s/bwC12L1_h0Vl4e1wk50Fjw)

core dump 是一个包含着意外终止的程序其内存快照的文件。这个文件可以被用来事后调试（debugging）以了解为什么会发生崩溃，同时了解其中涉及到的变量。通过 `GOTRACEBACK`，Go 提供了一个环境变量用于控制程序崩溃时生成的输出信息。这个变量同样可以强制生成 core dump，从而使调试成为可能。

8、[详解 Go 反射并实战一例](https://mp.weixin.qq.com/s/V2hcadvRmjy6Lr9bUoBLmw)

Go 的反射机制带来很多动态特性，一定程度上弥补了 Go 缺少自定义范型而导致的不便利。

9、[官发博文：进一步阐明关于 context 的最佳实践](https://mp.weixin.qq.com/s/Xv88vljtnDIRuLM0J_NSpA)

关于 context 的一点最佳实践。

10、[图解Go语言Context](https://mp.weixin.qq.com/s/SuYSo_APH2viuWiVxezyVQ)

一般新技术的出现都是为了解决现有技术存在的问题或者可以提供更优雅方便的实现方式，那我们就要想想 contex 包能解决什么问题？

11、[Go mod 七宗罪](https://mp.weixin.qq.com/s/CBiebXjBcik2pHQnbnB51A)

曹大还写了一篇：[吐槽 Go mod](https://mp.weixin.qq.com/s/N-mztlf9ARJUXd9wJGC4BQ)。

12、[Go 面试题： new 和 make 是什么，差异在哪？](https://mp.weixin.qq.com/s/tZg3zmESlLmefAWdTR96Tg)

在 Go 语言中，有两个比较雷同的内置函数，分别是 new 和 make 方法，其主要用途都是用于分配相应类型的内存空间。

13、[内存管理设计精要](https://mp.weixin.qq.com/s/lx0vX-4wlQWxxfj017T9HA)

系统设计精要是一系列深入研究系统设计方法的系列文章，文中不仅会分析系统设计的理论，还会分析多个实际场景下的具体实现。

## 开源项目

1、[generativeart](https://github.com/jdxyw/generativeart)

编写创造艺术的代码。如下代码：

```go
func main() {
	rand.Seed(time.Now().Unix())
	c := generativeart.NewCanva(500, 500)
	c.SetBackground(generativeart.White)
	c.FillBackground()
	c.SetColorSchema([]color.RGBA{
		{0xCF, 0x2B, 0x34, 0xFF},
		{0xF0, 0x8F, 0x46, 0xFF},
		{0xF0, 0xC1, 0x29, 0xFF},
		{0x19, 0x6E, 0x94, 0xFF},
		{0x35, 0x3A, 0x57, 0xFF},
	})
	c.Draw(generativeart.NewRandomShape(150))
	c.ToPNG("randomshape.png")
}
```

生成下面的图片：

![](imgs//issue085/generateariveart.png)

作者还写了一本[同名书](https://preslav.me/generative-art-in-golang/)。

2、[MongoDB 的轮子：lungoDB](https://github.com/256dpi/lungo)

适用于 Go 的 Mongo DB兼容嵌入式数据库和工具包。好吧，其实也不能完全算是轮子。

3、[roadrunner](https://github.com/spiral/roadrunner)

用 Go 编写的高性能 PHP 应用程序服务器，负载均衡器和流程管理器。

![](imgs//issue085/roadrunner.png)

4、[sedna](https://github.com/kubeedge/sedna)

基于 kubeedge 的 AI 套件。

5、[go-git-crypt](https://github.com/jbuchbinder/go-git-crypt)

简单的本地 go git-crypt 实现。目前还是不稳定版本。

6、[twitter-backend](https://github.com/arman-aminian/twitter-backend)

使用 Go 开发的类 Twitter 后端。

7、[mini](https://github.com/hibiken/mini)

一个 Go 编写的简易文本编辑器。

8、[lieu](https://github.com/cblgh/lieu)

Go 实现的社区搜索引擎。

## 资源&&工具

1、[新书：Network Programming with Go](https://nostarch.com/networkprogrammingwithgo)

3 月即将出版，目前已经预售了。跟之前[网上开源的版本](https://github.com/tumregels/Network-Programming-with-Go)不是一个作者。

2、[sq](https://github.com/neilotoole/sq)

通用的“瑞士军刀”数据工具。

3、[song2](https://github.com/matsuyoshi30/song2)

Go 实现的快速高斯模糊。

![](imgs//issue085/song2.png)

4、[chkb](https://github.com/MetalBlueberry/chkb)

可以将你的键盘变成可编程键盘的 Go 工具。

5、[KubernetesPatterns](https://github.com/sharadbhat/KubernetesPatterns)

使用 Go 和 yaml 实现的 Kubernetes 模式。

6、[微软真棒：出 Go 语言教程了](https://mp.weixin.qq.com/s/7bbJEgmE7LPRpBCVNw_Hcg)

中文版也快要出来了。

7、[播客第 169 期](https://changelog.com/gotime/169)

Clever 公司的 Go 使用情况。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs//wechat.png)
