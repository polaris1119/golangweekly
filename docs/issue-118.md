# Go语言爱好者周刊：第 118 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue118/cover.png)

题图：Go 圣诞日历

## 刊首语

上期的题目：

```go
package main

import "fmt"

func main() {
	x := []byte{}
	fmt.Printf("%#v %T\n", x, x)
}
```

A：[]byte{} []byte；B：[]byte{} []uint8；C：[]uint8{} []byte；D：[]uin8{} []uint8

答案是 B。这是一个 bug，说正确答案应该是 `  []uint8{} []uint8` 才对，因为 byte 是 uint8 的别名，但现在即使是 `x := []uint8{}`，结果也还是 B。不过为了兼容性，该 bug 目前不会修复，影响不大，详见：<https://github.com/golang/go/issues/44391>。

本期是一道关于 defer 的题目：

```go
package main

import (
	"fmt"
)

func main() {
	f := func() { fmt.Print("A") }
	defer f()
	f = func() { fmt.Print("B") }
	defer f()
}
```

A：AA；B：AB；C：BA；D：BB

## 资讯

1、[Go1.17.3 和 Go1.16.10 发布](https://mp.weixin.qq.com/s/6XiNbV-rvrvvXI951Ge6dw)

安全更新。

2、[crawley v1.1.0 发布](https://github.com/s0rg/crawley)

Unix 风格的 Web 爬虫。

3、[Google's Go Day 2021](https://opensourcelive.withgoogle.com/events/go-day-2021)

2021 年 11 月 5 日举行的，视频发布在了 youtube 上。

## 文章

1、[Go：如何获得项目根目录？](https://mp.weixin.qq.com/s/NJwOfaOT80uFyDh5G0ILjQ)

常见的需求。

2、[如何组织 Go 代码？Go 作者的回答惊呆了](https://mp.weixin.qq.com/s/uTCNXr5RoOjmlQ_mVjxnXg)

这是最常见的问题之一。你可以通过互联网寻找这个问题的答案。不过，我不确认我的设计是否 100% 正确，但希望给你一些参考。

3、[Go1.18 快讯：新增字符串 Clone API](https://mp.weixin.qq.com/s/hYciyIlp0EEoM-TVjydRiA)

标准库中新增的一个 API：strings.Clone()。

4、[go generate 完全指南](https://mp.weixin.qq.com/s/YBGppDhhBMorqkSzvufHlA)

自从 Go 1.4 引入 go generate 命令后，它一直广泛应用于 Go 生态系统。

5、[Go web 和微服务实战教程推荐](https://mp.weixin.qq.com/s/7jzPDm88XDkERwijLwlyKA)

各大框架的一些教程。

6、[25秒读取16GB文件，Go怎么做到的？](https://mp.weixin.qq.com/s/k6k9bwpKPdfShEEiTLSJ7w)

听起来很厉害！

7、[Go 中常用的四大重构技术](https://mp.weixin.qq.com/s/urdxZlq4nPassPwrQLzN3A)

重构是程序员需要掌握的技术。

8、[Go 语言服务、请求、响应、错误码设计与实现](https://juejin.cn/post/7025223216473833486)

不同的人可能有不同的做法，供参考。

## 开源项目

1、[MangoDB](https://github.com/MangoDB-io/MangoDB)

MongoDB 的的开源替代方案，Go 语言实现。

2、[gohtml](https://github.com/DrGrimshaw/gohtml)

将 Go 结构体转为 HTML 的编码器。

3、[noti](https://github.com/variadico/noti)

监听进程并触发通知。

![](imgs/issue118/noti.png)

4、[webview](https://github.com/webview/webview)

小型的跨平台 webview 库。

5、[kyoto](https://github.com/yuriizinets/kyoto)

Golang SSR-first 前端库。

6、[Open-IM-Server](https://github.com/OpenIMSDK/Open-IM-Server)

前微信技术专家打造的基于 Go 实现的即时通讯（IM）项目。

## 资源&&工具

1、[embedded-struct-visualizer](https://github.com/davidschlachter/embedded-struct-visualizer)

可视化 Go 结构体的嵌入式层次结构。

2、[structslop](https://github.com/orijtech/structslop)

一个 Go 的静态分析器，它建议重新排列结构字段，以提供最大的空间/分配效率。

3、[algs4-go](https://github.com/youngzhu/algs4-go)

将《算法》第四版中的 Java 算法实现“翻译”为 Go 实现。

4、[golang.christmas](https://golang.christmas/)

Gopher 圣诞日历。

5、[depp](https://github.com/CryogenicPlanet/depp)

Go 实现的快速未使用和重复的依赖项检查器。

6、[Go Day 2021](https://www.youtube.com/watch?v=nr8EpUO9jhw)

Go 中泛型的使用。油管视频。

7、[dl](https://github.com/thedevsaddam/dl)

命令行文件下载器。

8、[data-structure](https://github.com/Tv0ridobro/data-structure)

数据结构的泛型实现。

9、[u-root](https://u-root.org/)

Go实现的 linux/unix 常用工具集合。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
