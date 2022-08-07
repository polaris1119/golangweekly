# Go语言爱好者周刊：第 154 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue154/cover.png)

题图：GoLand 2022.3 Roadmap

## 刊首语

先看下上周题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	a := []int{7, 8, 9}
	fmt.Println(a[real(2)])
}
```

A：0；B：7；C：9；D：不能编译

正确答案：C。正确率 42%，近一半的人选择了 D。

简单解析下。

real 是一个内建函数，虽然返回的类型是 FloatType，但这里返回的是常量（见 [Go 规范](https://docs.studygolang.com/ref/spec#Constants)）。这里要提醒大家，并非 slice 的索引可以是 float 类型。以下情况都是编译错误的：

```go
// 以下编译错误：invalid argument: index b (variable of type float32) must be integer
var b float32 = 2
fmt.Println(a[b])

// 以下编译错误：invalid argument: index real(b) (value of type float32) must be integer
var b complex64 = 2
fmt.Println(a[real(b)])
```

本期是一道关于 context 的题目。以下代码输出什么？

```go
package main

import (
	"context"
	"fmt"
)

func main() {
	ctx, _ := context.WithTimeout(context.Background(), 0)
	<-ctx.Done()
	fmt.Println("timed out")
}
```

A：timed out；B：panic；C：没有任何输出

## 资讯

1、[Go1.19 如期发布了](https://mp.weixin.qq.com/s/86fS370Ryp69u3HLSDmXpA)

在 Go1.18 发布 5 个月后，Go1.19 如期发布了。

2、[Yaegi 0.14.0 发布](https://github.com/traefik/yaegi)

一个优雅的 Go 解释器。可以用于其他应用程序中的脚本编写，交互式 shell 或快速原型制作。你可以将其用作 REPL 或将其嵌入到自己的应用中。

3、[progressbar 3.9 发布](https://github.com/schollz/progressbar)

适用于 Golang 应用程序的非常基础的线程安全进度条。

4、[muffet 2.6 发布](https://github.com/raviqqe/muffet)

Go 实现的快速网站链接检查器。

5、[加一个标准的 iterator 接口](https://github.com/golang/go/discussions/54245)

很多语言都有这样的能力，这个 issue 讨论给 Go 加一个 iterator。

6、[GoLand 2022.3 Roadmap](https://blog.jetbrains.com/go/2022/08/04/goland-roadmap-2022-3/)

GoLand 下一版本功能介绍。

## 文章

1、[关于Go并发编程，你不得不知的“左膀右臂”——并发与通道！](https://mp.weixin.qq.com/s/VBn3A9P52HTEttt1gVFxpA)

本文主要介绍 Goroutine 和 channel 的实现。

2、[7 年后，发现用 Go 实现 CockroachDB 是正确的选择](https://mp.weixin.qq.com/s/4UZLyETOjp-kdIDmG9z99w)

分享 CockroachDB 团队使用 Go 的体会。

3、[函数式编程在 Go 泛型下的实用性探索](https://mp.weixin.qq.com/s/wPLH4agJr-LozUsOqwN08g)

尝试用 Go 的泛型循序渐进地实现一些常见的函数式特性，从而探索 Go 泛型的优势和不足。

4、[2022 Go生态圈 rpc 框架 Benchmark](https://colobu.com/2022/07/31/2022-rpc-frameworks-benchmarks/)

在实际使用微服务框架的时候，大部分的性能瓶颈在于业务代码，而不是框架本身，所以重点优化业务代码也非常的重要。

## 开源项目

1、[maths](https://github.com/theriault/maths)

标准库 math 包中不包含的数学函数。

2、[dig](https://github.com/uber-go/dig)

基于反射的依赖注入工具包。

3、[nano](https://nanos.cloud/)

一个完全用 Go 实现的私有云 IaaS 平台。作者自荐。

4、[go-cryptobin](https://github.com/deatil/go-cryptobin)

Go 常用的加密解密库。作者自荐。

5、[dbpack](https://github.com/cectc/dbpack)

一个数据库代理，目标是解决业务开发中遇到的分布式事务问题，并提供读写分离、分库分表的解决方案。

## 资源&&工具

1、[govim](https://github.com/govim/govim)

用 Go 开发的 Vim8 插件。

2、[iftree](https://github.com/t1anz0ng/iftree)

可视化的 k8s 网络设备关系的命令行工具。

3、[veinmind-tools](https://github.com/chaitin/veinmind-tools)

一款容器安全开源工具集，支持检测容器镜像安全风险。作者自荐。

4、[lakeFS](https://github.com/treeverse/lakeFS)

将对象存储转换为类似 Git 的存储库。

5、[grm](https://studygolang.com/p/1123)

Redis Web 管理工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
