# Go语言爱好者周刊：第 101 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue101/cover.jpg)

题图：各国语言识别

## 刊首语

上期周刊题目正确率 45%。题目如下。

Go 版本 1.12 以上，以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	m := map[string]int{"foo": 0, "bar": 1, "baz": 2}
	for k := range m {
		if k == "foo" {
			delete(m, "bar")
		}
		if k == "bar" {
			delete(m, "foo")
		}
	}
	fmt.Println(m)
}
```

A：map[baz:2 foo:0]；B：map[bar:1 baz:2]；C：map[baz:2]；D：不确定

正确答案：D。因为 map 中元素顺序是随机的，因此结果不确定，每次运行结果可能不一样。

本期的题目是 Go101 发的一道题：

```go
package main

var n = -99

func main() {
  m := make(map[string]int, n)
  println(m["Go"])
}
```

A：0；B：panic；C：不知道

## 资讯

1、[Caddy 2.4.3 发布](https://github.com/caddyserver/caddy/releases/tag/v2.4.3)

这是第 100 个发布。

2、[读写锁性能提升](https://go-review.googlesource.com/c/go/+/329769)

Dmitry Vyukov 提交一个变更，该变更是的读写锁的写锁性能有 40% 以上的大幅提升。

3、[Go1.17 快报之标准库越来越注重易用性](https://mp.weixin.qq.com/s/6MWl8eT0KetLpLql_YLf4A)

说起 Go 的优点，很多人会提到 Go 拥有强大的标准库，比如开发一个 HTTP 服务，几行代码就搞定。不过，如果是一个 PHPer 转到 Go，又会觉得 Go 标准库不够便利，很多东西都需要自己二次封装。这其实是一个取舍的问题。

4、[重磅！Go 启用新的官方问答社区](https://mp.weixin.qq.com/s/nEWD2SBzTpCTe_kmpq2c1w)

Go 官方宣布，在 StackOverflow 上启用新的问答社区，而这之前，官方的主要在 Google Groups。

5、[真任性](https://github.com/golang/go/issues/46934)

Go 核心团队安静两周（6.26 ~ 7.11）。

## 谁在招 Gopher

整理近期的 Go 职位。有招聘需求可以到「Go招聘」发布！ 

1、[网易游戏招聘Gopher，这福利有点香哦](https://mp.weixin.qq.com/s/8ZVpsngJC2_GxfhD4mj3AQ)

2、[待遇比肩字节的招聘，你要来挑战嘛？](https://mp.weixin.qq.com/s/xv0dme8y2N9-R_ulmrfbpw)

3、[这是要干嘛？！微软招 Go 编译器全职开发人员](https://mp.weixin.qq.com/s/gKeFG5mCLUsmXPPWratSGw)

4、[有问题，上知乎。找Gopher，来Go招聘](https://mp.weixin.qq.com/s/LZCpRFDgYFiuJOSE0GENPw)

## 文章

1、[为什么 Go 关心 unsafe.Pointer 和 uintptr 之间的差别](https://mp.weixin.qq.com/s/v37jHYwt-msNIwIntlRZPg)

Go 有两样东西或多或少是无类型指针的表示：uintptr 和 unsafe.Pointer （和外表相反，它们是内置类型）。

2、[Go：随机数是怎样产生的？](https://mp.weixin.qq.com/s/lg0LhtK4CiM7-OC790aYCQ)

Go 实现了两个包来产生随机数。

3、[图解 Go GC 内存标记法](https://mp.weixin.qq.com/s/t3SffaVmHUb_vqB9pn5yqA)

Go GC 的作用是回收不再使用的内存。实现的算法是并发的三色标记和清除回收法。本中文，我们研究三色标记法，以及各个颜色的不同用处。

4、[Go: GC 是怎样监听你的应用的？](https://mp.weixin.qq.com/s/Nqr096q51NWbyN6VujFTzA)

Go GC 能够帮助到开发者，通过自动地释放掉一些程序中不再需要使用的内存。

5、[50K Gopher的面试题是什么样的？](https://mp.weixin.qq.com/s/BXazVYFpDWKKQj9taRNc_g)

答案你来给？

6、[Go 问题排查实战: 请求无响应](https://mp.weixin.qq.com/s/-RmAIuPwT-bAwdKriwMg-w)

本文是问题排查经历以及容器 IO 流转原理分析。

7、[深度 | 字节跳动微服务架构体系演进](https://zhuanlan.zhihu.com/p/382833278)

本文整理自字节跳动（火山引擎）基础架构/服务框架团队负责人成国柱在 QCon 2021 的分享，主要介绍了 2018-2021 年间，服务框架团队在 Golang 服务框架和 Service Mesh 上的技术实践和经验总结。

## 开源项目

1、[lingua-go](https://github.com/pemistahl/lingua-go)

最准确的 Go 自然语言检测库，长文本和短文本均适用。迄今为止支持 75 种语言

2、[survey](https://github.com/AlecAivazis/survey)

建立交互式提示的库。

![](imgs/issue101/survey.gif)

3、[naml](https://github.com/kris-nova/naml)

用 raw go 替换 kubernetes yaml 的框架。

4、[smocker](https://github.com/Thiht/smocker)

简单高效的 HTTP Mock 服务和代理。

5、[pipeline](https://github.com/deliveryhero/pipeline)

一个帮助你在 Go 中创建流水线的库。

## 资源&&工具

1、[musgo](https://github.com/ymz-ncnk/musgo)

用于序列化和反序列化 Go 对象的代码生成器。

2、[timetrace](https://github.com/dominikbraun/timetrace)

Go 实现的基于命令行的时间跟踪工具。

3、[mahi](https://github.com/threeaccents/mahi)

多合一的 HTTP 服务，用于文件的上传、处理、服务和存储。

4、[liqo](https://github.com/liqotech/liqo)

实现跨 Kubernetes 集群的动态和分散的资源共享。

5、[plow](https://github.com/six-ddc/plow)

Go 实时 Web UI 和终端显示的高性能 HTTP 基准测试工具。

6、[dud](https://github.com/kevin-hanselman/dud)

Go 实现的用于与源代码一起版本控制数据的工具。

7、[Go 播客第 185 期](https://changelog.com/gotime/185)

TDD 是如何帮助我们更好地开发 Go 代码,原理与实践。

8、[elvish](https://github.com/elves/elvish)

Go 实现的交互式 shell。

9、[go-recipes](https://github.com/nikolaydubina/go-recipes)

Go 命令行实用命令。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
