# Go语言爱好者周刊：第 171 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue171/cover.jpeg)

题图：回顾 2022 年的 Go Gamedev，<https://ebitengine.org/en/blog/2022.html>。

## 刊首语

上期的题目有提示 math.Inf 含义，正确率 55%，正确答案是 A。

以下代码输出什么？

```go
package main

import (
    "fmt"
    "math"
)

func main() {
    // Inf returns positive infinity if sign >= 0, negative infinity if sign < 0.
    x := math.Inf(1)
    switch {
    case x < 0, x > 0:
        fmt.Println(x)
    case x == 0:
        fmt.Println("zero")
    default:
        fmt.Println("something else")
    }
}
```

A：+Inf； B：zero； C：something else； D：doesn't compile

本期不出题目了，不少人可能身体不适，好好休息，多喝水！

## 资讯

1、[Go 1.19.4 发布，同时 Go1.20 RC 也发布了](https://mp.weixin.qq.com/s/qolkg2mjlg7Q2IH6EHmkDg)

同时发布的还有 1.18.9。

2、[hertz 0.4.2 发布](https://github.com/cloudwego/hertz)

一个 Golang 微服务 HTTP 框架。

3、[dragonboat 3.3.6 发布](https://github.com/lni/dragonboat)

一个高性能纯 Go 语言实现的多组 Raft 共识算法库。

4、[Task 3.19.0 发布](https://github.com/go-task/task/releases/tag/v3.19.0)

任务运行器，使用 Go 语言编写。类似 GNU Make，目标是比它更简单和易于使用。

5、[FerretDB v0.7.0](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。之前叫 MangoDB，容易被人理解为碰瓷。

6、[go-sql-driver/mysql 1.7 发布](https://github.com/go-sql-driver/mysql/releases/tag/v1.7.0)

Go1.12 不再支持。

7、[Kubernetes v1.26 发布](https://kubernetes.io/blog/2022/12/09/kubernetes-v1-26-release/)

主题是*Electrifying*。

## 文章

1、[这个好：Go 1.20 将支持 Wrapping 多个 errors](https://mp.weixin.qq.com/s/1AzlUk-UH7gUs_JumwxfYw)

该项提案对错误处理进行了优化，与 Go 1.13 为错误处理提供的新功能有关：Error Wrapping。引入 Error Wrapping 后，Go 同时为 errors 包添加了 3 个工具函数，分别是 Unwrap 、 Is 和 As 。

2、[Go 1.20 快讯：新特性有哪些？一文了解](https://mp.weixin.qq.com/s/0jf8rNuaULak-ydrkZMZbQ)

提前看看究竟会有哪些新特性加入 Go。

3、[Go streaming 库的性能比较](https://macias.info/entry/202212020000_go_streams.md)

随着 Generics to Go 1.18 的到来，Go 出现了一种新的编程模型：函数式流处理。这篇文章评估了一些当前提供此类功能的库，并比较了单线程流中实现的性能。

4、[sonic ：基于 JIT 技术的开源全场景高性能 JSON 库](https://zhuanlan.zhihu.com/p/461772555)

sonic 是字节跳动开源的一款 Golang JSON 库，基于即时编译（Just-In-Time Compilation）与向量化编程（Single Instruction Multiple Data）技术，大幅提升了 Go 程序的 JSON 编解码性能。同时结合 lazy-load 设计思想，它也为不同业务场景打造了一套全面高效的 API。

5、[Go1.20 新特性：切片转数组](https://mp.weixin.qq.com/s/ZhvSrju3Z99TC_-8xMoAMw)

Go1.20 正式版本还没有发布，官方计划 2023 年 2 月份发布。不过，Go1.20rc 已经在 12 月 8 号发布了，一起来尝鲜。

## 开源项目

1、[git-bug](https://github.com/MichaelMure/git-bug)

分布式的、离线的、嵌入 Git 中的 bug 追踪器。

2、[valgo](https://github.com/cohesivestack/valgo)

类型安全、表现力丰富、可扩展的 Go 验证器包。

3、[airplanes](https://github.com/m110/airplanes)

Go 实现的射击游戏。

## 资源&&工具

1、[marmot](https://github.com/maxpert/marmot)

基于 NATS 构建的分布式 SQLite 复制器。

2、[terraform-exec](https://github.com/hashicorp/terraform-exec)

Go 实现的 Terraform CLI 工具。

3、[go-coffeeshop](https://github.com/thangchung/go-coffeeshop)

用 Go 构建的一个实用的事件驱动的微服务演示：使用 Nomad、Consul Connect、Vault和Terraform。

4、[Go Time 第 258 期](https://changelog.com/gotime/258)

TDD 还是 not TDD？

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
