# Go语言爱好者周刊：第 94 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。

本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue094/cover.jpeg)

题图：母亲节快乐！

## 刊首语

今天是母亲节。看到一个视频，说 30 岁了还没结婚，你跟妈妈说母亲节快乐，你觉得她能快乐的起来吗？！扎心了。是不是觉得知识改变命运，耽误结婚了。。。

今天周刊来一道简单的题目。以下代码输出什么？

```go
package main

import (
  "fmt"
)

func main() {
  var ans float64 = 15 + 25 + 5.2
  fmt.Println(ans)
}
```

A：不能编译；B：45；C：45.2；D：45.0

## 资讯

1、[Go1.16.4 发布](https://mp.weixin.qq.com/s/Iw4LeBgD5xxLtUy3mcws-w)

一起发布的还有 1.15.12。

2、[twirp 8.0 发布](https://github.com/twitchtv/twirp)

具有 Protobuf 服务定义的简单 RPC 框架。	

3、[sqlc 1.8 发布](https://github.com/kyleconroy/sqlc)

从 SQL 产生类型安全的 Go 代码。

4、[Ebiten 2.1.0 发布](https://ebiten.org/blog/v2.1.0.html)

主要的新功能是支持系统游标和新密钥常量。

5、[Fiber 2.9.0](https://github.com/gofiber/fiber)

这是一个受 Node 框架 Express.js 启发的 Web 框架。

## 文章

1、[Go 笔试题精选 二： 25 道选择题](https://mp.weixin.qq.com/s/xMXRafxVHud1yyz8GVM3GA)

题目不是太难。

2、[Docker 将 “ 跳过更新 ” 设为付费功能，引发网友吐槽](https://mp.weixin.qq.com/s/csGdmpRmy4GATtBUQevxig)

最近，纽约大学工学院助理教授 Brendan Dolan-Gavitt 在推特上发帖，吐槽 Docker 最新的升级功能。

3、[Go 语言中常见的几种反模式](https://mp.weixin.qq.com/s/KmKvwc0eeUuKAWASnTHBRA)

一篇译文。

4、[「卷」有理论依据：海勒姆定律—Go又是怎么卷的](https://mp.weixin.qq.com/s/I2Rm1d8LbOQg3V_CFSKgtg)

程序员应该掌握的定律。

5、[Go缓存系列之 go-cache](https://mp.weixin.qq.com/s/hz7mViPQIwca0mSylfS-ww)

基于内存的 K/V 存储/缓存 : (类似于 Memcached)，适用于单机应用程序。

[Go: 延长变量的生命周期](https://mp.weixin.qq.com/s/S_lO8jQY0TGS7_zvDIUcfw)

涉及逃逸。

7、[每日一库之实战项目推荐：rosedb](https://mp.weixin.qq.com/s/xl4XFjPwMAkx2F3v18msTg)

网友投稿。

## 开源项目

1、[gocondor](https://github.com/gocondor/gocondor)

用于构建现代 API 的 golang 框架。

2、[gocover](https://github.com/kjellkvinge/gocover)

Go 实现的测试覆盖率分析工具。

3、[lens](https://github.com/lensapp/lens)

Kubernetes IDE。

4、[zenity](https://github.com/ncruces/zenity)

支持 Windows、MacOS 平台的 go zenity 风格对话框库。

5、[SigNoz](https://github.com/SigNoz/signoz)

datadog的开源替代项目，帮助开发人员监控和诊断应用。

![](imgs/issue094/signoz.png)

## 资源&&工具

1、[goyek](https://github.com/goyek/goyek)

用于编写构建流水线的 Go 工具。

2、[fdlr](https://github.com/Imputes/fdlr)

Go 实现的命令行多协议下载工具。

3、[go module 速查表](https://encore.dev/guide/go.mod)

cheatsheet。

4、[go-version-action](https://github.com/marketplace/actions/go-version-action)

Go 版本的 github action。

5、[text-to-video](https://github.com/leoython/text-to-video)

文章转视频 text-to-video。

6、[pixie](https://github.com/pixie-labs/pixie)

实时 Kubernetes 原生应用观察与诊断。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)