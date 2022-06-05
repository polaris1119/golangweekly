# Go语言爱好者周刊：第 147 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue147/cover.jpeg)

题图：来自 golangweekly

## 刊首语

先看看上期的题目。以下代码输什么？

```go
package main

import (
	"fmt"
)

func main() {
	var nums1 []interface{}
	nums2 := []int{1, 3, 4}
	nums3 := append(nums1, nums2)
	fmt.Println(len(nums3))
}
```

A：3；B：1；C：4；D：编译失败

正确答案是 B，即长度是 1。正确率只有 37%。先不说具体原因，本期将这道题稍微改一下，看看有多少人能做对。

以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	var nums1 []interface{}
	nums2 := []int{1, 3, 4}
	nums3 := append(nums1, nums2...)
	fmt.Println(len(nums3))
}
```

A：3；B：1；C：4；D：编译失败

## 资讯

1、[Go 1.18.3 发布](https://mp.weixin.qq.com/s/qe4uNG5XKa98rNJN0NUHSA)

Go 官方发布了 Go1.18.3 和 Go1.17.11，这是两个小版本，主要涉及 4 个安全问题修复。

2、[GoLand 2022.2 EAP](https://blog.jetbrains.com/go/2022/06/03/goland-2022-2-eap-3-is-here-with-updates-for-generics-a-keyboard-shortcut-to-change-the-font-size-and-an-option-to-import-multiple-csv-files/)

这里提供了泛型更新、更改字体大小的键盘快捷键，以及导入多个 CSV 文件的选项。

## 文章

1、[用Go重写Node.js服务：项目性能提升5倍，内存减少40%](https://mp.weixin.qq.com/s/oEzqFQgyRgj8kgDhAhPn4A)

在使用 Golang 进行重写后，其可处理的服务请求数增加了 5 倍，同时内存消耗减半。

2、[2022 年值得学习的 Golang 包](https://mp.weixin.qq.com/s/fxrgYG1xm_hG-bNPQG0YMg)

今天为大家推荐 2022 年最好的 Go 包。

3、[Go中使用单调时钟获得准确的时间间隔](https://mp.weixin.qq.com/s/9LW3RSyX1uaHGydJ63zbIw)

墙上时钟与单调时钟。

4、[从项目的一个 panic 说起：Go 中 Sync 包的分析应用](https://mp.weixin.qq.com/s/ptpkN9AgV4GZHhruA-J8tA)

项目开发中遇到一个错误 “fatal error: concurrent map read and map write”。

5、[某些情况下，合理使用Go指针将大大提升程序的运行效率](https://mp.weixin.qq.com/s/0zwSjHdpxcVZvNihA90Bpg)

避免在循环中造成不必要的数组空指针检查。

6、[简化 Go 中对 JSON 的处理](https://mp.weixin.qq.com/s/ND_W1g0k0tKZNpC2ohDR0w)

JSON 是项目中不可避免的。

7、[Go 中的 HTTP debug 技能 了解一下](https://mp.weixin.qq.com/s/ZWJO4Y1RVqR4d4mJkPFb0Q)

介绍一下 httptrace 和问题的定位过程。

8、[我在抖音架构部门后端实习半年的感悟](https://mp.weixin.qq.com/s/SVB_2IRkopL-qI6xkU43dw)

面经。

## 开源项目

1、[zinc](https://github.com/zinclabs/zinc)

轻量级的 elasticsearch 替代者。

2、[testfixtures](https://github.com/go-testfixtures/testfixtures)

类似于 Ruby-on Rails 用于 Go 的测试，针对真实数据库编写测试。

3、[tarmac](https://github.com/madflojo/tarmac)

使用 Web Assembly 构建分布式服务的框架。

4、[Uniqush](https://github.com/uniqush/uniqush-push)

开源移动应用通知推送服务。

5、[connect-go](https://github.com/bufbuild/connect-go)

一个更好的 gRPC。

6、[Tigris](https://github.com/tigrisdata/tigris)

一个现代的、可扩展的用于构建实时网站和应用程序的后端。

7、[mo](https://github.com/samber/mo)

基于 Go 泛型实现的 monad 和函数编程抽象。

## 资源&&工具

1、[transporter](https://github.com/compose/transporter)

在持久性引擎之间同步数据，如 ETL。

2、[Go 播客第 231 期](https://changelog.com/gotime/231)

Berlin 转型为 Go 的过程。

3、[webrtc-nuts-and-bolts](https://github.com/adalkiran/webrtc-nuts-and-bolts)

通过代码和详细的文档全面了解 WebRTC 及其协议的实际运行情况。

4、[jid](https://github.com/simeji/jid)

通过使用 jq之 类的过滤查询以交互方式深入 JSON。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
