# Go语言爱好者周刊：第 142 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue142/cover.webp)

题图：51 劳动节快乐

## 刊首语

上期题目解析：

以下代码输出什么？

```go
package main

import "fmt"

func main() {
	fmt.Println(func() {} == func() {})
}
```

A：true；B：false；C：编译错误

正确答案：C。

在 Go 规范中有这么一句：

> Slice, map, and function values are not comparable. However, as a special case, a slice, map, or function value may be compared to the predeclared identifier `nil`. 

## 资讯

1、[Ebiten 2.3 发布](https://ebiten.org/documents/2.3.html)

2D 游戏库。

2、[GoLand 2022.2 Roadmap](https://blog.jetbrains.com/go/2022/04/28/goland-2022-2-roadmap/)

进一步增强对 Go 泛型的支持。

3、[Caddy 2.5.0 发布](https://github.com/caddyserver/caddy/releases/tag/v2.5.0)

快速的、跨平台 HTTP/2 Web 服务器。

4、[go-toml 2.0 发布](https://github.com/pelletier/go-toml)

TOML 格式的 Go 库。

## 文章

1、[为什么你不应该接受有 race 的 Go 代码](https://mp.weixin.qq.com/s/1LrULyUXIBJbGyiwmt2pvg)

在任何语言的并发编程场景中，都有 race 问题，现代语言为了解决 race 问题有两种思路。

2、[为 Go 项目自动生成 model](https://mp.weixin.qq.com/s/NiE-tgZHHtnEj1KT5tFWzg)

我们写业务的时候和 db 接触是少不了的，那么要生成 model 也是少不了的，如何自动生成 model，想着要给 hade 框架增加个这样的命令。

3、[通过 SingleFlight 模式学习 Go 并发编程](https://mp.weixin.qq.com/s/X0x-bYorzGuJ4R7DeB92pA)

最近接触到微服务框架go-zero，翻看了整个框架代码，发现结构清晰、代码简洁，所以决定阅读源码学习下，本次阅读的源码位于core/syncx/singleflight.go。

4、[如何封装安全的 go](https://mp.weixin.qq.com/s/UWakTncHOQxECiuH3T2HHA)

在业务代码开发过程中，我们会有很大概率使用go语言的goroutine来开启一个新的goroutine执行另外一段业务，或者开启多个goroutine来并行执行多个业务逻辑。

5、[一种优雅的Golang的库插件注册加载机制](https://mp.weixin.qq.com/s/VRl1I1NUU3Syw9rReUyHEQ)

如何增加框架的扩展性，可能多少都会想到“插件”机制，本质上是可以把第三方开发库快速融入项目的方法。本文介绍的就是这么一种方法。

6、[eBPF 入门与实践指南](https://mp.weixin.qq.com/s/gax8lokjYUbXBmj2RgcUVg)

本文将介绍 eBPF 的前世今生，并构建一个 eBPF 环境进行开发实践。

7、[深度解析 Go 泛型版排序比 sort 包更快吗？](https://mp.weixin.qq.com/s/xpxlgz1cP4x2-_ZpZysADQ)

为了将我们的讨论与 Go 标准库和实验存储库的混乱细节分离，并能够专注于更小、更简单的代码示例。

8、[Go 泛型的坏例子](https://colobu.com/2022/04/26/Crimes-with-Go-Generics/)

Go 1.18发布了第一版的Go泛型之后，大家开始对Go泛型进行了深入的研究，今天翻译的这一篇，是加拿大的Xe Iaso刚出炉的一篇有趣的文章，对Go泛型的应用做了一些探索。

## 开源项目

1、[btree](https://github.com/google/btree)

Google 的 B 树实现。

2、[go-cmp](https://github.com/google/go-cmp)

用于在测试中比较 Go 值的包，谷歌出品。

3、[ZenQ](https://github.com/alphadose/ZenQ)

比 Go 原生 channel 更快的、线程安全的队列，基于 Go1.18。

## 资源&&工具

1、[blush](https://github.com/arsham/blush)

带颜色的 grep。

2、[mergestat](https://github.com/mergestat/mergestat)

用 SQL 查询 git 仓库。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
