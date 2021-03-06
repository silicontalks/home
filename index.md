---
layout: default
---

## 关于

本站点希望能够为国内的RISC-V开发者和爱好者提供便利。

----

## RISC-V双周简报

国内的RISC-V爱好者利用Github协作的方式，以双周简报的方式为大家带来最新的RISC-V相关咨询，同时在微信公众号和CNRV站点上发布。内容覆盖RISC-V邮件列表、行业新闻、项目进展以及各类点评。也欢迎大家关注CNRV公众号获取最新信息。

- **2017-09-14**: [硬件公司真的越来越像一个软件公司？你怎么看？](bi-week-rpts/2017-09-14)
- 2017-08-31: [越来越多的开源软件支持RISC-V!](bi-week-rpts/2017-08-31)
- 2017-08-17: [感觉RV就要引爆了！小编手已断!](bi-week-rpts/2017-08-17)
- 2017-08-03: [光有Chisel还不够，又来一个SpinalHDL，Scala我真心看不懂啊！](bi-week-rpts/2017-08-03)
- 2017-07-20: [进主线这事儿能走后门吗?](bi-week-rpts/2017-07-20)
- 2017-07-06: [ARM~ARM~你不要怕~](bi-week-rpts/2017-07-06)
- 2017-06-21: [你们心心念念的RV32E终于来了~](bi-week-rpts/2017-06-21)

----

## 资源列表

### [RISC-V 资料搜集页面](resource)

----

## 如何在国内快速搭建SiFive的Freedom环境

### 下载freedom/rocket-chip/riscv-tools完整压缩包

因为国内用户访问github比较慢，而且clone过后submodule更加慢，以下的压缩包是在clone了[freedom](https://github.com/sifive/freedom)之后，执行`git submoudle update --init --recursive`之后打包的。所以已经以submodule的形式包含了rocket-chip和riscv-tools以及下面的诸多submodules。

网盘中还新增了[freedom-e-sdk](https://github.com/sifive/freedom-e-sdk)和[freedom-u-sdk](https://github.com/sifive/freedom-u-sdk)的完整压缩包。

- [百度网盘freedom/rocket-chip/riscv-tools完整打包文件](https://pan.baidu.com/s/1eR80gMY)
    - GitHash: [ec70d85](https://github.com/sifive/freedom/commit/ec70d85cbc03ce5b497b58d1b0f50f39a3e2a4e3)
    - MD5Sum: b3643841ff41083f004871359dd3ffe4
    - 打包时间: 2017-Aug-19
- [百度网盘freedom-e-sdk完整打包文件](https://pan.baidu.com/s/1qYa6fd6)
    - GitHash: [fcbcd44](https://github.com/sifive/freedom-e-sdk/commit/fcbcd440a0556b90bb7f6a739ac567d5f8e93fa2)
    - MD5Sum: 1b5c97dd71918cfaa1c43fb7f38ecade
    - 打包时间: 2017-Aug-20
- [百度网盘freedom-u-sdk完整打包文件](https://pan.baidu.com/s/1mi9kjiw)
    - GitHash: [b38f7c9](https://github.com/sifive/freedom-u-sdk/commit/b38f7c9)
    - MD5Sum: ec7f3f73c23f228a2dfa5fd5030dfffd
    - 打包时间: 2017-Aug-10

下载成功之后执行：

~~~
$ tar xzvf freedom.tar.gz
$ cd freedom
$ git submodule update --init --recursive

# 如果需要更新到最新，可以执行
$ git pull origin master
~~~

### 利用国内镜像加速sbt

目前Aliyun提供了Maven的镜像可以用来加速在构建`rocket-chip`或是`freedom`过程中的`sbt`的运行。

可以在Ubuntu上的~/.sbt/repositories中加入以下内容

~~~
[repositories]
  local
  aliyun: http://maven.aliyun.com/nexus/content/groups/public/
  sbt-releases-repo: http://repo.typesafe.com/typesafe/ivy-releases/, [organization]/[module]/(scala_[scalaVersion]/)(sbt_[sbtVersion]/)[revision]/[type]s/[artifact](-[classifier]).[ext]
  sbt-plugins-repo: http://repo.scala-sbt.org/scalasbt/sbt-plugin-releases/, [organization]/[module]/(scala_[scalaVersion]/)(sbt_[sbtVersion]/)[revision]/[type]s/[artifact](-[classifier]).[ext]
  central: http://repo1.maven.org/maven2/
~~~

参考： [Scala 的构建工具 SBT 镜像设置](http://www.jianshu.com/p/c8c48b0b3866)

**以上sbt镜像功能还需要充分验证，请各位给出反馈**

### 二进制包

- [百度网盘 riscv32-unknown-gcc-6.1.0](https://pan.baidu.com/s/1kV7QJkj) *provided by 胡振波*

----

## oschina镜像服务

在提供压缩包的同时，我们在[oschina](http://git.oschina.net)上镜像了主要的RISC-V工程。 我们利用国外服务器定期同步oschina上的镜像，方便大家获得最新的更新。
相比压缩包，镜像服务器同步了更多的RISC-V相关GitHub工程，包括freechipsproject, riscv, ucb-bar和lowrisc的所有工程。
镜像服务器的具体使用方法请参考[clone-helpers](https://github.com/cnrv/clone-helpers/blob/master/README.md)工程。

----

**欢迎关注微信公众号CNRV，接收最新最时尚的RISC-V讯息！**

![CNRV微信公众号](https://cnrv.io/assets/images/cnrv_qr.png)
