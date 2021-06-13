# Go语言爱好者周刊：第 99 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue099/cover.png)

题图：端午节快乐

## 刊首语

上次的题目忘记做成投票形式了，不知道大家答题情况如何！题目比较简单：

```go
package main

import (
  "fmt"
)

func main() {
  a := make([]int, 20)
  a = []int{7, 8, 9, 10}
  b := a[15:16]
  fmt.Println(b)
}
```

A：[0]；B：panic；C：7；D：不清楚

正确答案是 B。a 被重新赋值为 `[]int{7, 8, 9, 10}`，之前 make 创建的 slice 跟 a 没有任何关系了。因此 a[15:16] 肯定会越界，所以 panic。

看看今天的题目，以下代码输出什么？

```go
package main

import "fmt"

func named() (n, _ int) {
	return 1, 2
}

func main() {
	fmt.Print(named())
}
```

A：1 0；B：1 2；C：不能编译；D：0 0

## 资讯

1、[Go1.17 Beta1 发布](https://mp.weixin.qq.com/s/2UeuFECPBoxh2nUDxohVNg)

看看有哪些新变化。

2、[gopls 0.7 发布](https://github.com/golang/tools/releases/tag/gopls/v0.7.0)

增加了 Postfix 完成，降低了内存使用。

3、[CodePerfect 95](https://codeperfect95.com/)

专为 Go 开发者打造的新 IDE。

4、[rqlite 6.0 发布](https://www.philipotoole.com/rqlite-6-0-0-building-for-the-future/)

分布式数据库设计的演变。

5、[vagrant 3.0 将使用 Go 重写](https://www.hashicorp.com/blog/toward-vagrant-3-0)

官方提到，为了支持其日益增长的生态系统和社区，计划开发 3.0 版本。

## 谁在招 Gopher

整理近期的 Go 职位。有招聘需求可以到「Go招聘」发布！ 

1、[Top云厂商招Gopher，你看你行吗？](https://mp.weixin.qq.com/s/GE05WZBz2SqlwswUhZaJ-Q)

2、[运维开发有点香哦，广州Gopher这下又有福了](https://mp.weixin.qq.com/s/g737LlDDxsEnQDTd6wgy5Q)

## 文章

1、[Go 调度器的任务窃取（Work-Stealing）](https://mp.weixin.qq.com/s/trBAi976eaaTDcSzpAqPkQ)

在 Go 中创建 Goroutine 既方便又快捷，然而 Go 在同一时间内最多在一个核上运行一个 Goroutine，因此需要一种方法来存放其他的 Goroutine，从而确保处理器（processor）负载均衡。

2、[字节跳动打造的轮子：Go 表单验证器](https://mp.weixin.qq.com/s/Oc90iCYyZGj5uDKhj8eGWw)

字节跳动开源的一个库：go-tagexpr。

3、[编写友好的Go命令行应用程序](https://mp.weixin.qq.com/s/qOhdWkIG5lZG6hV7QHIsaQ)

这是 Go 的一大应用场景。

4、[Go：内存管理与内存清理](https://mp.weixin.qq.com/s/gTk2UcVCv4a0xuP44oqZhg)

清理内存是一个过程，它能够让 Go 知道哪些内存段最近可用于分配。但是，它并不会使用将位置 0 的方式来清理内存。

5、[go test 的这些用途你都懂吗？](https://mp.weixin.qq.com/s/rt737Zdt30sYw9Fk-5n71A)

go test 命令提供了许多出色的功能，比如代码覆盖率，CPU 和 内存分析。要提供这些统计信息，Go 就需要一种方式来跟踪 CPU 使用率，或在代码覆盖中跟踪一个函数何时被用到。

6、[Go timer 是如何被调度的？](https://mp.weixin.qq.com/s/iseiQ20eIUR9i02fy1tFhg)

本篇文章剖析下 Go 定时器的相关内容。定时器不管是业务开发，还是基础架构开发，都是绕不过去的存在，由此可见定时器的重要程度。

## 开源项目

1、[lorca](https://github.com/zserge/lorca)

使用 Go + HTML5 建立跨平台现代桌面应用程序。

![image-20210613182357508](/Users/xuxinhua/opensource/golang/golangweekly/docs/imgs/issue099/lorca.png)

2、[connpool](https://github.com/buraksezer/connpool)

net.Conn 的连接池。

3、[geziyor](https://github.com/geziyor/geziyor)

快速的网络爬虫框架。支持 JS 渲染。

4、[go-hashlru](https://github.com/saurabh0719/go-hashlru)

简单的、线程安全的 LRU 实现。

5、[sso](https://github.com/buzzfeed/sso)

内部服务的 Go 单点登录方案。

6、[log](https://github.com/ermanimer/log)

Go 中简单、可定制、分级且高效的日志记录。

7、[godis](https://github.com/HDT3213/godis)

纯 Go 实现的 redis server。

8、[bramble](https://github.com/movio/bramble)

生产可用的 GraphQL 网关。

## 资源&&工具

1、[Worldwide](https://github.com/pokemium/Worldwide)

Go 编写的 Gameboy 颜色模拟器。

2、[dbmate](https://github.com/amacneil/dbmate)

轻量级数据库迁移框架。用 Go 实现的，但可以与任何语言编写的应用程序一起使用。支持 MySQL，Postgres，SQLite 和 Clickhouse。

3、[reqstress](https://github.com/utkusen/reqstress)

Go 实现的发送原始 HTTP 请求的基准测试和压力测试工具。

4、[一本花了2.5年写成的Go免费在线图书](https://mp.weixin.qq.com/s/Z97eT7FrqeJhygQwKvJaIw)

这是一本免费的 Go 语言在线图书：<https://www.practical-go-lessons.com/>。

5、[kuma](https://github.com/kumahq/kuma)

Go 实现的通用服务网格, CNCF sandbox 项目。

6、[libvault](https://github.com/canidam/libvault)

vault 的轻量级 Go 客户端。

7、[播客第 183 期](https://changelog.com/gotime/183)

以不寻常的方式使用 Go。

8、[GopherCon2021IsraelStaticAnalysisWorkshop](https://github.com/amit-davidson/GopherCon2021IsraelStaticAnalysisWorkshop)

Go 代码静态分析实战指南。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
