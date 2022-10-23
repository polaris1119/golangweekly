# Go语言爱好者周刊：第 164 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue164/cover.jpeg)

题图：无题

## 刊首语

上期是一道关于 map 的题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
    var m map[string]int
    delete(m, "oh noes!")
    fmt.Println(m)
}
```

A：map[]；B：nil；C：Panic；D：编译错误

正确答案是 A。

在 delete 函数的文档有说明：

```bash
The delete built-in function deletes the element with the specified key (m[key]) from the map. If m is nil or there is no such element, delete is a no-op.
```

因此 delete 啥也没做。

本期继续看一道关于 map 的题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	pairs := [][2]string{
		{"a", "apple"},
		{"a", "ant"},
		{"b", "bee"},
	}

	m := map[string]string{
		pairs[0][0]: pairs[0][1],
		pairs[1][0]: pairs[1][1],
		pairs[2][0]: pairs[2][1],
	}
	fmt.Println(m["a"])
}
```

A：编译错误；B：apple；C：ant；D：panic

## 资讯

1、[提议：增加清除 map 的方法](https://github.com/golang/go/issues/56351)

rsc 建议这样 `delete(m)` 清除 map。

2、[实验性支持 arena 包](https://github.com/golang/go/commit/e0d01b8467b5cb9e68758932f50c3187374011ba)

这是今年二月份的提案：<https://github.com/golang/go/issues/51317>，提供另一种分配内存的方法，可以减少内存管理开销。

3、[Wails 2.1 发布](https://wails.io/zh-Hans/)

构建跨平台的桌面应用。

4、[buf 1.9 发布](https://github.com/bufbuild/buf)

一种新的 Protobuf 处理库。

5、[rqlite v7.8.0 发布](https://github.com/rqlite/rqlite)

基于 SQLite 分布式关系数据库。

6、[easegress 2.2 发布](https://github.com/megaease/easegress)

全能型流量编排系统。国人开发。

## 文章

1、[字节大规模微服务 Go 语言发展之路](https://mp.weixin.qq.com/s/Oz0Zn8Y43UfHIOPL6rZ5Ig)

本文整理自字节跳动高级工程师马春辉在 DIVE 全球基础软件创新大会 2022 的演讲分享，主题为“字节大规模微服务语言发展之路”。

2、[Golang依赖注入提升开发效率！](https://mp.weixin.qq.com/s/aqw3KzxAyt-BlMfW31oV4Q)

依赖注入并不是java独有的，也不是web框架独有的，本文用通俗易懂的语言讲解什么是依赖注入，为什么需要依赖注入，以及go语言如何使用依赖注入来提升开发效率。

3、[一文搞懂Go内联优化](https://mp.weixin.qq.com/s/SrsYKPjM7hph8yaW9rYENw)

在这一篇文章中，我就和大家一起来学习和理解一下Go编译器的内联优化。

4、[Go 的 IO 流怎么并发？小技巧分享](https://mp.weixin.qq.com/s/7hWvLdcTIkokX9DpIuqovQ)

今天聊一个存储的实现细节，数据副本的并发写入。

5、[Fleet 特性预览](https://programmingpercy.tech/blog/previewing-the-ide-of-the-future)

JetBrains 下一代 IDE，本文针对 Go 开发者。

6、[还咋优化？我是说Go程序](https://colobu.com/2022/10/17/a-first-look-at-arena/)

arena 包使用示例。

7、[Go 每日一库之 go-cache 缓存](https://mp.weixin.qq.com/s/f4FAt-RgraOFXSfZmWjeoQ)

go-cache 是一个轻量级的基于内存的 K-V 储存组件，内部实现了一个线程安全的 map[string]interface{}，适用于单机应用。

## 开源项目

1、[frankenphp](https://github.com/dunglas/frankenphp)

一个现代的 PHP app server。

2、[pp](https://github.com/k0kubun/pp)

带颜色的漂亮打印包。

3、[goatcounter](https://github.com/arp242/goatcounter)

简单的 Web 流量分析程序。

4、[retry-go](https://github.com/avast/retry-go)

简单的重试机制包。

5、[nbio](https://github.com/lesismal/nbio)

纯 Go 的 1000k+ 连接解决方案。

## 资源&&工具

1、[GoLab 2022 talk](https://golab.io/)

其中一篇 [The Go WebAssembly ABI at a Low Level](https://xeiaso.net/talks/wasm-abi)。

2、[文档中找不到的Go 1.18和1.19版本的变化](https://go101.org/blog/2022-08-22-some-undocumented-changes-in-go-1.18-and-1.19.html)

Go 101 各种抠细节。

3、[油管视频](https://www.youtube.com/watch?v=0ZxYL3M9Ytg&themeRefresh=1)

使用 Go 编写更快、更安全的应用。

4、[GopherCon 2022 技术大会 slides](https://github.com/gophercon/2022-talks)

新鲜出炉。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
