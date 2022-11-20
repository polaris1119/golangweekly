# Go语言爱好者周刊：第 168 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue168/cover.png)

题图：GoLand 2022.3 RC 发布

## 刊首语

以下代码输出什么？

```go
package main

import "fmt"

func main() {
    a := (-3) % 2
    b := (-3) % (-2)
    fmt.Println(a, b)
}
```

A：1 1；B：-1 1；C：-1 -1；D：编译错误

## 资讯

1、[Google Go 风格指南](https://google.github.io/styleguide/go/index)

Go Style Guide 和随附的文档整理了当前编写可读和惯用的 Go 的最佳方法。

2、[GoLand 2022.3 RC 发布](https://blog.jetbrains.com/go/2022/11/17/goland-2022-3-release-candidate-is-out/)

正式版不远了。

3、[NSA 推荐使用类型安全的语言代替 C/C++](https://www.theregister.com/2022/11/11/nsa_urges_orgs_to_use/)

推荐的重点包括 Go 和 Rust。

4、[lo 1.35 发布](https://github.com/samber/lo)

基于泛型的 Lodash 风格库。

5、[rqlite v7.11.0 发布](https://github.com/rqlite/rqlite/releases/tag/v7.11.0)

轻量的、分布式关系数据库。

6、[slashbase 1.1 发布](https://github.com/slashbaseide/slashbase)

数据库协作工具。

7、[chroma 2.4 发布](https://github.com/alecthomas/chroma)

纯 Go 实现的通用语法高亮库。

8、[ElasticSearch Go 8.5 发布](https://github.com/elastic/go-elasticsearch)

ElasticSearch Go 8.5 官方客户端发布。

9、[fzf 0.35.0 发布](https://github.com/junegunn/fzf/releases/tag/0.35.0)

Command-line fuzzy finder。

## 文章

1、[Go标准库依赖的那些modules](https://mp.weixin.qq.com/s/pPySr5vgxU3zhSvDhP1U6A)

对于程序员来说，编写的代码依赖标准库是“天经地义”的事情。

2、[基于 Twitch 的 Go RPC](https://thedevelopercafe.com/articles/rpc-in-go-using-twitchs-twirp-3dcb78ece775)

类似于 gRPC。

3、[在 Go 程序中嵌入提交哈希的 3 种方法](https://developers.redhat.com/articles/2022/11/14/3-ways-embed-commit-hash-go-programs)

清晰的知晓当前程序使用的哪个提交。

4、[鹅厂后台大佬教你Go内存管理！](https://mp.weixin.qq.com/s/MIohusSSUxIg5S5cMZGhig)

本文推选自腾讯云开发者社区-【技思广益 · 腾讯技术人原创集】专栏。

5、[Go每日一库之实时可视化Go Runtime指标](https://mp.weixin.qq.com/s/n-d2HKiDhNYrTYSFRksf3w)

在浏览器中可以实时看到服务的 runtime 指标信息。

6、[成为 Go 高手的 8 个 GitHub 开源项目](https://mp.weixin.qq.com/s/65pjvdsFNNeFXHy3J-A16A)

想成为 Go 高手吗？那推荐看看这些开源项目。

7、[一起看看 Go 1.20 新特性有哪些？](https://mp.weixin.qq.com/s/65S0KRbtdZTzC4YmsY_3-A)

在这篇文章中，一起去Go 1.20 milestone 的 issues 列表中翻翻，提前看看究竟会有哪些新特性加入 Go。

## 开源项目

1、[varint](https://github.com/1pkg/varint)

快速、内存高效的、支持任意位的整型。

2、[golang-lru](https://github.com/hashicorp/golang-lru)

LRU 算法的实现。

3、[pie](https://github.com/elliotchance/pie)

slice 和 map 便利、通用的操作。

4、[tamarin](https://github.com/cloudcmds/tamarin)

内嵌的脚本语言。

5、[go-quartz](https://github.com/reugn/go-quartz)

小型、零依赖的调度库，启发自 Java 的 Quartz。

6、[memos](https://github.com/usememos/memos)

开源、自托管的知识管理和协作系统。

7、[pdf](github.com/dslipak/pdf)

从 PDF 文件中提取文本。

## 资源&&工具

1、[一致性的 log](https://www.youtube.com/watch?v=gd_Vyb5vEw0)

基于 Go 官方的结构化日志（视频）。

2、[Go Time 第 256 期](https://changelog.com/gotime/256)

grpc 和 protobuf。

3、[sablier](https://github.com/acouvreur/sablier)

按需启动容器，在没有活动时自动关闭容器。Docker、Docker Swarm 模式和 Kubernetes兼容。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
