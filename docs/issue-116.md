# Go语言爱好者周刊：第 116 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue116/cover.png)

题图：来自网络

## 刊首语

这次来一道简单的题目：

```go
package main

import (
	"fmt"
)

func main() {
	c := make(chan int, 5)
	c <- 5
	c <- 6
	close(c)
	fmt.Println(<-c)
}
```

A：panic；B：5；C：6；D：编译错误

## 资讯

1、[Kratos 2.1 发布](https://github.com/go-kratos/kratos)

一个国产的 Go 微服务框架。

2、[Go 重视兼容性是认真的：泛型得慢慢加](https://mp.weixin.qq.com/s/ADCFQEM7yIWvZyv2loOWEg)

Rob Pike 发话。

3、[怎么回事？Go 标准库 sync 包中竟然包含一个 porn 网址](https://mp.weixin.qq.com/s/829i4G30WzAt_gCQHbAFiA)

有点无语。。。

## 文章

1、[优化Go的内存使用，避免用Rust重写](https://mp.weixin.qq.com/s/7m7npdj2vHWtww4-jrgvmA)

今天分享一篇文章，更多是和 Go 相关。不过从标题可以看到，某些时候，Go 需要较好的优化，才能避免需要使用 Rust 重写。

2、[使用 Go Modules（模块）进行依赖项迁移](https://mp.weixin.qq.com/s/WM_yPfRnaPjGXhhngaCZKA)

本文主要对项目转换为模块的工具和技术进行讲解叙述。

3、[Golang 无限开启 Goroutine？该如何限定 Goroutine 数量？](https://juejin.cn/post/7017286487502766093) 

如果不控制 Goroutine 的数量会出什么问题？

4、[GRPC: 如何让 gRPC 提供 Swagger UI?](https://juejin.cn/post/7017396592428711972) 

本文将介绍如何让一个 gRPC 服务之上提供 Swagger UI。

5、[使用 goland 进行 go 源码调试](https://juejin.cn/post/7016875587792797733)

本文中调试的 go 源码为 1.14.12 版本，本文介绍的调试方法与 go 版本没有关系。

6、[网工人的辛酸转Go历程](https://mp.weixin.qq.com/s/GnUcjNF8CIxIGkTnCLXaZw)

分享一下一位群友从网工到Gopher的面试经历，希望大家能从中有所收获。

7、[etcd:从应用场景到实现原理的全方位解读](https://mp.weixin.qq.com/s/98YyK9AW4__z-zphoKIf1Q)

本文将从 etcd 的应用场景开始，深入解读 etcd 的实现方式，以供开发者们更为充分地享用 etcd 所带来的便利。

## 开源项目

1、[decimal](https://github.com/shopspring/decimal)

Go 中的任意精度定点十进制数。

2、[truthy](https://github.com/carlmjohnson/truthy)

使用 Go 泛型提供了真值条件测试。

3、[broadcast](https://github.com/teivah/broadcast)

Go 中的通知广播。

4、[tile38](https://github.com/tidwall/tile38)

实时地理空间和地理围栏数据库。

5、[goic](https://github.com/adhocore/goic)

Golang 的 OpenID 连接客户端库。

6、[gojtp](https://github.com/ankur-anand/gojtp)

Go 中的高性能、零分配、动态 JSON 威胁防护。

7、[igop](https://github.com/goplus/igop)

Go+脚本版: Go+解释器项目开源。

## 资源&&工具

1、[hostsfile](https://github.com/kevinburke/hostsfile)

用于处理 /etc/hosts 文件的工具。

2、[depstat](https://github.com/kubernetes-sigs/depstat)

Kubernetes 的 Go module 依赖更新分析器，大型 Go 项目都适用。

3、[ansisvg](https://github.com/wader/ansisvg)

基于 ANSI 输出转换为 SVG 图片。

![](imgs/issue116/ansisvg.png)

4、[ddosify](https://github.com/ddosify/ddosify)

Go 实现的高性能压测工具。

5、[chatbot](https://github.com/kevwan/chatbot)

一个快速响应的聊天机器人。

6、[播客第 198 期](https://changelog.com/gotime/198)

Go 团队是如何运转的。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
