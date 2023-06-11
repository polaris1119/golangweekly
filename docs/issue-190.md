# Go语言爱好者周刊：第 190 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue190/cover.jpeg)

题图：When，自然语言解析时间，可惜不支持中文 <https://github.com/olebedev/when>。

## 资讯

1、[goxygen v0.4 发布](https://github.com/Shpota/goxygen)

分分钟生成一个全栈 Web 项目（Go，Angular/React/Vue）。

2、[miller v6.8 发布](https://github.com/johnkerl/miller)

文本数据处理的瑞士军刀，Go 实现。

3、[wazero v1.2 发布](https://github.com/tetratelabs/wazero)

零依赖的 WebAssembly 运行时库。

4、[go-quartz v0.7 发布](https://github.com/reugn/go-quartz)

小型、零依赖的调度库，启发自 Java 的 Quartz。

5、[connect-go v1.8.0 发布](https://github.com/bufbuild/connect-go)

一个更好的 gRPC。

6、[FerretDB v1.3.0 发布](https://github.com/FerretDB/FerretDB)

MongoDB 的替代品。

7、[go-openai v1.10 发布](https://github.com/sashabaranov/go-openai)

OpenAI 的 Golang SDK，包括 ChatGPT、GPT-3、GPT-4 等。

## 文章

1、[Go1.21.0 新特性：不需要循环 delete map 元素了](https://mp.weixin.qq.com/s/rxxQhrVk3_4ZvTjsIJbstw)

内置函数 clear。

2、[Go1.20.5 发布：更新了什么？](https://mp.weixin.qq.com/s/XykWqJFM3LpGAa1Z8d15HA)

同时发布的还有 Go1.19.10。

3、[Go 这么不稳？TIOBE 6 月榜单发布！](https://mp.weixin.qq.com/s/BmkECfpBlRoFedlh8B6-XA)

稳定进入前 10 还是挺难的。

4、[收藏！！！一图掌握 Go 中 IO 包的关系](https://mp.weixin.qq.com/s/cjQyDdIgcdzj7LOeZf21bQ)

在知乎上看到这样一个问题：Golang的IO库那么多，我该怎么选。今天就跟大家聊聊这个问题。

## 开源项目

1、[when](https://github.com/olebedev/when)

一个自然语言日期/时间解析器，可以使用可插拔的规则和合并策略。它可以识别和处理类似于 “on next wednesday at 2:25 p.m.” 的文本，并将其转换为 time.Time 类型。它支持英语、俄语和巴西葡萄牙语的规则，也可以自定义规则和选项。

2、[pnutmux](https://gitlab.com/fruitygo/pnutmux)

一个使用正则表达式匹配和处理 HTTP 请求的 Web 框架。

3、[email-verifier](https://github.com/AfterShip/email-verifier)

一个用 Go 语言编写的电子邮件验证库，可以在不发送任何邮件的情况下验证电子邮件地址的有效性和可达性。

4、[grpc-gateway](https://github.com/grpc-ecosystem/grpc-gateway)

gRPC 到 JSON 代理生成器。

5、[goipc](https://gitee.com/mqyqingkong/goipc) （作者自荐）

一个轻量的 IPC 组件。

6、[ringbuf](https://github.com/JamesYYang/ringbuf) （作者自荐）

一个 RingBuffer 的 Go 实现，基于 channel。

## 资源&&工具

1、[Go Time 第 278 期](https://changelog.com/gotime/278)

Go 项目的文件和文件夹。

2、[local-git-contributions-visualizer](https://github.com/abdullah-alaadine/local-git-contributions-visualizer)

扫描本地 Git 仓库并生成一个可视化的贡献图。这个工具对于使用多个Git服务（如 Github 和 Gitlab）的开发者很有用，它可以让他们看到他们在不同平台上的贡献情况，即使没有网络连接也可以。

3、[batch-image-generator](https://github.com/codenoid/batch-image-generator)

批量图片生成器。

4、[GopherChina 2023](https://github.com/studygolang/conference/tree/master/2023)

PPT 下载。

5、[gvc](https://github.com/moqsien/gvc) （作者自荐）

一个功能丰富的全平台辅助开发工具。

6、[apicat](https://github.com/apicat/apicat)

使用 Go + Vue + openapi 实现的一套开源接口管理工具，支持 openapi 导入导出。afocus 推荐。

7、[1Panel](https://github.com/1Panel-dev/1Panel)（作者自荐）

开源的 Linux 服务器运维管理面板。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
