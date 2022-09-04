# Go语言爱好者周刊：第 157 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue157/cover.png)

题图：《100 Go Mistakes and How to Avoid Them》 正式发布

## 刊首语

本期的题目是关于类型断言的。以下代码输出什么？

```go
const X = 7.0
var x interface{} = X

if y, ok := x.(int); ok {
  fmt.Println(y)
} else {
  fmt.Println(int(y))
}
```

A：7；B：7.0；C：0；D：编译错误

上期题目正确率不到 50%，只有 44%，一起看看。以下代码输出什么？

```go
package main

import (
	"fmt"
	"net/url"
)

// 其中 url.Values 的定义：type Values map[string][]string
type Query struct {
	url.Values
}

func main() {
	q := Query{}
	q.Values["name"] = []string{"polarisxu"}
	fmt.Println(q.Get("name"))
}
```

A：panic；B：编译错误；C：polarisxu

Url.Values 是 map，没有进行初始化，可以在 `q := Query{}` 之后加上这么一句看输出结果：

```go
// 输出：url.Values(nil)
fmt.Printf("%#v\n", q.Values)
```

nil 的 map 自然不能设置值，所以 panic。

## 资讯

1、[excelize 2.6.1 发布](https://github.com/qax-os/excelize)

Go 语言编写的用于操作 Office Excel 文档基础库，基于 ECMA-376，ISO/IEC 29500 国际标准。

2、[go-vcr 3.1 发布](https://github.com/dnaeon/go-vcr)

记录并重放 HTTP 交互以获得快速，确定性和准确的测试。

3、[bloom 3.3 发布](https://github.com/bits-and-blooms/bloom)

Go 的 Bloom filters 实现。

4、[ElasticSearch Go 8.4 发布](https://github.com/elastic/go-elasticsearch)

ElasticSearch Go 8.4 官方客户端发布。

5、[clickhouse-go 2.3 发布](https://github.com/ClickHouse/clickhouse-go)

clickhouse 官方 go 客户端 API  库。

6、[Go 性能优化](https://github.com/golang/go/commit/cf26fbb1f6d9644f447342f42d2dddcbe9ceda61)

strconv.ParseXXX 系列函数性能将提升 15% 以上。

7、[Kubernetes 1.25 发布](https://kubernetes.io/blog/2022/08/23/kubernetes-v1-25-release/)

Ephemeral Containers 进入 stable。

## 文章

1、[Go语言从0到1实现最简单的数据库！](https://mp.weixin.qq.com/s/VFS4TWi3OpeAegScZ4cJRw)

后台开发对于数据库操作是必不可少的事情，了解数据库原理对于平常的工作的内功积累还是很有帮助的，这里实现一个最简单的数据库加深自己对数据库的理解。

2、[Go：负载均衡原理分析与源码解读](https://mp.weixin.qq.com/s/5Xskm1gZmaOw0jatrJOMOA)

我们一起学习下和 Resolver 关系密切的 Balancer 的相关内容。这里说的负载均衡主要指数据中心内的负载均衡，即 RPC 间的负载均衡。

[贝壳Go实现的多云对接存储网关建设](https://mp.weixin.qq.com/s/ZnIP-Lk2GICffQR_swnGkQ)

贝壳存储服务通过S3协议向业务方提供文件、图片、音视频的存储及下载。

4、[Rust 与 Go 可以互操作？](https://mp.weixin.qq.com/s/7A6VCvuv8umUlOUzB2uHfA)

Go 和 Rust 是近几年比较受关注的新编程语言，两者没有直接的竞争关系，更多是互补。如果你想使用两者的优势并喜欢互操作，本文也许对你有帮助！

5、[看Go中的struct如何被优化，还有小插曲](https://mp.weixin.qq.com/s/SIDN3pOgK5cToNwflt7Lgg)

想必大家在coding的时候，很少对struct中的字段的字节对齐关注，今天带大家来看一下字节对齐在我们项目编码中的一些影响。

6、[万字长文告诉你 Go 1.19 中值得关注的几个变化](https://tonybai.com/2022/08/22/some-changes-in-go-1-19)

新版 Go 内存模型文档与 Go 运行时引入 Soft memory limit。

## 开源项目

1、[buffalo](https://github.com/gobuffalo/buffalo)

快速的 Go Web 开发框架，1.0 版本发布。

2、[go-chassis](https://github.com/go-chassis/go-chassis)

Go-Chassis 是一个go语言的微服务开发框架，专注于帮你实现云原生应用。Logo的含义是开发者可以通过引入go chassis重新创造和定制自己的“轮子”（即开发框架），以此来加速云原生应用的交付速度。

3、[go-sstables](https://github.com/thomasjungblut/go-sstables)

protobuf 兼容的 sstables 的 Go 库

## 资源&&工具

1、[seenvoy](https://github.com/saltbo/seenvoy)

可视化 Envoy 的配置。

2、[go_test_workshop](https://github.com/smallnest/go_test_workshop)

Go Test 从入门到躺平。

3、[example](https://github.com/GoAdminGroup/example)

一个简单的示例演示了如何快速运行 GoAdmin。

4、[《100 Go Mistakes》正式出版](https://www.manning.com/books/100-go-mistakes-and-how-to-avoid-them)

剧透下，中文版不会太远。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
