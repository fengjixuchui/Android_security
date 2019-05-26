f# Android_security
> 仅为私人的成长笔记，记录下来，聊表心意。
> one crash one day ， graduate one day。
## Android的功能
* Android生态圈
TODO:
* 各个组件，存的漏洞类型，这些漏洞的利用可能性有多大，被利用之后分别会产生什么样的效果
这个放在 各组件漏洞积累里

## 语言
* c、c++、java、javascript、python、scala、smali
* 逆向工程 
  https://beginners.re/RE4B-CN-partial/html/RE4B-CN-partial.html

## 技能

* 看洞

	历史漏洞的git log、bug报告、从非 lib 目录下等

* 识洞

	代码审计

* ctf

	看着做吧

* CVE

## 分析记录

## 动态调试(dynamic)

	软件调试可以分为源码级调试与汇编级调试。源码级调试（代码审计）多用于软件开发阶段，汇编级调试也就是动态调试。

## 代码审计

* 安卓 app
	历史漏洞

    掌握漏洞所在模块或子系统，不看完整的漏洞细节描述，尝试在漏洞版本中找出对应的漏洞
    如果未能找出漏洞，去看漏洞细节描述，对比自己审计过程，看遗漏了哪一步骤
    直到相信：挖洞只是体力消耗，而非能力问题

* 项目所涉及安卓 app

## Fuzzing训练

	已公开的历史漏洞问自己，如何写fuzzer挖掘到此漏洞，如果自己不知道此漏洞，那又能挖掘到呢？不断重复训练并改进fuzzer
	甚至可以来一个议题，叫做： From open-source security to closed-source application
	然后就发现，这个方向可以一直做下去，包括组件的识别啊，版本识别啊，开源闭源对应啊，爬虫扫描啊，漏洞模式，触发路径寻找啊，inter-device fuzzing啊
	搞出个 exploit android app deep from the native world

## 漏洞信息来源

RSS、相关博文 【RSS订阅】TODO 推送吧

### Android知识的正确基础

* 书

> 读书。请一定要读书。这是为了打好Android知识的正确基础。

1. Mark Murphy的《The Busy Coder’s Guide to Android Development》

2. Android Design
  《Devices and Displays》
  《Touch Feedback 》
  《Metrics and Grids》
  《Iconography》
  Best Practices for User Experience & UI (必读)
  Best Practices for Performance
  Displaying Bitmaps Efficiently
  Adding Animations (也可见于NineOldAndroids库)
  Tools help
  SDK Samples

* 订阅博客，通过RSS参与stackoverflow社区。

1. STACKOVERFLOW
  CommonsWare（Mark Murphy)，Dianne Hackborn，Romain Guy，Reto Meier，Trevor Johns，Roman Nurik，Adam Powell

2. 博客
  
> https://android-developers.googleblog.com 
  这个博客的文章非常值得浏览


### 安全会议

  * BlackHat

  > https://www.blackhat.com
  > 这次BlackHat USA的议题也陆续公开了：https://www.blackhat.com/us-19/briefings/schedule/index.html

  * OffensiveCon

  > https://www.offensivecon.org/
  > 会后，一般是由演讲者选择是否公开ppt，多数人是在Twitter上公开的，官网上我没找到资源（https://github.com/riusksk/SecConArchive/tree/master/OffensiveCon2019），所以之前收集的ppt都是从twitter上扒下来的。

  * HITB (Hack In The Box)

  > https://conference.hitb.org/
  > 这几天HITB刚在荷兰阿姆斯特丹举办完，议题PPT也一并公开(https://conference.hitb.org/hitbsecconf2019ams/materials/)。

  * InfiltrateCon

  > https://infiltratecon.com
  >今年的议题涉及Chrome RCE、iOS与Android提权、Pwn TEE、浏览器JS Fuzzing等等，只能坐等官方公开PPT了。

  * Chaos Communication Congress(C3)

  > https://www.ccc.de/
  > 这些议题只有演讲视频公开，没有PPT，官方会放在https://media/ccc.de，可在线或下载观看。
  > 都是在每年的12月份举办，2019的还有半年呢……

  * CanSecWest

  > https://cansecwest.com
  > CanSecWest都是与Pwn2Own一块出现的，以前议题PPT都是放在https://www.slideshare.net/上分享，但从2018年开始又不搞了。
  > 每年议题不多，但质量还是可以的，不过感觉这两年的质量略有下降。
  > 今年3月的议题也没看到有下载，也是混Twitter找ppt的，只看了《vs com.apple.security.sandbox》这个议题，今年我感兴趣的议题没几个，大家根据自己喜好选择吧。

  * MOSEC 移动安全技术峰会

  > http://mosec.org
  > MOSEC是从2015年开始举办的，由盘古与韩国POC联合举办，聚集移动安全领域，包括Android、iOS、IoT以及无线电等领域。虽然起步晚，但议题干货满满的，应该是目前国内最好的安全会议了。
  > 今年的议题也已经陆续公开了，包括iOS越狱、Android提权、LTE、基带、卫星系统等等。
  > 官网是不公开大会的议题PPT，由演讲者选择，所以想学习的同学，可能还是得去参会。

  * POC

  > http://powerofcommunity.net/

### 研究者团队、社区

  * Dianne Hackborn
    Google资深大牛

    > https://www.jianshu.com/p/07b87084337f

    > 关于Android四大组件深刻解读

  * Twttier 

  * 漏洞赏金计划、私有市场 每个国家都有
      Hackone

      > https://github.com/B3nac/Android-Reports-and-Resources

## 漏洞挖掘工具

## 工具与方法论沉淀
   一些漏洞可能需要人工审计，不少漏洞可以自动化Fuzzing，一些能自动化或半自动化实现的，尽量写程序自动化
   * AFL源码解析
   * google search
   * 各组件漏洞积累
   * Android软件安全与逆向分析
   * 强大的IDA
   * 强大的markdown
   * 命令行tips
   * 别人家的 fuzz 思路

## DOING

* Thor
* xxxx（移动app分析）

### Fuzz
* monkey(1个月)
		ffmeg
		chrome

### Reverse 
* RE4B

### 熟悉漏洞
* 各组件漏洞积累
   one crash one day ， graduate one day。
* https://github.com/B3nac/Android-Reports-and-Resources
* 复现搜狗浏览器 
     替换了so 
* 复现blueborne: 
     http://www.ms509.com/2017/11/14/blueborne/ 
     http://go.armis.com/hubfs/BlueBorne%20Technical%20White%20Paper.pdf 
     android.googlesource.com 
         system/bt 

### CTF以及Android安全基础
* https://mobisec.reyammer.io/challs

## Mark
wrike (lib/armeabi-v7a/libnpl-tls.so,execv，Musigy::Platform::PID __fastcall Musigy::Platform::SpawnProcess,涉及到c++ name mangling ref https://blog.csdn.net/yaoyutian/article/details/55209963。类似于Jni，需要自己逆出虚表，手动调)
Mico apk里面的 

Lcom/facebook/ads/internal/hb b（unzip以及dex）

Android软件安全与逆向分析中一些TODO的基础


