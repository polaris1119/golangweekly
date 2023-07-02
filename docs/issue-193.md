# Go语言爱好者周刊：第 193 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue193/cover.jpeg)

题图：Go1.21 RC 发布

## 资讯

1、[lingua-go v1.3 发布](https://github.com/pemistahl/lingua-go)

最准确的Go自然语言检测库，长短文本均适用。

2、[cli v4.0 发布](https://github.com/create-go-app/cli)

通过运行一个 CLI 命令，创建一个具有后端、前端和部署自动化的项目。

3、[immudb v1.5.0 发布](https://github.com/codenotary/immudb)

用于系统和应用程序的轻量级高速不可变数据库。

4、[opengist v1.4 发布](https://github.com/thomiceli/opengist)

由 Git 驱动的自我托管的 Pastebin，GitHub Gist 开源替代方案。

5、[MongoDB Go Driver 1.12 发布](https://github.com/mongodb/mongo-go-driver)

MongoDB 的 Go 驱动，官方出品。

5、[quic-go v0.36 发布](https://github.com/quic-go/quic-go)

纯 Go 的 QUIC 实现。

## 文章

1、[Go1.21 RC 发布了！！！](https://mp.weixin.qq.com/s/jpy4cQ0anUrBUPUcb-9G_g)

不要怀疑，为什么没见到 RC1，直接 RC2 了？因为打完 go1.21rc1 后发现了一个 bug，然后修复了，所以直接发布 RC2。（实际上 go 仓库是能看到 RC1 tag 的）

2、[写给go开发者的gRPC教程-metadata](https://mp.weixin.qq.com/s/2BQdYDUDeCpL12S_R1UNPA)

和在普通HTTP请求中一样，gRPC提供了在每一次RPC中携带上下文的结构：metadata。

3、[布隆过滤器 - 实现和特征](https://mp.weixin.qq.com/s/VJ0iBpezlMs-8Ja-FdoW2w)

Go 描述。

4、[用 Go 基于 epoll 实现一个最小化 IO库](https://mp.weixin.qq.com/s/2PBPX2jKhvotW5N3zutVig)

Go圈有很多款异步的网络框架:evio,nbio,gnet,cloudwego/netpoll......

5、[Go1.21 速览：go.mod 的 Go 版本号将会约束 Go 程序构建，要特别注意了！](https://mp.weixin.qq.com/s/9tyiEA7tUZXo_so7-CXfaw)

在这次 Go1.21 的更新中，正式将多年前引入 go.mod 的 Go 行的版本声明使用了起来。

## 开源项目

1、[dkron](https://github.com/distribworks/dkron)

分布式、容错作业调度系统。

2、[objectbox-go](https://github.com/objectbox/objectbox-go)

嵌入式 Go 数据库，SQLite、gorm 等的快速替代品。

3、[errors](https://github.com/morrisxyang/errors)（作者自荐）

Go 优雅的错误处理。

## 资源&&工具

1、[gonb](https://github.com/janpfeifer/gonb)

Jupyter 的 Go Notebook 内核。

2、[tailer](https://github.com/hionay/tailer)

tailer 是一个 CLI 工具，用于在命令输出停止时插入行。

3、[migration-to-go](http://code.sd/books/migration-to-go/)

免费电子书：迁移到 Go。

4、[vanus](https://github.com/vanus-labs/vanus)

一个具有处理能力的无服务器事件流系统。

5、[开源电子书 Effortless Golang](https://github.com/Duffney/effortless-golang)

英文的，目前还没写完。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
