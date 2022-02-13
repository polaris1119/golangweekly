# Go语言爱好者周刊：第 131 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue131/cover.jpg)

题图：自由式滑雪运动员谷爱凌

## 刊首语

本期题目。以下代码输出什么？

```go
package main

import (
	"fmt"
	"time"
)

func main() {
	ch := make(chan bool)
	go func() {
		<-ch
		fmt.Print("Goroutine")
	}()
	time.Sleep(2 * time.Second)
	close(ch)
	time.Sleep(3 * time.Second)
	fmt.Print("Main")
}
```

A：Groutine；B：Main；C：Goroutine；D：GoroutineMain

## 资讯

1、[Go 1.17.7 和 1.16.14 发布](https://mp.weixin.qq.com/s/xSeBvTbfRt6s0wnI9hbTdg)

三个安全问题修复。

2、[rqlite 7.2.0 发布](https://github.com/rqlite/rqlite)

基于 SQLite 分布式关系数据库。

3、[Telebot 3.0 发布](https://github.com/tucnak/telebot/releases/tag/v3.0.0)

Telegram 机器人框架。

4、[go-elasticsearch 8.0 发布](https://github.com/elastic/go-elasticsearch)

Elasticsearch 的官方 Go 客户端。

5、[CoreDNS 1.9 发布](https://github.com/coredns/coredns)

一个 DNS 服务器/转发器，用 Go 编写，链式插件，每个插件都执行一个（DNS）功能。

6、[Zap 1.21 发布](https://github.com/uber-go/zap)

Uber 出品的日志库。

7、[给力！Go 马上进前十了](https://mp.weixin.qq.com/s/uFyrMW_Y0D-64XU0eNFMYw)

2022 年 2 月编程语言排行榜。

## 文章

1、[「2022 版」轻松搞定 Go 开发环境](https://mp.weixin.qq.com/s/jq8hmovN7YD90dCBOToKuQ)

希望对新手有帮助。

2、[Go1.18 这个包确定没了](https://mp.weixin.qq.com/s/odWcML2OIlT97EXbhYcZNQ)

constraints 包在正式版中将不包含。

3、[我做了一个 Go 语言的微服务工具包](https://mp.weixin.qq.com/s/6FZVr_gInuQLUJREDNzrKQ)

开发一个工具包帮助希望使用 Go 来增强微服务的其他开发人员。

4、[2022 技术趋势：Go、Rust 将大放异彩](https://mp.weixin.qq.com/s/tOUjNsDlW5qs2dghwAEjig)

在线学习平台 O'Reilly 最新发布了一份《Technology Trends for 2022》报告。

5、[Go：基于 MongoDB 构建 REST API — Fiber 版](https://mp.weixin.qq.com/s/8k6SJ5NOV7E4UdWDrJ-EgA)

一篇基于 MongoDB 构建 REST API 的文章，使用的是 Fiber 框架。

## 开源项目

1、[wish](https://github.com/charmbracelet/wish)

让在 Go 中构建基于 SSH 的应用变得更容易。

2、[shortuuid](https://github.com/lithammer/shortuuid)

一个简洁、URL 安全的 uuid 的生成器库。

3、[oak](https://github.com/oakmound/oak)

一个纯 Go 实现的游戏引擎。

4、[gambit](https://github.com/maaslalani/gambit)

在终端下国际棋。

![](imgs/issue131/chess.gif)

5、[smart.go](https://github.com/anatol/smart.go)

用于访问磁盘低级别的 S.M.A.R.T. 信息的 Go 包。

6、[ql](https://gitlab.com/cznic/ql)

用 Go 和 SQLite 建立一个网络应用程序。

## 资源&&工具

1、[pget](https://github.com/Code-Hex/pget)

Go 实现的最快的客户端下载工具。

2、[demangle](https://github.com/ianlancetaylor/demangle)

可用于解读 C++ 和 Rust 符号名称的 Go 包。Go 官方团队的人写的。

3、[playbook-go](https://github.com/betrybe/playbook-go/blob/main/README_EN.md)

Trybe 公司的 Go 编程指南。英文。

4、[Go 博客第 214 期](https://changelog.com/gotime/214)

无痛数据迁移(使用 goose)。

5、[CoreRAD](https://github.com/mdlayher/corerad)

一个可扩展和可观察的 IPv6 邻居发现协议路由器守护程序。

6、[gocovsh](https://github.com/orlangure/gocovsh)

一个从命令行探索 Go Coverage 报告的工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
