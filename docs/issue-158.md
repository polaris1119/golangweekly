# Go语言爱好者周刊：第 158 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue158/cover.jpeg)

题图：2D 游戏开发库

## 刊首语

本期题目比较简单。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	var s fmt.Stringer
	s = "s"
	fmt.Println(s)
}
```

A：s；B：编译错误；C：运行时 panic

上期的题目是关于类型断言的，正确率很低，只有 18%。

```go
const X = 7.0
var x interface{} = X

if y, ok := x.(int); ok {
  fmt.Println(y)
} else {
  fmt.Println(int(y))
}
```

A：7；B：7.0；C：0；D：编译错误

正确答案是 C，即 输出 0。首先，X 是无类型常量，当赋值给需要类型的变量时，因为 7.0 的默认类型是 float64，因此，`x.(int)` 的断言是失败的，断言失败，y 的值就是 int 类型的默认值，即 0。实际上，int(y) 这里的类型转换是必须要的，直接 fmt.Println(y) 结果是一样的。

## 资讯

1、[Ebitengine 2.4](https://ebiten.org/documents/2.4.html)

Go 的 2D 游戏库。

2、[haxmap 0.3 发布](https://github.com/alphadose/haxmap)

最快、内存效率最高的 golang 并发 hashmap。

3、[progressbar 3.10 发布](https://github.com/schollz/progressbar)

适用于 Golang 应用程序的非常基础的线程安全进度条。

4、[pocketbase 0.6 发布](https://github.com/pocketbase/pocketbase)

单个文件的 Go 开源实时后端。

5、[hertz 0.3 发布](https://github.com/cloudwego/hertz)

一个 Golang 微服务 HTTP 框架。

6、[Visual Studio Code 1.71 发布](https://mp.weixin.qq.com/s/yCrx3ysp5Hl31QdSSr3TxQ)

更新的内容不少。

## 文章

1、[3种方式！Go Error处理最佳实践](https://mp.weixin.qq.com/s/Zb5zGOy_mdalUQ_Qy0HngQ)

错误处理一直以一是编程必需要面对的问题，错误处理如果做的好的话，代码的稳定性会很好。不同的语言有不同的出现处理的方式。Go语言也一样，在本篇文章中，我们来讨论一下Go语言的错误处理方式。

2、[必撸系列！Go另外几个黑魔法技巧汇总](https://mp.weixin.qq.com/s/3RZpwI88lKUdDbEtsqXF4g)

最近一段时间，笔者重新梳理了一下go知识点，并深入地看看了它的源码，在实践中又有了新的沉淀，于是写下这篇文章和大家分享一下。

3、[Go 每日一库之一个让终端内容彩色化的工具：Color](https://mp.weixin.qq.com/s/Kx5mubQ4yYuAGfqc6TUgzg)

在命令行的文本输出中，你经常见到的是不是都是黑色背景，白色文字。今天给大家推荐一款能让输出的文本带上颜色的工具：color

4、[Go：熔断原理分析与源码解读](https://mp.weixin.qq.com/s/r07STu712MkyZ0mhwCRNug)

注意熔断是一种有损的机制，当熔断后可能需要一些降级的策略进行配合。

5、[图文结合！Redis延迟队列golang高效实践](https://mp.weixin.qq.com/s/r3ayFm_7kD07AAShcQF8xA)

本文主要讲述如何使用golang基于Redis实现延迟消息队列组件。希望对有需求的同学有所帮助。

6、[Uber 基于 gRPC 上的下一代推送平台](https://www.uber.com/en-GB/blog/ubers-next-gen-push-platform-on-grpc/)

这篇文章介绍如何将协议从服务器发送事件（HTTP1.1）更改为基于 gRPC 的双向流（QUIC/HTTP3），我们面临的挑战，最终结果，以及一些关键学习成果。

## 开源项目

1、[wazero](https://github.com/tetratelabs/wazero)

零依赖的 WebAssembly 运行时库。

2、[hanko](https://github.com/teamhanko/hanko)

密钥优先的身份验证。

3、[go-plugin](https://github.com/knqyf263/go-plugin)

基于 WebAssembly 的 Go 插件系统。

4、[caps](https://github.com/chanced/caps)

用于 Go 的大小写转换库。

5、[flowprocess](https://gitee.com/mqyqingkong/flowprocess)

一个轻量的流处理引擎，可以高效地进行数据处理。

## 资源&&工具

1、[goose](https://github.com/pressly/goose)

数据库迁移工具。

2、[rmq](https://github.com/adjust/rmq)

基于 Redis 的消息队列系统。

3、[gopher-pattern](https://github.com/Acyony/gopher-pattern)

如何 DIY 一个 Gopher 吉祥物玩偶。

4、[xmind](https://github.com/jan-bar/xmind)

基于 Go 语言的 xmind 接口。作者自荐。

5、[rainbond](https://github.com/goodrain/rainbond)

Rainbond 云原生应用管理平台。读者推荐。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
