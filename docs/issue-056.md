# Go语言爱好者周刊：第 56 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于大部分人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](https://raw.githubusercontent.com/polaris1119/golangweekly/master/docs/imgs/issue056/cover.png)

题图：中文 LeetCode Go 刷题指南

## 资讯

1、[Go 1.15 正式版发布](https://mp.weixin.qq.com/s/AdB5jxMj6fBQBY0KMbazVQ)

看看都有哪些值得关注的变化。

2、[mpb v5.3.0 发布](https://github.com/vbauerster/mpb)

在终端为 Go 命令行应用程序显示进度条。5.3.0 增加装饰器。

![](https://raw.githubusercontent.com/polaris1119/golangweekly/master/docs/imgs/issue056/mpb.jpg)

3、[Excelize 发布 2.3.0 版本， Go 语言 Excel 文档基础库](https://studygolang.com/articles/30181)

Go 语言编写的用于操作 Office Excel 文档基础库，基于 ECMA-376，ISO/IEC 29500 国际标准。可以使用它来读取、写入由 Microsoft Excel™ 2007 及以上版本创建的电子表格文档。支持 XLSX / XLSM / XLTM 等多种文档格式，高度兼容带有样式、图片(表)、透视表、切片器等复杂组件的文档，并提供流式读写 API，用于处理包含大规模数据的工作簿。

4、[Go 提案](https://github.com/golang/go/issues/40724)

Go 1.16 将基于栈的函数调用约定迁移为基于寄存器的函数调用约定（calling convention）。

## 文章

1、[面试题：Go 1.15 中 var i interface{} = 3 会有额外堆内存分配吗？](https://mp.weixin.qq.com/s/1r0nt8nA3foDRRrbRp4omg)

题目是这样的：

```go
var in int = 3
// 以下有额外内存分配吗？
var i interface{} = in
```

2、[学习 Rob Pike 的 6 条编程原则](https://mp.weixin.qq.com/s/thStKO5VMjiDQomcZquaAg)

过早的优化是万恶之源、拿不准就穷举等。

3、[Prometheus 不完全避坑指南](https://mp.weixin.qq.com/s/fDWcR99AWoKHgKRMwGom9w)

一个开源监控系统，它本身已经成为了云原生中指标监控的事实标准，几乎所有 k8s 的核心组件以及其它云原生系统都以 Prometheus 的指标格式输出自己的运行时监控信息。

4、[在 Go 语言中管理 Concurrency 的三种方式](https://mp.weixin.qq.com/s/J7vTfAjxSXq0UUxT6T5WBg)

相信大家踏入 Go 语言的世界，肯定是被强大的并发（Concurrency）所吸引，Go 语言用最简单的关键字`go`就可以将任务丢到后台处理，但是开发者怎么有效率的控制并发，这是入门 Go 语言必学的技能，本章会介绍几种方式来带大家认识并发，而这三种方式分别对应到三个不同的名词：WaitGroup，Channel，及 Context。

5、[Go 的两级线程模型](https://juejin.im/post/6859312340630929421)

再复习一下也挺好。

6、[优化 Golang 服务来减少 40% 以上的 CPU](https://mp.weixin.qq.com/s/wspSwZEm6oQoOOQCeIcFGw)

通过对 Go 解析服务进行性能测试，我们能够查明有问题的地方，更好的理解我们的服务并且确定在哪里（如果有的话）投资时间进行改进。

7、[Go 每日一库之 fuckdb Lite — 帮助你更快地生成go struct代码](https://mp.weixin.qq.com/s/zNaItNb7zUb9I379AbU8Qw)

名字很给力！

8、[Nodejs 与 Golang 的比较：Web 开发人员选择哪个最佳？](https://mp.weixin.qq.com/s/wRXmohbGeyL3Y7ARra8moA)

在本文，我们将讨论 NodeJS 和 Golang 这两种广为人知的语言，开发人员可以选择这两种语言开发出色的软件和移动应用程序。

9、[前缀树算法实现路由匹配原理解析：Go 实现](https://mp.weixin.qq.com/s/4UNLWbKvYL-Wt36FjQylVg)

路由功能是 web 框架中一个很重要的功能，它将不同的请求转发给不同的函数(handler)处理，很容易能想到，我们可以用一个字典保存它们之间的对应关系，字典的 key 存放 path，value 存放 handler。当一个请求过来后，使用 **routers.get(path, None)** 就可以找到对应的 handler。

10、[go trace 剖析 go1.14 异步抢占式调度](https://mp.weixin.qq.com/s/Wp15aOLeYhZYla275TzISw)

go 1.14 版本带来了一个非常重要的特性：异步抢占的调度模式。之前我们通过解释一个简单的协程调度原理（），并且实现协程调度例子都提到了一个点：协程是用户态实现的自我调度单元，每个协程都是君子才能维护和谐的调度秩序，如果出现了流氓（占着 cpu 不放的协程）你是无可奈何的。

## 开源项目

1、[Dynamo：富有表现力的 DynamoDB 库](https://github.com/guregu/dynamo)

dynamo 是 Go 的富有表现力的 DynamoDB 客户端，其 API 受 mgo 启发很大。dynamo 与官方的 AWS 开发工具包集成。

2、[oscar](https://github.com/chenjiandongx/oscar)

下一代构建工具 for nothing。是的，这是一个玩笑/轻松的项目！您可以使用它来使自己看起来像在不工作时一样高效。

3、[httpmock](https://github.com/jarcoal/httpmock)

轻松模拟来自外部资源的 http 响应。

4、[gofmtmd](https://github.com/po3rin/gofmtmd)

将 markdown 中的 go 代码块进行格式化。

![](https://raw.githubusercontent.com/polaris1119/golangweekly/master/docs/imgs/issue056/gofmtmd.png)

还提供了 Vim 插件。

5、[kowl](https://github.com/cloudhut/kowl)

kafka WebUI。

6、[wrapcheck](https://github.com/tomarrell/wrapcheck)

一个 Go linter 检查器，检查是外部错误是否 Wrap 了。

7、[gopdf](https://github.com/tiechui1994/gopdf)

pdf 文件生成库。支持 Unicode 字符 (包括中文, 日语, 朝鲜语, 等等)。

8、 [go-quake2](https://github.com/samuelyuan/go-quake2)

Go 实现的 Quake 2 级别的渲染器。

## 资源&&工具

1、[Go 下载管理器](https://github.com/usmanhalalit/go-download-manager)

支持并发下载。

2、[project52](https://github.com/kkdai/project52)

52 周，52 个 Go 项目，厉害！

3、[Prometheus-Basics](https://github.com/yolossn/Prometheus-Basics)

Prometheus 基础教程。

4、[LeetCode Cookbook](https://books.halfrost.com/leetcode)

Go 刷 LeetCode。

5、[播客第 142 期](https://changelog.com/gotime/142)

Go 与基础设施。

6、[code-playground](https://github.com/Trendyol/code-playground)

CodePlayground 是用于 Go 和 Rust 语言的 Playground 工具，支持 Vim、VS Code 和 Sublime。

7、[interface-type-check](https://github.com/siadat/interface-type-check)

空接口的类型检查。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](https://raw.githubusercontent.com/polaris1119/golangweekly/master/docs/imgs/wechat.png)

