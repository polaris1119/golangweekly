# Go语言爱好者周刊：第 121 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue121/cover.png)

题图：Go 实现的模拟器。

## 刊首语

上期是一道关于不定参数的题目：

```go
package main

import (
	"fmt"
)

func f(a ...int) {
	fmt.Printf("%#v\n", a)
}

func main() {
	f()
}
```

A：[]int{}；B：[]int{nil}；C：panic；D：编译错误

正确答案是 B，但却有 58% 的用户选的 A。首先，a 的类型是 []int，调用 f 时，没有传递任何参数，因此相当于值是 nil，即 a 的类型是 `[]init`，值是 nil。而 fmt.Printf 的动词 `%#v` 会同时打印类型和值。所以结果是 B。

## 资讯

1、[imgproxy 3.0 发布](https://github.com/imgproxy/imgproxy)

一个 Go 语言写的图片代理网关，可以代理远程图片，并且提供格式转换和大小缩放功能。

2、[mongo-go-driver 1.8.0 发布](https://github.com/mongodb/mongo-go-driver)

Mongo 官方出品的驱动。

3、[终于，golang.org 官网被彻底抛弃了](https://mp.weixin.qq.com/s/erlYR1TFo0XbfLpRyfcWEQ)

全面使用 go.dev。

4、[tailscale v1.8.1 发布](https://github.com/tailscale/tailscale)

使用 WireGuard 和 2FA 最简单、最安全的方法。

## 文章

1、[Go泛型系列：slices 包讲解](https://mp.weixin.qq.com/s/z30xJqiweIROlSp1YgcIsQ)

通过学习 slices 包，掌握 Go 泛型的使用方法。

2、[Go：Recover 那些事](https://mp.weixin.qq.com/s/y6bLqjevvqlP3AEjTaztYw)

了解 recover 或者终止的过程，可以更好地理解一个会发生 panic 的程序的后果。

3、[Go 中的程序诊断](https://mp.weixin.qq.com/s/-Lgz_6AzQhUE90VFsX0jjQ)

本文面总结了可用的工具，并帮助 Go 用户针对他们的特定问题选择正确的工具。

4、[Go: Goroutine 泄漏检查器](https://mp.weixin.qq.com/s/eSa6B1Z1cnpUJ1Vn3bxhUA)

具有监控存活的 goroutine 数量功能的 APM (Application Performance Monitoring) 应用程序性能监控可以轻松查出 goroutine 泄漏。

5、[在 Go1.18 中实现一个简单的 Result 类型](https://mp.weixin.qq.com/s/MAKcuI6M8xcbP3bSkkimoQ)

Go 中的错误处理一直是争议最多的。Rust 是通过引入 Result 类型来解决此问题。

6、[Go错误集锦 | 字符串底层原理及常见错误](https://mp.weixin.qq.com/s/y2gSmjeUp6UdOs84iONOfw)

用图解的方式介绍了 string 的底层原理以及 rune 类型，同时介绍了 string 在使用中常见的错误。

## 开源项目

1、[tally](https://github.com/uber-go/tally)

Uber 开源的高性能、支持缓存的分层的统计信息收集接口。

2、[porto](https://github.com/jcchavezs/porto)

自动为包添加 vanity import path。

3、[ramsql](https://github.com/proullon/ramsql)

用于测试的内存 SQL 引擎。

4、[i18n](https://github.com/go-i18n/i18n)

包 i18n 为你的 Go 应用程序提供国际化和本地化。

5、[goconvey](https://github.com/smartystreets/goconvey)

在浏览器中进行测试。与 “go test” 集成，在 Go 中编写行为测试。

6、[goi](https://github.com/neguse/goi)

QOI 是一种无损图像格式，它提供了加速压缩和解压缩以及简单的实现。

7、[r2](https://github.com/aofei/r2)

Go 极简的 HTTP 请求路由辅助器。

## 资源&&工具

1、[sniffer](https://github.com/chenjiandongx/sniffer)

一个现代化的基于 BPF 的跨平台进程流量分析工具。

2、[nes](https://github.com/fogleman/nes)

NES 模拟器。

3、[new](https://github.com/carlmjohnson/new)

用于在 Go 1.18+ 中创建指向新对象指针的辅助函数。

4、[microservices](https://github.com/ebosas/microservices)

Go 微服务示例。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
