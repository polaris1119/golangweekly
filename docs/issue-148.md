# Go语言爱好者周刊：第 148 期

这里记录每周值得分享的 Go 语言相关内容，周日发布。本周刊开源（GitHub：[polaris1119/golangweekly](https://github.com/polaris1119/golangweekly)），欢迎投稿，推荐或自荐文章/软件/资源等，请[提交 issue](https://github.com/polaris1119/golangweekly/issues) 。

鉴于一些人可能没法坚持把英文文章看完，因此，周刊中会尽可能推荐优质的中文文章。优秀的英文文章，我们的 GCTT 组织会进行翻译。

![](imgs/issue148/cover.jpeg)

题图：Go 在 GitHub 上超过了 100000 颗星星，值得庆祝这一里程碑！

## 刊首语

上期的题目，真的惨不忍睹！

以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	var nums1 []interface{}
	nums2 := []int{1, 3, 4}
	nums3 := append(nums1, nums2...)
	fmt.Println(len(nums3))
}
```

A：3；B：1；C：4；D：编译失败

正确答案是 D，编译失败，只有 15% 的人做对了。看到错误信息应该知晓为什么了：

```bash
cannot use nums2 (variable of type []int) as type []interface{} in argument to append
```

看下本期的题目。以下代码输出什么？

```go
package main

import (
	"fmt"
)

func main() {
	m := [...]int{
		'a': 1,
		'b': 2,
		'c': 3,
	}
	m['a'] = 3
	fmt.Println(len(m))
}
```

A：3；B：4；C：100；D：编译失败

## 资讯

1、[Go1.19 Beta1 发布](https://tip.golang.org/doc/go1.19)

这是基本完成了的 Release Notes。

2、[fyne 2.2.0 发布](https://github.com/fyne-io/fyne)

基于 Material Design 的 Go 跨平台 GUI。

3、[HugoConf 大会](https://hugoconf.io/)

会议在 7 月 8、9 两天进行，在线免费会议。

4、[ddosify 0.8 发布](https://github.com/ddosify/ddosify)

Go 实现的高性能压测工具。

5、[SFTPGo 2.3.0 发布](https://github.com/drakkan/sftpgo)

Go 实现的功能齐全的 SFTP 服务器。

6、[regexp 性能提升](https://github.com/golang/go/commit/0293c51bc5d8ca0728913c4b7f9f92339f8fd9a6)

在 Go1.19 中体现。

## 文章

1、[提高效率的 5 个 GoLand 快捷键，你都知道吗？](https://mp.weixin.qq.com/s/5-ebv0lxEM8ZMiOXYYPsoQ)

分享一些预定义的按键映射供您选择，并介绍几个必备快捷键用法。只需要记住这 5 个基本的快捷键操作，就能有事半功倍的效果。

2、[PHP 跌出前 10，Go 机会来了？6 月 TIOBE 榜单](https://mp.weixin.qq.com/s/DlvMClQorruvF0FetDdl4w)

TIOBE 出炉了 2022 年 6 月份的编程语言趋势榜单。

3、[使用BPF, 将Go网络程序的吞吐提升8倍](https://colobu.com/2022/06/05/use-bpf-to-make-the-go-network-program-8x-faster/)

经典的bpf(classical Berkeley Packet Filter) 是非常好用的一个技术，在一些特殊的Go底层网络编程的场合，可以很好的提高性能。

4、[Go 官方调查变频繁了：6 月份开启新的调查，参与下吧](https://mp.weixin.qq.com/s/8zJQTIClQL7DaEnItdUlHg)

Go 不断提升。

5、[Gopher 应该记住这 10 个命令](https://mp.weixin.qq.com/s/UIeIBtC9MZJh3w-EphWHiA)

Go 最近真的起飞了。越来越多的公司采用它，开发人员也普遍接受它，因为它易于学习，功能强大。

## 开源项目

1、[mo](https://github.com/samber/mo)

一个为函数式编程爱好者准备的，基于泛型构建。

2、[garr](https://github.com/line/garr)

高性能、线程安全、无锁的 Go 数据结构。

3、[SyMon](https://github.com/dhamith93/SyMon)

简单的系统监控和报警系统。

4、[gofound](https://github.com/newpanjing/gofound)

go语言全文检索引擎，毫秒级查询。

## 资源&&工具

1、[benthos](https://github.com/benthosdev/benthos)

流处理。

2、[gta](https://github.com/digitalocean/gta)

通过传递分析快速找到依赖关系发生变化的包。

3、[durationlint](https://github.com/vigliag/durationlint)

专门针对 time.Duration 的 lint。

4、[rain](https://github.com/cenkalti/rain)

一个 BitTorrent 客户端。

5、[Kratos](https://github.com/ory/kratos)

云原生身份和用户管理系统

## 订阅

这个周刊每周日发布，同步更新在[Go语言中文网](https://studygolang.com/go/weekly)和[微信公众号](https://weixin.sogou.com/weixin?query=Go%E8%AF%AD%E8%A8%80%E4%B8%AD%E6%96%87%E7%BD%91)。

微信搜索"Go语言中文网"或者扫描二维码，即可订阅。

![wechat](imgs/wechat.png)
