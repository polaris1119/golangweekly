# Go语言爱好者周刊：第 152 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue152/cover.png)

题图：golangweekly

## 刊首语

上期题目，以下代码输出什么？

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

正确答案：D，该题正确率 36%。错误：

```bash
cannot take address of m["uno"] (map index expression of type int)
```

本期题目。以下代码输出什么？

```go
package main

import "fmt"

func main() {
	const c = 8
	a := &c
	*a = 12
	fmt.Println(*a)
}
```

A：8；B：不能编译；C：12

## 资讯

1、[plow 1.3 发布](https://github.com/six-ddc/plow)

Go 实时 Web UI 和终端显示的高性能 HTTP 基准测试工具。

2、[Logrus 1.9 发布](https://github.com/sirupsen/logrus)

功能丰富的结构化 Logger。

3、[rqlite 7.6.0 发布](https://github.com/rqlite/rqlite)

基于 SQLite 分布式关系数据库。

4、[usql 0.10 发布](https://github.com/xo/usql)

数据库的通用 cli 工具，可以认为是数据库的瑞士军刀。

## 文章

1、[GC 指南](https://go.dev/doc/gc-guide)

Go 官方的 GC 指南。

2、[相比高人气的Rust、Go，为何 Java、C 在工具层面进展缓慢？](https://mp.weixin.qq.com/s/cG5R6J4PW6OEGSIK6z02UA)

最受欢迎的高人气编程语言（2022）：Rust，Typescript，Python，Go，C#，Kotlin，JavaScript。

3、[Go 每日一库之 roaring](https://mp.weixin.qq.com/s/zu0HyJybjwb19nNMDeFcEw)

集合是软件中的基本抽象。实现集合的方法有很多，例如 hash set、tree等。

4、[Hugo 作者、Go 语言产品负责人突然宣布离职](https://mp.weixin.qq.com/s/du5DYfyOSMGygArtRPOu8g)

7月18日，谷歌Go语言产品负责人Steve Francia在个人博客上发了篇长文，回顾总结自己在谷歌的6年生涯经历，并分享了离开的原因。

5、[Go 每日一库之 bitset](https://mp.weixin.qq.com/s/Fy_OKqSmIK6ImQQDiNGH9A)

bitset 库实现了位集合及相关操作。

## 开源项目

1、[cpuid](https://github.com/klauspost/cpuid)

获取 CPU 详细信息。

2、[graph](https://github.com/dominikbraun/graph)

用于创建图形数据结构并对其执行操作的泛型库。

3、[flogo](https://github.com/TIBCOSoftware/flogo)

开源的事件驱动能力的生态系统。

## 资源&&工具

1、[lensm](https://github.com/loov/lensm)

以源码对照方式查看 Go 汇编，还有一篇专门介绍的文章：<https://www.storj.io/blog/lensm>。

2、[swag](https://github.com/swaggo/swag)

Swag 将 Go 的注释转换为 Swagger2.0 文档。

3、[gotemplate](https://gotemplate.io/)

在线快速测试 Go template。

4、[gokey](https://github.com/cloudflare/gokey)

Go 中一个简单的无保险库密码管理器。

5、[Go Time 第 238 期](https://changelog.com/gotime/238)

Go 是面向对象编程语言吗？

6、[nezha](https://github.com/naiba/nezha)

Go 实现的自托管的轻量级服务器和网站监控和运维工具。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
