# Go语言爱好者周刊：第 198 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue198/cover.jpeg)

题图：Go1.21 发布

## 资讯

1、[BadgerDB v4.2 发布](https://github.com/dgraph-io/badger)

BadgerDB 是一个用纯 Go 编写的可嵌入，持久和快速键值（KV）数据库。 它是 Dgraph（快速，分布式图数据库）的基础数据库。它打算成为 RocksDB 等非基于 Go 的键值存储的高性能替代品。

2、[validator v10.15.0 发布](https://github.com/go-playground/validator)

该验证器基于标签对结构和单个字段实现值验证。

3、[pop v0.2 发布](https://github.com/charmbracelet/pop)

通过终端发送邮件。

4、[openfga v1.3 发布](https://github.com/openfga/openfga)

一个高性能和灵活的授权/权限引擎。

5、[retry-go v4.5 发布](https://github.com/avast/retry-go)

简单的重试机制包。

6、[kratos v2.7 发布](https://github.com/go-kratos/kratos)

B 站开源的 Go 微服务框架。

## 文章

1、[Go 每日一库之 zap 高性能设计与实现](https://mp.weixin.qq.com/s/6dLtjHbtDRekVHC8G_Rv9w)

zap 是 Uber 开源的 Go 高性能日志库，性能远超于标准库和其他开源日志库。

2、[Go中url.ParseRequestURI和url.Parse函数的踩坑记](https://mp.weixin.qq.com/s/YIz1s5eSXy3t4feSWxJiAg)

实际工作中遇到的问题。

3、[Go 2永远不会给Go 1带去破坏性变化](https://mp.weixin.qq.com/s/FLW0v_3qZOi8GjB3dtDavA)

rsc 说不会破坏。

4、[Go每日一库之 vegeta — http压力测试工具库](https://mp.weixin.qq.com/s/am9dfFLnRE51ETwEnsOu2w)

今天给大家推荐的是一个对HTTP接口做压力测试的工具：vegeta。

5、[在 Go 中正确关闭 HTTP](https://dev.to/mokiat/proper-http-shutdown-in-go-3fji)

直到今天，我仍然遇到在Go中优雅地关闭HTTP服务器时遇到问题的代码。这就是为什么我决定写一篇关于这个的文章。

6、[Go 1.21 中的泛型推断](https://colobu.com/2023/08/18/go1-21-generics/)

Go 1.21 已经发布了，带来了一系列的改进，例如更好的泛型类型推断（本文的内容）;新的内置函数min`,max和clear`;以及标准库中的几个新软件包（maps`,slices`,cmp`,log/slog和testing/slogtest`)。

## 开源项目

1、[oto](https://github.com/ebitengine/oto)

在多个平台上播放声音的低级库。

2、[ensure](https://github.com/iamkoch/ensure)

基于场景的 Go 测试框架。

3、[gonull](https://github.com/lomsa-dev/gonull)

用于轻松处理可为空值的Go包。

4、[queryx](https://github.com/swiftcarrot/queryx)（作者自荐）

支持数据库自动管理的 Go ORM。

5、[mongo-plus](https://github.com/here-Leslie-Lau/mongo-plus)（作者自荐）

简易的mongodb库。

## 资源&&工具

1、[GopherCon UK 2023](https://www.jaminologist.com/gophercon-uk-2023-the-ultimate-review-were-so-back/)

终极回顾 - 我们回来了！

2、[Go 播客第 288 期](https://changelog.com/gotime/288)

深入了解 Go 的堆栈。

3、[开源的代码转换工具（作者自荐）](https://aicodeconvert.com/)

支持：自然语言转代码，描述需求就生成对应的代码；把代码一键转换为另一种代码语言实现。

4、[protoc-gen-validate](https://github.com/giftDad/protoc-gen-validate)（作者自荐）

基于proto文件的注解，为每个 message 生成 validate 函数。

5、[multi-cluster-informer](https://github.com/Kubernetes-Learning-Playground/multi-cluster-informer)

基于golang实现的k8s多集群多资源的简易informer监听。

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
