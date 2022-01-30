# Go语言爱好者周刊：第 129 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue129/cover.png)

题图：来自 golangweekly

## 刊首语

<https://studygolang.com/interview/question> 上的每日一题，不少人问，如何查看历史题目。这是我故意这么设计的，目的是希望大家能够坚持刷题。

如果你希望能看到历史题目，只需要在当天题目留言，然后在网站「我的主页」也可以找到所有评论过的内容，找到对应题目的入口。当然，后续也许会放出历史题目入口。

如果你有好的 Go 题目，欢迎提交给我！

## 资讯

1、[fsnotify 寻找新的维护者](https://github.com/fsnotify/fsnotify/issues/413)

这是一个流行的 Go 库，用于处理文件系统通知。新的维护者将在 2022 年 2 月 28 日之前接管该项目，否则该项目会归档，不再接受任何修改。

2、[fiber 2.25.0 发布](https://github.com/gofiber/fiber)

一个受 Express.js 启发的 Go Web 框架。

## 文章

[1、Go 为什么选择 Gopher 作为吉祥物？](https://mp.weixin.qq.com/s/7m9gTMyrEitLoWQddMXvzw)

据说，有些人学 Go 是因为 Gopher 这个吉祥物。

2、[Go 并行性和并发性：有什么不同？](https://mp.weixin.qq.com/s/sXvqNgMHiIcZojuxDuYGQw)

并发和并行，Go 刚发布时，官方就不断强调这两点的不同。可能新手依然迷糊。这次给大家弄一个系列，详细讲解并发和并行。

3、[Go 原生并发原语和最佳实践](https://mp.weixin.qq.com/s/rtq5m1HMd47yedwY4i_FvQ)

Go 编程语言是用并发作为一等公民创建的。它是一种语言，通过抽象出语言中并发原语1背后的并行性细节，您可以轻松编写高度并行的程序。

4、[让你在虎年如虎添翼的Go测试工具和技巧](https://mp.weixin.qq.com/s/x8h3GfsoNtdShal7MTgkZw)

文中作者介绍了不少好用的 Go 库和工具。

5、[你要的 Go CheatSheet 这里都有](https://mp.weixin.qq.com/s/02rA4KPSeHNYeqX7-jlUuQ)

关于 Go 的 CheatSheet 和 CheatSheet 站点的介绍。

6、[2021年Go语言盘点：厉兵秣马强技能，蓄势待发新征程](https://tonybai.com/2022/01/16/the-2021-review-of-go-programming-language/)

2021 年围绕 Go 语言项目以及 Go 社区都发生了哪些大事件。

## 开源项目

1、[redix](https://github.com/alash3al/redix)

一个使用 Redis 协议但使用 Postgres 作为其存储引擎的键值存储。

2、[goridge](https://github.com/roadrunner-server/goridge)

使用 PHP 套接字和 Go 的`net/rpc`包来支持从 PHP 调用 Go 服务方法，具有相对较高的性能和低空间占用。

3、[tt](https://github.com/lemnos/tt)

打字测试程序，每分钟告诉你字符和单词数。

4、[apd](https://github.com/cockroachdb/apd)

用于 Go 的任意精度小数工具包。

5、[goes](https://github.com/modernice/goes)

用于在 Go 中编写 event-source 应用程序的工具包。

## 资源&&工具

1、[新的 Go 播客](https://go.transistor.fm/)

自 2014 年以来，作者每天都在写 Go，并决定开始这个播客，将每两周选择一个主题，并提供有关 Go 编程的提示和技巧。

2、[qlmka](https://github.com/remko/qlmka)

如果使用 macOS，应该知晓在 Finder 中的文件上按 Space 可以“快速查看”该文件的内容预览。有趣的是，Go 在这样的插件中使用了（C 提供了 macOS 和 Go 代码之间的接口）并且不需要 Xcode。

3、[litestream](https://github.com/benbjohnson/litestream)

SQLite 的流式复制。

4、[gokrazy](https://github.com/gokrazy/gokrazy)

用于 Raspberry Pi 3 或 4 设备（或 amd64 PC！）的本地 Go 用户空间。

5、[switchboard](https://github.com/Cian911/switchboard)

自动文件组织。

6、[LocklessGenericRingBuffer](https://github.com/GavinClarke0/LocklessGenericRingBuffer)

使用 Go 泛型实现的单生产者和多读取者无锁 ringbuffer。

7、[gogradle](https://github.com/gogradle/gogradle)

一个为 Go 提供全面支持的 Gradle 插件。

8、[Go 播客第 213 期](https://changelog.com/gotime/213)

AI 驱动的 Go 开发。

9、[go-generics-the-hard-way](https://github.com/akutz/go-generics-the-hard-way)

掌握 Go 泛型的实用方法。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
