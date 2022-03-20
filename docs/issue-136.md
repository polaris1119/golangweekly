# Go语言爱好者周刊：第 136 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue136/cover.jpeg)

题图：Go1.18 发布，一个重大的版本

## 刊首语

上期题目是关于取模运算符的。

以下代码输出什么？

```go
package main

import "fmt"

func main() {
	fmt.Println(1 % 2.0)
	fmt.Println(int(1) % 2.0)
}
```

A：1 1；B：1.0 1.0；C：编译不通过；D：1.0 1

正确答案 C，该题正确率 60%，还不错。这里有一点：% 运算只能用于 整数类型。1 % 2.0，两个操作数都是字面量常量，都是无类型的，这时会以 2.0 的 untype float constant 为准，1 隐式转为 untype float constant，所以编译错误。

而 int(1) % 2.0 中，2.0 是无类型的，int(1) 是 int，因此 2.0 会转为 int，因此能正常编译。

本期题目：以下代码输出什么？

```go
func main() {
  var m sync.Mutex
  fmt.Print("A, ")
  m.Lock()

  go func() {
    time.Sleep(200 * time.Millisecond)
    m.Unlock()
  }()

  m.Lock()
  fmt.Print("B ")
}
```

A：A，B；B：A，C：A，fatal error；D：fatal error...

## 资讯

1、[freecache 1.2.1 发布](https://github.com/coocood/freecache)

Go 缓存库，具有零 GC 开销和高并发性能。

2、[Mage 1.13.0 发布](https://magefile.org/)

类似 Make 的工具。

3、[cli 2.4 发布](https://github.com/urfave/cli)

快速构建 CLI APP。

4、[gopls v0.8.1 发布](https://github.com/golang/tools/releases/tag/gopls%2Fv0.8.1)

全面支持泛型。

## 文章

1、[WASM in Go 真的有前途？都出书了](https://mp.weixin.qq.com/s/P7B_H-0Qy7EEoaXTllULbQ)

今天发现有人写了一本书：《Wasm Cooking with Golang》，即使用 Go 开发 WASM 应用，该书是英文的。

2、[Go1.18 终于发布了：新特性学起来](https://mp.weixin.qq.com/s/tjHOd6jvGj7tpmf1K4wlYg)

Go 1.18 是一个大型版本，其中包括新功能、性能改进以及对该语言的最大更改。

3、[Go中fuzzing系统的原理分析](https://mp.weixin.qq.com/s/d8LslW77d8TiWzVkGoBGEw)

fuzzing 是 Go1.18 中的新特性。这篇是关于模糊测试原理的文章。

4、[Go 1.18 Release Note 抢鲜看](https://mp.weixin.qq.com/s/YLbD5brlXLvF0_P9FuUQng)

官方 Release Note 中文翻译版。

5、[使用 Gin 过程中的一些优化](https://mp.weixin.qq.com/s/fTFKKhRdMcJV9j0JOjxEyQ)

本文介绍 Gin 的一些知识点，如自定义 Response，中间件等。

## 开源项目

1、[go-clickhouse](https://github.com/uptrace/go-clickhouse)

clickhouse 的 Go 客户端，支持 Go1.18。

2、[sqlite](https://gitlab.com/cznic/sqlite)

纯 Go 实现的 SQLite 驱动。

3、[crane](https://github.com/gocrane/crane/)

首款企业成本优化的开源工具，腾讯出品。

4、[go-sql-spanner](https://github.com/googleapis/go-sql-spanner)

Google Cloud Spanner 的 database/sql 驱动。

5、[loggie](https://github.com/loggie-io/loggie)

一个基于 Golang 的轻量级、高性能、云原生日志采集 Agent 和中转处理 Aggregator，支持多 Pipeline 和组件热插拔。

6、[netgo](https://github.com/AletheiaWareLLC/netgo)

用于帮助 Web 服务器开发的工具和实用程序的集合。

## 资源&&工具

1、[go-gopher-model](https://github.com/justinribeiro/go-gopher-model)

Gopher 可打印的 3D 模型。

![](imgs/issue136/go-gopher-model.png)

2、[播客第 221 期](https://changelog.com/gotime/221)

精通 Go 语言。

3、[Fixtory](https://github.com/k-yomo/fixtory)

一个测试 fixture 工厂，利用泛型初始化类型安全的、灵活的 fixture。

4、[curlconverter](https://curlconverter.com/)

将 curl 命令转换为任意编程语言代码。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
