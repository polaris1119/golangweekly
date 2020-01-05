# Go语言爱好者周刊：第 24 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue024/cover.jpeg)

题图来自：unsplash


## 刊首语

这是 2020 年的第一期，本周刊跨年了，和你陪伴了 2019 年，接下来会和你一起度过 2020 年。国外人都在休假，国内似乎动作也少，本期内容不多，但希望有对你有启发或帮助的内容。

## 资讯

1、[Go 语言中文网 2019 年终总结暨 2020 年展望](https://mp.weixin.qq.com/s/QzbQH0X04B8pa4e34XSISA)

2020年计划：2020 年一定要开始进行 2019 年发誓要做的原定于推迟到 2018 年完成的 2017 年度计划！

2、[Go 101 v1.13.m (v.1.14-pre) 电子书发布](https://github.com/golang101/golang101/releases)

本书定期（一个月左右）发布新版本，所以请时常访问此页面以获取本书最新版。

## 文章

1、[谁拔了我的网线？Go 网络异常对程序行为的影响](https://mp.weixin.qq.com/s/xXTsroriaub61Sjx8LuHKA)

本文尝试探讨几种网络异常的情况，研究在这些情况下客户端和服务端的的行为，包括连接断掉的检测能力、half-close 情况下两端的读写能力、丢包的情况等等。

2、[Go 不通过标准 C 库进行系统调用的一些原因](https://mp.weixin.qq.com/s/Ry1-ke62GXWNoN-4dUjKeQ)

本文翻译自 **Some reasons for Go to not make system calls through the standard C library**。

3、[大神是如何学习 Go 之并发编程与 Context](https://mp.weixin.qq.com/s/fRb4G74LW-es87jxWkiByw)

介绍 Go 语言中这个非常常见的 `Context` 接口，我们将从这里开始了解 Go 语言并发编程的设计理念以及实现原理。

4、[为什么 Go 适合微服务](https://mp.weixin.qq.com/s/ypR0CM32I2Z1unVwrFZ2hQ)

去年早些时候，我们决定改用 Go(Golang) 作为我们（**SafetyCulture**）开发微服务的选择。在这之前，我们的微服务使用 Node.js(CoffeeScript, Javascript 和 TypeScript 的混合 ) 编写。下来我将分享我们更改的原因。

5、[小改动，大提升：最近 Go 标准库的一次优化](https://mp.weixin.qq.com/s/ipVRZOEJwaUXt2HE8kx2Lg)

Carlo Alberto Ferraris 提交了一个对`math/rand`库中的`lockedSource`优化的 pr(**CL#191538**),核心代码其实只有一行，却带来了相对的巨大的性能提升，让我们一起老看看这次的修改，学习一下代码的优化技巧，提高我们 Go 语言的底层优化经验。

6、[使用 Go 优化我们的接口](https://juejin.im/post/5e09e2d16fb9a016536ed0e5)

标题起的是有点大，不过还好本片文章主要也是使用 Go 来优化 HTTP 服务的，也算打个擦边球吧。

7、[golang实现依赖注入](https://mp.weixin.qq.com/s/CYT4v-s_ouAGSrUI_j4Ecw)

golang 中的依赖注入怎么实现，inject 包如何理解？

8、[微服务架构的 10个 最佳实践 ！](https://mp.weixin.qq.com/s/-N_PC6t1iMAu3OgEKGOg1g)

论如何正确实施微服务架构的10个技巧？

9、[100 行写一个 go 的协程池 (任务池)](https://segmentfault.com/a/1190000021468353)

本文正是针对上述情况而提供一种简单的解决方案, 编写一个协程池（任务池）来实现对 goroutine 的管控。

10、[Go之for-range排坑指南](http://blog.newbmiao.com/2020/01/03/dig101-golang-for-range.html)

golang常用的遍历方式，有两种： for 和 for-range。而for-range使用中有些坑常会遇到，今天我们一起来捋一捋。

11、[许式伟：Go 语言有机会登顶，桌面侧亟待突破](https://mp.weixin.qq.com/s/PFvl0CNEyN7uTebxPj5O9g)

这是 GVP 首位公布的超级大咖，这是一个所有中国 Gopher 无人不知的名字。无论是创建国内首批全面拥抱 Go 语言的七牛云，还是《 Go 语言编程》一书的编写，抑或是他独力发起并维护至今的 ECUG 社区，他的一切努力都在推动着 Go 语言的前进。

## 开源项目

1、[go-geom](https://github.com/twpayne/go-geom)

应用于地理空间应用的几何类型的实现。

2、[hexya](https://github.com/hexya-erp/hexya)

Go 实现的开源 ERP 和业务应用开发框架。

3、[shelby](https://github.com/athul/shelby)

用纯 Go 编写的轻巧、高性能的 shell 提示工具。

4、[jql](https://github.com/cube2222/jql)

Go 中具有 Lispy 语法的 Easy JSON 查询处理器。

5、[mgm](https://github.com/kamva/mgm)

Mongo Go 模型（mgm）是用于 Go 的快速，简单的 MongoDB ODM。

6、[tasks](https://github.com/madflojo/tasks)

易于使用的进程内调度程序，用于 Go 中的重复任务。

7、[koanf: 号称是 spf13/viper 的更干净，更轻便的替代品，具有更好的抽象性和可扩展性以及更少的依赖性](https://github.com/knadh/koanf)

轻量级的可扩展库，用于在 Go 应用程序中读取配置（文件，S3 等）。内置对 JSON，TOML，YAML，env，命令行的支持。

8、[waitabit](https://github.com/heartwilltell/waitabit)

一个用于处理系统中断的微型库。

9、[heksa](https://github.com/raspi/heksa)

CLI 十六进制 dumper，带有颜色。

10、 [rel](https://github.com/Fs02/rel)

clean architecture 的 sql 层。

11、[secrets](https://github.com/jarmo/secrets)

Go 实现的密码管理器。

## 资源&&工具

1、[创业公司更适合用 Go 语言，那大公司呢？](https://mp.weixin.qq.com/s/Pd4No6XVd2UNMoTfG9gUyg)

对于创业公司来说，人少资源少、产品又要求快速上线。选择合适的技术栈非常重要，本文就谈谈我们早期选择后端语言时的考量。

2、[阿里技术专家 Go 关键技术系列](https://mp.weixin.qq.com/s/tEW9nm89eaD7vJnXqxhuqQ)

从问题本身出发，不局限于 Go 语言，探讨服务器中常常遇到的问题，最后回到 Go 如何解决这些问题，为大家提供 Go 开发的关键技术指南。我们将以系列文章的形式推出《Go 开发的关键技术指南》，共有 4 篇文章。

3、[Golang IO Cookbook](https://github.com/jesseduffield/notes/wiki/Golang-IO-Cookbook)（英文）

![](imgs/issue024/go-io.png)

作者把学习的过程记录下来。

4、[程序员应该有的一些好习惯](https://github.com/Snailclimb/programmer-advancement)

养成一个学习习惯和编程习惯真的太重要了，一个好习惯的养成真的对后面的学习有很大帮助。说实话我自己当初在这方面吃了不少亏，很多比较好的习惯我也是后面自己才慢慢发现，所以这里想着重给大家说一下有哪些好的学习和编程习惯。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)、[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91) 和 [今日头条](https://www.toutiao.com/c/user/59903081459/#mid=1586087918877709)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
