# Go语言爱好者周刊：第 70 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue070/cover.jpg)

题图：golangweekly

## 刊首语

一道问答题：以下代码可能有什么问题？如何改进？

```go
type Stats struct {
    mutex sync.Mutex

    counters map[string]int
}

func (s *Stats) Snapshot() map[string]int {
    s.mutex.Lock()
    defer s.mutex.Unlock()

    return s.counters
}

func (s *Stats) Add(name string, num int) {
    s.mutex.Lock()
    defer s.mutex.Unlock()
    s.counters[name] = num
}
```

欢迎留言讨论。

## 资讯

1、[Go 标准库性能测试，对比 Intel 和 苹果 M1 处理器](https://roland.zone/m1-go-benchmarks/)

想知道基于 Apple M1 的笔记本电脑与基于 Intel 的笔记本电脑的 Go 性能如何？这个测试可以看看。

2、[GoLand 2020.3 Beta 版发布](https://blog.jetbrains.com/go/2020/11/12/goland-2020-3-goes-beta/)

与“抢先体验计划”版本相比，该测试版非常稳定，但是请记住，这里和那里仍然可能存在一些粗糙的地方。

3、[GitHub 向开发着妥协，恢复 youtube-dl 项目](https://github.blog/2020-11-16-standing-up-for-developers-youtube-dl-is-back/)

下载用。

## 文章

1、[一起看看 Go1.14 的抢占调度](https://mp.weixin.qq.com/s/4_p45bHFn46T1nbWtPPz_Q)

抢占是调度器的重要部分，基于抢占调度器可以在各个协程中分配运行的时间。

2、[Go 最细节篇 — chan 为啥没有判断 close 的接口 ?](https://mp.weixin.qq.com/s/LJusfTvTgO4wC3uySl4Bhg)

相信大家初学 golang chan 的时候应该都遇到过 "send on closed channel" 的 panic 。

3、[通过这个 Runtime 统计信息可视化库学到了什么？](https://mp.weixin.qq.com/s/sRxKJa-zKo-Lb7KRKLhthA)

掌握系统运行状态，知道系统哪些地方可能存在问题，方便进行优化，这是一个实际系统必备的。裸奔，对系统一无所知，迟早是要出大事的。

4、[C++ 调用 Go 方法的字符串传递问题及解决方案](https://www.cnblogs.com/huaweiyun/p/13998446.html)

C++ 调用 Go 方法时，字符串参数的内存管理需要由 Go 侧进行深度值拷贝。

5、[聊聊 Go 和创业](https://mp.weixin.qq.com/s/tGrq-vdCrn6KU-3mgxbDpA)

PingCAP、七牛、掘金。。。

6、[Go 语言名人：除了 Rob Pike，很多人可能不知道他](https://mp.weixin.qq.com/s/kmcJRBahAl4gtPzZUvd5bg)

Russ Cox 是 Go Team Leader。

7、[在 Go 中恰到好处的内存对齐](https://mp.weixin.qq.com/s/8beAx_QiqPcQWz2dqe_IsA)

通过本文的介绍，可得知是由于不同类型导致需要进行字节对齐，以此保证内存的访问边界。

8、[Go 基准测试还可以这么搞？高级基准测试](https://mp.weixin.qq.com/s/bibdVJ-v68IgCF99fBtmKA)

有时你必须解决不同类型的问题。通常来说复杂的问题并不会只有单一的解决方案，但是解决方案的优劣取决于程序在运行时所要解决问题的子集。

9、[Go 语言之 pprof 的性能调优 “燥起来”](https://juejin.cn/post/6896453718527442951)

在计算机性能调试领域里，profiling 是指对应用程序的画像，画像就是应用程序使用 CPU 和内存的情况。 Go语言是一个对性能特别看重的语言，因此语言中自带了 profiling 的库，这篇文章就要讲解怎么在 golang 中做 profiling。

10、[Golang 协程并发的流水线模型](https://segmentfault.com/a/1190000038212342)

总结下 golang 协程并发常用的流水线模型。

11、[好未来开源框架 go-zero：如何用它进行 rest 开发？](https://mp.weixin.qq.com/s/Ug8emhEoWMIYBVFJCd5U7Q)

go-zero 是一个集成了各种工程实践的 web 和 rpc 框架，其中 rest 是 web 框架模块，基于 Go 语言原生的 http 包进行构建，是一个轻量的，高性能的，功能完整的，简单易用的 web 框架。

12、[为什么 Go 的泛型一拖再拖？](https://mp.weixin.qq.com/s/ftmuA9g7QPAwSwiswRuSuw)

据说 2022 年 2 月会有泛型。

13、[Java 微服务能像 Go 一样快吗？](https://mp.weixin.qq.com/s/e1yKNKc-C6LbdbWH3-qyPg)

留言比较有料。

## 开源项目

1、[gomponents](https://github.com/maragudk/gomponents)

Go 中的声明式视图组件，可以呈现为 HTML5。

2、[address](https://github.com/bojanz/address)

地址处理库，支持多国语言。

3、[peer-calls](https://github.com/peer-calls/peer-calls)

为使用 Go 和 TypeScript 编写的进行点对点视频通话。

4、[ebpf](https://github.com/cilium/ebpf)

eBPF 是一个纯 Go 库，提供用于加载，编译和调试 [eBPF](https://ebpf.io/) 程序的实用程序。它具有最小的外部依赖性，适合在长时间运行的进程中使用。

![](imgs/issue070/ebpf.png)

5、[h2go](https://github.com/jmrobles/h2go)

Apache H2 Go SQL Driver。

6、[statsview](https://github.com/go-echarts/statsview)

实时 Golang 运行时统计数据可视化分析器。

7、[k0s](https://github.com/k0sproject/k0s)

最小体积的发行版 k8s。

8、[gwda](https://github.com/electricbubble/gwda)

用 Golang 实现 appium/WebDriverAgent 的客户端库，使得 Gopher 也可以编写代码来控制 iOS iPadOS 设备的各种操作。

## 资源&&工具

1、[go-getter](https://github.com/hashicorp/go-getter)

可使用 URL 作为输入的主要形式从各种来源下载文件或目录。

2、[gdriver](https://github.com/mtojek/gdriver)

从 Google Drive 下大文件。

3、[油管视频](https://www.youtube.com/watch?v=VVqaFLev19Y)

深入 go build cache。

4、[适合 Go 新手学习的开源项目](https://juejin.cn/post/6896255508983283719)

看看有没有你需要的。

5、[rf](https://github.com/rsc/rf)

Go 重构工具，目前还是实验阶段。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
