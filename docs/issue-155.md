# Go语言爱好者周刊：第 155 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue155/cover.jpeg)

题图：Web Server

## 刊首语

上期题目解析。以下代码输出什么？

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

正确答案：A。正确率 47%。

## 资讯

1、[Echo v4.8 发布](https://github.com/labstack/echo/releases/tag/v4.8.0)

高性能的 REST 框架。

2、[imagor v1.0.0 发布](https://github.com/cshum/imagor)

用 Go 和 libvips 编写的高性能图像处理服务器。

3、[juicefs v1.0 发布](https://github.com/juicedata/juicefs)

基于 redis 和 S3 构建的分布式 POSIX 文件系统。

4、[sarama v1.36 发布](https://github.com/Shopify/sarama)

Sarama 是 Apache Kafka 0.8 及更高版本的 Go 库。

5、[sonic 1.3.5 发布](https://github.com/bytedance/sonic)

字节开源的高性能 json 编解码库。

6、[freecache 1.2.2 发布](https://github.com/coocood/freecache)

Go 缓存库，具有零 GC 开销和高并发性能。

7、[RedisShake 3.0 发布](https://github.com/alibaba/RedisShake)

阿里开源的Redis数据同步工具，Go 语言实现。

## 文章

1、[Go 每日一库之 Redis Web 端管理工具](https://mp.weixin.qq.com/s/hJhjNo8Z8ULA0UON8O6meA)

GRM 是基于 go+vue 的 web 版 redis 管理工具，部署简单便捷，支持 SSH 连接，用户校验，操作日志、命令行模式、LUA脚本执行等功能。

2、[2022 年 8 月编程语言排行榜：Go 降了这么多？](https://mp.weixin.qq.com/s/q_LR0vLcHSQV68XksaNQyA)

TIOBE 公布了 2022 年 8 月的编程语言排行榜。

3、[Carbon 会扼杀 Go 的势头吗？](https://mp.weixin.qq.com/s/esKde6mVxZp-O_F7JDzgbA)

近期，应该有不少人看到了，Google 要出另外一门编程语言：Carbon。虽然号称是 C++ 的继任者，但不少人可能会有疑问：会不会扼杀 Go 语言的势头？毕竟也是 Google 出的。

4、[从Golang调度器的作者视角探究其设计之道！](https://mp.weixin.qq.com/s/N1ColaDQtm7-LM5IqrJWqw)

本文是笔者结合自身经验和认知的一点观后感，采用从零开始层层递进的方法，总结剖析了其背后的软件设计思想，希望对读者更好地理解goroutine调度GMP模型会有所帮助。

## 开源项目

1、[algernon](https://github.com/xyproto/algernon)

小型独立的纯 Go Web 服务器，支持 Lua、Markdown、HTTP/2、QUIC、Redis 和 PostgreSQL 等。

2、[haxmap](https://github.com/alphadose/haxmap)

最快、内存效率最高的 golang 并发 hashmap。

3、[nff-go](https://github.com/intel-go/nff-go)

Go Network Function 框架。

4、[tdigest](https://github.com/influxdata/tdigest)

Ted Dunning t-digest 算法的 Go 实现。

## 资源&&工具

1、[Go 博客第 242 期](https://changelog.com/gotime/242)

依赖管理之痛。

2、[gotv](https://github.com/go101/gotv)

一个用于管理多个 Go 工具链版本安装的工具。

3、[infinite](https://github.com/fzdwx/infinite)

用 Golang 开发的交互式命令行(终端)组件库。作者投稿。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
