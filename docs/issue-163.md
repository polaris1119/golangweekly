# Go语言爱好者周刊：第 163 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue163/cover.jpeg)

题图：error 处理提案

## 刊首语

本期一道关于 map 的题目。以下代码输出什么？

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

## 资讯

1、[考虑重新定义 for 变量](https://github.com/golang/go/discussions/56010)

在 HN 上也有讨论：<https://news.ycombinator.com/item?id=33160236>。

2、[gum 0.8 发布](https://github.com/charmbracelet/gum)

一款用于制作迷人 shell 脚本的工具。

3、[fsnotify 1.6.0 发布](https://github.com/fsnotify/fsnotify/releases/tag/v1.6.0)

文件系统事件通知。

4、[lazydocker 0.19 发布](https://github.com/jesseduffield/lazydocker)

用于 Docker 的基于终端的 UI。

5、[cobra 1.6.0 发布](https://github.com/spf13/cobra)

一个构建现代 CLI APP 的框架。

6、[goa 3.10 发布](https://github.com/goadesign/goa)

一个使用独特的设计优先的方法在 Go 中构建微服务和 API 的框架。

## 文章

1、[31个！Golang常用工具来啦（建议收藏）](https://mp.weixin.qq.com/s/JH6_UB1NJ5HWquN7biBLRQ)

本文主要分享Golang相关的一些使用工具，简单介绍工具作用和使用场景，不会详细介绍其使用，列举的工具也不是最全的，具体可以参考链接或自行搜索学习。

2、[10月榜单：Go 进前 10 一步之遥，Rust 最近很猛](https://mp.weixin.qq.com/s/9pAFkcdfCFzOIZ8MHvbj6Q)

TIOBE 公布了 2022 年 10 月的编程语言排行榜。

3、[通俗易懂！图解Go协程原理及实战](https://mp.weixin.qq.com/s/VtwXu0aerBwgaDJV7i3guw)

本文主要介绍一下线程、协程的原理，以及写成的基本使用，希望能对此方面感兴趣的开发者提供一些经验和启发。

4、[Go：Map 和 内存泄露](https://mp.weixin.qq.com/s/IZbDb60hhY04NyrbdKYU8g)

map 总是可以在内存中增长；它从不收缩。因此，如果它导致一些内存问题，你可以尝试不同的选项，例如强制 Go 重新创建 map 或使用指针。

5、[如何在 Golang 中编写断路器（circuit breaker)](https://mp.weixin.qq.com/s/1v_FGO76bahLvTQlq71iig)

在这篇文章中，我想谈谈一个基于流行的开源项目 hystrix 的 circuit breaker （断路器）模式（实际上，我会看看 golang 版本的hystrix-go，而不是用 Java 编写的原始版本）。

6、[探究 Go 源码中 panic & recover 有哪些坑？](https://mp.weixin.qq.com/s/dN9G4Tnt9HgVqlNh73HNUQ)

本篇文章从一个例子出发，然后讲解了 panic & recover 的源码。

7、[深入理解 Go CPU profiler 内幕](https://mp.weixin.qq.com/s/Jexes21Irb4__9xyTSaOCg)

Go 是那种自带 profiler (分析器)的语言之一。

## 开源项目

1、[cute](https://github.com/zakaria-chahboun/cute)

简洁、漂亮的 fmt 替代包。

2、[opus](https://github.com/pion/opus)

Opus （交互式音频编解码器）的 Go 实现。

3、[go-htmltable](https://github.com/nfx/go-htmltable)

Go 的 HTML 表格数据提取器。

4、[tacquito](https://github.com/facebookincubator/tacquito)

一个用 Go 编写的开源 TACACs+ 服务器，它实现了 RFC8907。

5、[go-simpex](https://github.com/tobiassjosten/go-simpex)

标准库 regexp 替代者，更简单、快速。

## 资源&&工具

1、[autostrada](https://autostrada.dev/)

用于 Go 的闪电般快速的代码库生成。

2、[pagoda](https://github.com/mikestefanello/pagoda)

快速、轻松的全栈 Web 开发初学者工具包。

3、[circumflex](https://github.com/bensadeh/circumflex)

终端查看 Hacker News。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
