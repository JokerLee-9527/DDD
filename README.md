# 欧创新的《DDD实战课》学习笔记

---

学习DDD是有一定难度的，特别是第一次接触，如何进行战略和战术如何结合？很多人都会有这样的疑问.



这里,首先想整理一下DDD的知识点，然后通过一组工程构建一个DDD开发的Demo。水平有限， 有什么不好的地方,期望不吝赐教（lijian79@gmail.com）



## 笔记整理(进行中)

下载 [DDD/StudyNotes at main · JokerLee-9527/DDD · GitHub](https://github.com/JokerLee-9527/DDD/tree/main/StudyNotes)  中的html或者mmap文件.



## DDD的Demo项目组(进行中)

#### 技术栈:

1.第一阶段: springboot(Jpa)、dubbo、mysql、zk、RocketMQ、ELK、Kafka、mongodb   (进行中)

2.第二阶段:分库分表ShardingJdbc   (未开始)

3.第二阶段:全链路跟踪zipkin  (未开始)

(想把自己用到的技术串起来, 构造一套生产上可以使用的模型. 想的比较多.但是时间有限,可能时间比较长.)

#### 项目介绍:

1. DockerSupport项目 (启动项目)  (进行中)
   
   [JokerLee-9527/DDD-DockerSupport · GitHub](https://github.com/JokerLee-9527/DDD-DockerSupport)

2. 

3. Liqubase项目(mysql数据库定义)   (未开始)

4. 前台项目   (未开始)

5. 中台项目  (未开始)

6. 后台项目  (未开始)
   
   会员后台  (未开始)
   
   订单后台  (未开始)

###### 随便说说(可以跳过):

个人希望把后端分为三层,由下往上分别是后台,中台,前台。

1. 后台：负责数据的持久化，这些数据应该都是实体(对象)所固有的，与业务模型耦合度不高的属性。
   这样能保证数据稳定(在大型系统中迁移数据,甚至是大表增减字段都可能遇到问题)

2. 中台：调用后台，负责具体业务模型的编排，是业务的主要实现模块。（如果某个业务下线，可以直接停止中台应用，保证后台的稳定性）

3. 前台：很薄一层，主要为前端提供特殊服务（例如：权限登录等）

在实际中，有些具体的实现会把中台向上合并到前台，或者向下合并到后台。
个人觉得大型系统如果要合并，向上合并到前台比较合适，可以保证数据的稳定。
当然这些都是仁者见仁智者见智。

## 感谢

谢谢易永健

通过欧创新的《DDD实战课》比较系统的梳理的DDD的思路。

对DDD认识还是比较肤浅， 期望各位指摘。（lijian79@gmail.com）