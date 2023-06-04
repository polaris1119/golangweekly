# Go语言爱好者周刊：第 189 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue189/cover.png)

题图：Go 实现的模拟器 <https://github.com/maxpoletaev/dendy>

## 资讯

1、[html-to-markdown v1.4 发布](https://github.com/JohannesKaufmann/html-to-markdown)

使用 Go 将 HTML 转换为 Markdown。它使用 [HTML 解析器](https://github.com/PuerkitoBio/goquery)来尽可能避免使用 regexp。这样可以避免某些奇怪的情况，并允许将其用于完全未知输入的情况。

2、[joker v1.1 发布](https://joker-lang.org/)

Go 实现的 Clojure 解释器。

3、[Beego v2.1 发布](https://github.com/beego/beego)

一个 Web 框架。

4、[maddy v0.7.0 发布](https://github.com/foxcpp/maddy)

SMTP email 服务器。

## 文章

1、[为什么取消了Go1.21，而采用了Go1.21.0的版本命名规则](https://mp.weixin.qq.com/s/-HXqQQcMr1CA4c6SS51yLQ)

你支持这种方式吗？

、[Go 标准库中隐藏了一个文件类型识别的宝贝](https://mp.weixin.qq.com/s/spUKBQB_Ig6ANabbP4FG8g)

文件类型识别是在很多应用场景中都需要用到的功能，本文介绍标准库的方法。

、[filetype: 一个基于 Go 语言的文件类型鉴别神器](https://mp.weixin.qq.com/s/tOlhhT2Abmv2_QSJTqXqSQ)

一个 Go 语言的第三方库，可以根据文件的魔数（magic numbers）签名来推断文件的类型和 MIME 类型。

4、[channel 的 15 条规则和底层实现](https://mp.weixin.qq.com/s/AsytcOBg0XpTnPzDq7iEhQ)

本文主要分析 channel 的内部实现中的数据结构和算法。

、[Go 每日一库之 redis官网推荐的go版本的分布式锁：redsync](https://mp.weixin.qq.com/s/yXbEMTsZEgLWZuZgrFPXSg)

给大家推荐的是基于 redis 的 Go 版本的分布式锁工具：redsync。

## 开源项目

1、[junodb](https://github.com/paypal/junodb)

JunoDB 是 PayPal 自行开发的安全、一致且高度可用的键值存储，可在任何规模下提供低（数毫秒的）延迟。

2、[versioninfo](https://github.com/carlmjohnson/versioninfo)

从 runtime/debug.ReadBuildInfo() 解析版本信息的包。这里有一个篇介绍文章：<https://blog.carlmjohnson.net/post/2023/golang-git-hash-how-to/>。

3、[gut](https://github.com/tompston/gut)

一个将 Golang 结构体转换为 Typescript 接口的工具。这个库也有类似功能：<https://github.com/gzuidhof/tygo>。

4、[quic-go](https://github.com/quic-go/quic-go)

纯 Go 的 QUIC 实现。

5、[ftp](https://github.com/jlaffaye/ftp)

ftp 客户端。

## 资源&&工具

1、[grank](https://www.grank.io/)

搜索 Go 库，查看 star 排行、依赖等信息。源码是 Go 语言实现的：<https://github.com/hullarb/grank>。

2、[ls-lint](https://github.com/loeffel-io/ls-lint)

一个非常快速的目录和文件名检查器，用于前端项目。

3、[dendy](https://github.com/maxpoletaev/dendy)

Go 实现的 NES/Famicom 模拟器。

4、 [trzsz-ssh](https://github.com/trzsz/trzsz-ssh) （作者投稿）

Go 实现的 ssh 客户端（千行左右的代码），已实现 ssh 客户端常用的基本功能。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
