# Go语言爱好者周刊：第 160 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue160/cover.jpeg)

题图：来自 golangweekly

## 刊首语

有一位网友后台留言，遇到了一个面试题，这里放出来看看大家知道答案吗？以下代码输出什么？

```go
package main

import "fmt"

type temp struct{}

func (t *temp) Add(elem int) *temp {
	fmt.Println(elem)
	return &temp{}
}

func main() {
	tt := &temp{}
	defer tt.Add(1).Add(2)
	tt.Add(3)
}
```

A：1 3 2；B：1 2 3；C：3 1 2；D：3 2 1

上期的题目正确率比之前好，达到了 52%。一起看看。

以下代码输出什么？

```go
package main

func main() {
  m := make(map[int]int, 3)
  x := len(m)
  m[1] = m[1]
  y := len(m)
  println(x, y)
}
```

A：3 3；B：3 4；C：0 0；D：0 1

正确答案：D。这里关键是 m[1] = m[1]，右边的 m[1] 返回 0（map 中不存在某个 key 时，返回零值），因此最后 map 中有一个元素：1->0。

不过，这道题竟然有 35% 的人选 A，完全不知道 make 对 map 而言，第二个参数意味着什么。

## 资讯

1、[Go 向后兼容讨论](https://github.com/golang/go/discussions/55090)

rsc 发起的兼容性讨论。

2、[CodePerfect](https://codeperfect95.com/)

Go 高性能 IDE，使用 C++编写。不收收费的。

3、[chroma 2.3 发布](https://github.com/alecthomas/chroma)

纯 Go 实现的通用语法高亮库。

4、[Liftbridge 1.9 发布](https://github.com/liftbridge-io/liftbridge)

通过为 NATS 消息传递系统实施持久的流增强，Liftbridge 提供了轻量级的，容错的消息流。

5、[bud 0.2.5 发布](https://github.com/livebud/bud)

一个全栈框架。

6、[Buf 1.8 发布](https://github.com/bufbuild/buf)

一种新的 Protobuf 处理库。

7、[golang net/url 路径穿越漏洞](https://mp.weixin.qq.com/s/LZVYsjY5Wbg5m4JhOjtfoQ)

golang 的组件 net/url 实现了 URL 的解析处理和查询转义。

## 文章

1、[Go 每日一库之一个兼具单机和集群模式的轻量级限流器 throttled](https://mp.weixin.qq.com/s/BDL-rrBk_P3irluHda4brQ)

今天给大家推荐的工具是一个轻量级的限流器，star：1.2k。该工具实现了对资源的访问速率限制，资源可以是特定的 URL、用户或者任何自定义的形式。比如针对HTTP API接口。

2、[你信吗？Go 泛型竟然已经被迅速采用](https://mp.weixin.qq.com/s/FdCl0BZT_v_pjBZKcTUnoQ)

9 月 8 日，Go 语言社区发布 2022 年第二季度开发者调查报告，本次调研覆盖 5752 位受访开发者，主题涉及他们在使用 Go 1.18 全新功能特性（包括泛型、安全工具和工作区）时的真实感受。

3、[在 Go 中进行 Web UI 开发](http://www.myriptide.com/painless-web-ui-in-go/)

基于 [sunmao-ui](https://github.com/smartxworks/sunmao-ui/) 库。

4、[不得不知道的Golang之sync.Map解读！](https://mp.weixin.qq.com/s/NkSyv7iDSZsLhMUgAi-r4w)

本文结合源码，分析sync.Map的实现思路和原理，希望为更多感兴趣的开发者提供一些经验和帮助。

5、[Go：基于 Redis 实现的延迟队列详解](https://mp.weixin.qq.com/s/qFSzt32BjFW_Gl5OpI3lXA)

本文来自 Go 爱好者投稿，作者：finley。

6、[全面解读！Golang中泛型的使用](https://mp.weixin.qq.com/s/QBZ1dp0XIqMo24vVFYf1fA)

Golang在2022-03-15发布了V1.18正式版，里面包含了对泛型的支持，那么最新版本的泛型如何使用呢？有哪些坑呢？本文全面且详细的带你了解泛型在Golang中的使用。

## 开源项目

1、[go-sql-spanner](https://github.com/googleapis/go-sql-spanner)

Google Cloud Spanner 的 database/sql 驱动。

2、[seaweedfs](https://github.com/seaweedfs/seaweedfs)

一个快速的分布式存储。

3、[go-set](https://github.com/micnncim/go-set)

Set 的泛型实现。

4、[nset](https://github.com/bloeys/nset)

无符号整数的超快速和内存高效 Set 实现。

5、[gojq](https://github.com/itchyny/gojq)

jq 的纯 Go 实现。

6、[bun](https://github.com/uptrace/bun)

适用于PostgreSQL、MySQL、MSSQL和SQLite的SQL-first Go ORM。

## 资源&&工具

1、[toxiproxy](https://github.com/Shopify/toxiproxy)

模拟混乱网络条件的 TCP 代理。

2、[prolog](https://github.com/ichiban/prolog)

Go 的 prolog 引擎。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
