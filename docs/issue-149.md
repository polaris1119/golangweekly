# Go语言爱好者周刊：第 149 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue149/cover.png)

题图：父亲节快乐！

## 刊首语

上期题目的答案解析。以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	m := [...]int{
		'a': 1,
		'b': 2,
		'c': 3,
	}
	m['a'] = 3
	fmt.Println(len(m))
}
```

A：3；B：4；C：100；D：编译失败

正确答案是 C。这次的正确率也是惨不忍睹，只有 22%。为什么是这个答案，我会专门写文章讲解。

本期的题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	var p [100]int
	var m interface{} = [...]int{99: 0}
	fmt.Println(p == m)
}
```

A：true；B：false；C：panic；D：编译失败

## 资讯

1、[GoLand 2022.2 EAP](https://blog.jetbrains.com/go/2022/06/17/goland-2022-2-eap-5-is-out-with-automatic-sql-injection-support-for-websockets-and-graphql-endpoints-and-more/)

自动注入 SQL 语句，支持 WebSocket 和 GraphQL 端点等。

2、[chroma 2.2 发布](https://github.com/alecthomas/chroma)

纯 Go 实现的通用语法高亮库。

3、[tengo 2.12.0 发布](https://github.com/d5/tengo)

Go 脚本语言。

4、[Task 3.13.0 发布](https://github.com/go-task/task/releases/tag/v3.13.0)

任务运行器，使用 Go 语言编写。类似 GNU Make，目标是比它更简单和易于使用。

5、[欧洲 GopherCon 2022](https://gophercon.eu/)

7 月 28 日 到 31 日。

## 文章

1、[关于 Go1.18 新函数 TryLock 的故事](https://mp.weixin.qq.com/s/Lnr3ohaJlgqzZYonnczWSA)

分享一篇关于 1.18 新函数 TryLock 故事的文章。

2、[Java、Go 和 Python 的多线程性能对比](https://mp.weixin.qq.com/s/IKpaJE4icDhX6kyNaxsqRw)

分享多线程下这三门语言的表现。

3、[你所知道的 string 和 []byte 转换方法可能是错的](https://mp.weixin.qq.com/s/T--shUtArU-asFthtR7waA)

网上很多 string 和 []byte 的转换都是有问题的。

4、[发现了国外不加班的秘诀，各种 Go 代码示例都能在这搜到](https://mp.weixin.qq.com/s/Quw1LILDyxjisp7dmD-Dmg)

一个代码示例网站。

5、[Go 分布式链路追踪实现原理](https://mp.weixin.qq.com/s/JLy_-wTJFlDjets1sbmrDg)

在分布式、微服务架构下，应用一个请求往往贯穿多个分布式服务，这给应用的故障排查、性能优化带来新的挑战。

## 开源项目

1、[validate](https://github.com/gookit/validate)

Go 通用的数据验证与过滤库，使用简单，内置大部分常用验证、过滤器，支持自定义验证器、自定义消息、字段翻译。

2、[ioc-golang](https://github.com/alibaba/ioc-golang)

一款服务于 Go 开发者的依赖注入框架，方便搭建任何 Go 应用。

3、[manioc](https://github.com/fuzmish/manioc)

基于泛型的依赖注入容器。

4、[open-match](https://github.com/googleforgames/open-match)

开源的游戏匹配框架。

5、[slog](https://github.com/gookit/slog)

Go 实现的一个易于使用的，易扩展、可配置的日志库。

## 资源&&工具

1、[ptg](https://github.com/crossoverjie/ptg)

性能测试工具，也是一个 GUI gRPC 客户端。基于 Fyne 构建。

2、[envd](https://github.com/tensorchord/envd)

机器学习的开发环境。

3、[st](https://github.com/alistanis/st)

st 是一个命令行实用程序，用于在 Go 代码中为结构体打 tag。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
