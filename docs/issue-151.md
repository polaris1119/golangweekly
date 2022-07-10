# Go语言爱好者周刊：第 151 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue151/cover.jpeg)

题图：土拨鼠逛图书馆

## 刊首语

上周因为忙，没来得及出周刊，有人催，这感觉还是挺好，表明有人一直在看，这是更新地动力。

上期的一道题目，正确率 36%。一起看看：

以下代码输出什么？

```go
package main

import "fmt"

func main() {
	fmt.Println(09)
}
```

A：09；B：9；C：11；D：编译不通过

正确答案：D。0 开头，表明是八进制，但八进制最大的数字是 7，因此编译不通过。

一起看看本期题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	m := map[string]int{"uno": 1}
	p := &m["uno"]
	*p = 2
	fmt.Println(m["uno"])
}
```

A：1；B：2；C：panic；D：不能编译

## 资讯

1、[ElasticSearch Go 8.3 发布](https://github.com/elastic/go-elasticsearch)

ElasticSearch Go 8.3 官方客户端发布。

2、[traefik 2.8 发布](https://github.com/traefik/traefik)

HTTP 反向代理和负载均衡器。

3、[FerretDB 0.4 发布](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。之前叫 MangoDB，容易被人理解为碰瓷。

4、[vitess 14.0 发布](https://github.com/vitessio/vitess)

用于 MySQL 水平扩展的集群系统。

5、[fasthttp 1.38.0 发布](https://github.com/valyala/fasthttp)

一个 HTTP 库。

6、[go-version 1.6 发布](https://github.com/hashicorp/go-version)

版本号解析和验证库。

7、[delve 1.9 发布](https://github.com/go-delve/delve)

Go 调试器。

8、[GoLand 2022.2 Beta 发布](https://blog.jetbrains.com/go/2022/07/07/goland-2022-2-goes-beta/)

GoLand 2022.2 已达到测试里程碑！

## 文章

1、[各大主流编程语言性能PK，结果出乎意料](https://mp.weixin.qq.com/s/yVr5NZxDecJ7GEC9mWmtPQ)

什么编程语言速度最快？

2、[Go 每日一库之 hystrix-go](https://mp.weixin.qq.com/s/VE1iZfgh9odCnfBXnmugKw)

Hystrix 是 Netflix 的一个非常棒的项目，这是 Go 版本。

3、[在Go中如何正确重试请求](https://mp.weixin.qq.com/s/GKggVplX_ZzoXJDuWf5ctA)

我们平时在开发中肯定避不开的一个问题是如何在不可靠的网络服务中实现可靠的网络通信，其中 http 请求重试是经常用的技术。

4、[揭秘！用标准Go语言能写脚本吗？](https://mp.weixin.qq.com/s/zXNPWl80AkNZ_IwqQyL6EA)

作为编译型语言的特性，也让Go在多协程环境下的性能有不俗的表现。但脚本语言则几乎都是解释型语言，那么Go怎么就和脚本扯上关系了？

5、[gRPC如何在Golang和PHP中进行实战？7步教你上手！](https://mp.weixin.qq.com/s/yOmQ1AQEi6qM8yFECHWRDQ)

本文主要实战演示一下gRPC的几种调用通讯模式（普通、客户端流、服务端流、双向流）以及和PHP客户端的联通调用。

6、[Golang原生json可以一库走天下吗？](https://mp.weixin.qq.com/s/YaQ4MH9wpy-XfAS9EvYkpg)

Go的“玩家”们看到这个题目可能会很疑惑。

7、[Go究竟是否为空切片分配了底层数组](https://mp.weixin.qq.com/s/LD2MOnr-lvgBdzaS2eOxZw)

切片是Go语言中的一个重要的语法元素，也是日常Go开发中使用最为频繁的语法元素。

8、[Go 每日一库：tproxy 是个啥？](https://mp.weixin.qq.com/s/_iZsFPaUk2RzHR_A2u-AdQ)

复杂网络情况的处理从来都是后端开发的重点和难点之一。

9、[Wasm 的主力，你觉得是谁？Go？Rust？](https://mp.weixin.qq.com/s/rCrLL48nqrzA2--Dg2N_pQ)

最新的一份《The State of WebAssembly 2022》调查报告已出炉。

10、[为什么国内做不出 JetBrains 那样的产品？](https://mp.weixin.qq.com/s/swpgU1V0Oh6DQnKiQbd9Hg)

分享一个很有意思的回答。

## 开源项目

1、[go-nanoid](https://github.com/jaevor/go-nanoid)

一个小巧、安全、URL 友好的字符串 ID 生成器。

2、[go-metrics](https://github.com/rcrowley/go-metrics)

Metrics 库的 Go 端口。

3、[erpc](https://github.com/andeya/erpc)

高效、灵活、易于使用的 RPC 框架。

![](imgs/issue151/erpc.png)

4、[do](https://github.com/samber/do)

基于 Go1.18 泛型的依赖注入工具包。

5、[slacker](https://github.com/shomali11/slacker)

Slack Bot 框架。

6、[pocketbase](https://github.com/pocketbase/pocketbase)

单个文件的 Go 开源实时后端。

7、[scriggo](https://github.com/open2b/scriggo)

强大的模板引擎和 Go 嵌入式解释器。

8、[hptx](https://github.com/CECTC/hptx)

Go 语言分布式事务框架。（网友 dk-lockdown 推荐）

9、[sqlw](https://github.com/lesismal/sqlw)

最简单易用的 RawSql 库。（网友 lesismal 推荐）

## 资源&&工具

1、[理解 K8S](https://www.linode.com/content/kubernetes-guide/)

免费电子书（英文）。

2、[socks5lb](https://github.com/mingcheng/socks5lb)

socks5 透明代理和负载均衡代理。

3、[go-ldap-admin](https://github.com/eryajf/go-ldap-admin)

基于 Go+Vue 实现的 openLDAP 后台管理项目。(网友 eryajf 推荐)

4、[rdb](https://github.com/HDT3213/rdb)

Redis RDB 文件编解码器。（网友 HDT3213 推荐）

5、[lancet](https://github.com/duke-git/lancet)

一个全面、高效、可复用的 Go 语言工具函数库。（网友 thecodeworks 推荐）

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
