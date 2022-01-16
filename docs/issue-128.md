# Go语言爱好者周刊：第 128 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue128/cover.png)

题图：csvutil

## 刊首语

上期是一道关于 `|` 的题目，以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	var a, b float64 = 1.0, 4.0
	fmt.Println(a | b)
}
```

A：5；B：+Inf；C：panic；D：不能编译

正确答案是 D。

Go 语言中文网最近新增了一个功能：Go每日一题，每天一道 Go 题目及解析，可以每天一刷，访问地址：<https://studygolang.com/interview/question>。

## 资讯

1、[validator 寻找额外的维护者](https://github.com/go-playground/validator/issues/874)

因为需求多，作者觉得自己一个人没法花太多时间在这个项目，希望有其他人参与进来。

2、[GoReleaser 1.3 发布](https://goreleaser.com/)

尽可能快速、轻松地交付 Go 二进制文件。

3、[go-github v42.0 发布](https://github.com/google/go-github)

GitHub v3 API 的 Go 客户端。

## 文章

1、[Go：服务怎么做到监听随机端口](https://mp.weixin.qq.com/s/DNfegnHPWAe1oBgLx2O-4g)

通常，服务一般会监听固定的端口。不过如果是本地测试服务，也许有时候想随机一个可用的端口。

2、[Uber：大规模、半自动化 Go GC 调优](https://mp.weixin.qq.com/s/XithQarYmXHbPhtVzhNm-w)

Uber 是国外大规模使用 Go 的公司之一，在 GitHub 上，他们开源了不少 Go 相关项目，本文介绍 Uber 如何在 30 个关键任务服务中节省 7 万个内核。

3、[Typora 宣布收费后，这款开源 Markdown 编辑器火了](https://mp.weixin.qq.com/s/4zqNSSA0Ortw-Wx1cG9qCA)

喜欢 Typora 的可以付费支持下。

4、[GitHub 发现了 studygolang 项目依赖的漏洞](https://mp.weixin.qq.com/s/jFqy_HtK-1qIh--RIx00rQ)

GitHub 这个功能挺好。

5、[为 Java 开发者准备的 Go 教程 02：Java 有而 Go 无](https://mp.weixin.qq.com/s/1BPDqnmwUDNKN7qwYoc4QQ)

Go 语言的设计是站在巨人的肩膀上的，它吸取了其他语言的优秀设计，同时摒弃了一些「不认可」的设计。

6、[Go 1.18 中的三个小功能](https://mp.weixin.qq.com/s/NwMzaXEUzRLdjK1VG32HBA)

二进制中包含的版本控制信息，这个挺好。

7、[2022 年 7 本最佳 Go 图书](https://mp.weixin.qq.com/s/q3gXz803psBdy0vkFyPxvA)

Go 图书越来越多，有些不错，有些不太好。我认为如果你正在学习 Go，你应该尽可能广泛地阅读：即使是最好的 Go 图书也只代表一种观点。

## 开源项目

1、[bintris](https://github.com/Lallassu/bintris)

Go 开发的手机游戏。

![](imgs/issue128/bintris.png)

2、[remark42](https://github.com/umputun/remark42)

注重隐式的轻量级、Go 实现的评论引擎，可以嵌入你的任何网站。

3、[govcl](https://github.com/ying32/govcl)

跨平台的 GUI 库，国人实现。

4、[toml](https://github.com/BurntSushi/toml)

使用反射实现的 toml 解析器。

5、[mr-plow](https://github.com/Ringloop/mr-plow)

最小的内存使用，云原生 logstash 的替代品。

6、[asm](https://github.com/segmentio/asm)

提供优化的算法库，充分利用现代 CPU 的特性。

7、[camellia](https://github.com/debevv/camellia)

一个轻量级的、持久的、分层的键值存储，用 Go 语言编写。

8、[ratelimit](https://github.com/yudeguang/ratelimit)

业务级访客限流库（非网关级如go.uber.org/ratelimit），作者自荐。

9、[csvutil](https://github.com/jszwec/csvutil)

csvutil 提供了 CSV 和 Go 值之间的快速且惯用的映射。

## 资源&&工具

1、[miller](https://github.com/johnkerl/miller)

文本数据处理的瑞士军刀，Go 实现。

2、[mango](https://github.com/muesli/mango)

为 Go flag、pflag 和 cobra 软件包提供的 man page 生成器。

3、[Go 播客第 212 期](https://changelog.com/gotime/212)

传统工作之外的 Go 应用。

4、[gocap](https://github.com/cugu/gocap)

列出你的依赖能力，监测依赖更新是否需要更多的能力。

5、[helmify](https://github.com/arttor/helmify)

从 Kubernetes yaml 创建 Helm chart。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
