# j2ee-study-path

根据自己的工作经验，为哥们写的一个比较完整的j2ee的学习路径。学习周期大约6个月，目标是成为一个合格的SE。文档编写计划大概一个月内，会不断更新修正，会附上一些代码示例。

成为一个合格的SE，个人认为，知识面广而全是首要条件，基础要扎实，要了解原理和设计思想。如果你只是要成为一个能编码的初级人员，这里的很多知识点对你来说可能意义不大，可能长时间用不上。比如，这里会学习servlet容器和springmvc的使用，而很多人觉得有了springboot这些都不需要学习了。但首先很多系统还是在使用springmvc，第二springboot的强包装让你忽略了太多的实现原理和细节，你只懂springboot，说实话很难应对工作中的各种情况。我的风格是知其然知其所以然，只会使用那只是初级阶段。

# 指导思想

知识学习要一步一步来，首先是使用，然后是原理，原理好好理解之后就应该领悟思想，从而融会贯通。初学者不要以为看懂了就能理解思想，这种人有，但不是我。我建议扎扎实实一步一步学习，多敲代码多思考，等你的知识面广了，实现原理理解看多了，自然水到渠成。如果按照正确的道路学习6个月，技术能达到一个质的飞跃，一点都不夸张。而现实中更多的人是混混沌沌编码多年，连门都没有入。

学习过程中，最主要的是自己的实践和思考，而不只是看懂我写的东西。

开始学习的时候应该是全面铺开学习，而不是学完一个再学另外一个，如果你学玩数据结构在学线程，难度太大并且容易变成死记硬背。正确的应该学点这个再学点那个，先开始学的是应用，后面学习的是原理，代码还是那些代码，但自己的认知深度应该越来越深越来越有内涵，死记硬背也变成融会贯通就对了。这个在于自我感觉，自己心里越来越有底就对了，不会以为学到什么新的知识点而欢喜，而不会以为自己不懂什么知识点而害怕，以为你知道最重要的东西是什么，那些你学号了，其他都只是招式而已，一下子就上手了。

另外我这个教程，不是针对一干二净的小白，针对的是有一定的学习和理解能力的人。这里不会教你怎么安装jdk，ide，也不会给你指定第一天学什么第二天学什么。我这里给的方向和重要的知识点，大家应该在方向正确的前提上自己安排自己的学习计划，重点是先广再精，不要一开始就在一个问题上钻太深，功力不到意义不大。


# 大纲

大纲是根据我的工作中用到的我觉得重要的点来写的。肯定不是完整的，大家批判学习吧、

## 基础知识/基础数据结构

- 初级
  - 学习List/Map
    - [如何学习](basic-data-structure/how-to-study.md)
    - ArrayList/LinkedList/HashMap/LinkedHashMap/TreeMap 的使用
  - 序列化的概念和transient关键字
  - 了解注解
- 中级
  - 了解 ArrayList/LinkedList/HashMap的实现原理
  - 了解 ConcurrentHashMap的实现原理
  - 查看java.util包
  - 反射/自省
  - 自定义注解

## 编程能力

这块能力不能忽略，很多人懂很多知识点，却连一个复杂一点的功能都写不出来，归根到底是思维能力太差。我面试Android开发人员的时候，有1/3的人连1到100的加法递归实现都不会写。

初级里面的都是工作中用得上的知识。而中级的，说实话看着高大上，工作中基本用不上，最少我的这么多年工作中，基本没用过。

编程能力里面，最重要是函数的编写，函数的编写里面最主要的输入参数，其次是输出参数，方法名正常人问题不会太大。当你学会了写函数，能写好函数，你的编程之路会越来越轻松。

- 初级
  - 理解oop的思想
  - 实现List
  - 实现二叉树
  - 二叉树遍历
    - 使用递归和循环实现各种遍历
    - 输入叶子节点得到完整路径
- 中级
  - 了解常规算法
    - 动态规划

## 线程/并发

- 初级
  - 线程（概念、方法和状态）
  - synchronize/wait/notify关键字
- 中级
  - 线程池
  - 线程通信
  - ReentryLock的使用
    - 重点阅读BlockingList的源码
- 高级
  - JUC包

## JVM

- 初级
  - 引用的4中类型和OOM关系
  - volatile关键字使用
  - final关键字使用
  - 理解java的传值
- 中级
  - volatile关键字语义
  - final关键字语义
  - OOM的多种类型
  - GC日志的阅读分析
  - dump文件分析
- 高级


## j2ee 容器

- 初级
  - servlet容器
    - 编写filter/servlet处理请求
      - 不使用数据库，直接用List/Map来处理数据
    - 返回json数据
    - 模板返回试图数据
- 中级
  - 实现登录功能
  - springmvc框架使用
    - ORM/Hibernate的使用
    - 理解IOC/AOP
  - springboot框架使用
- 高级
  - 参考我的代码框架

## 网页开发

网页开发东西太多，难度也很大。这里不做重点讲解，只是了解基础知识。SE需要知道网页的基本工作原理。

- 初级
  - 了解js/css/html
  - 使用jquery+BootStrap+模板实现功能
  - http协议，重点了解post/get协议
  - rest接口测试插件使用
- 中级
  - vuejs+BootStrap+Axois实现功能
  - http协议返回码
  - http basic 认证
  - session/cookie
    - cookie的坑
- 高级
  - webpack打包
  - 跨域

## 部署架构

部署架构知识是SE的重中之重，但很多人这块认知非常差。不过好消息就是这块很简单，主要是概念的理解和配置而已，没有太多动脑子的地方。

- 初级
  - 了解基本部署结构图
  - 了解nginx/tomcat作用
  - 了解AJP
- 中级
  - 概念了解
    - 虚拟主机概念
    - 负载均衡概念
    - 反向代理概念
  - 使用nginx配置负载均衡
  - 配置反向代理

## 设计模式

设计模式很多人奉若圭臬，但我个人却没有啥感觉，工作中作用也没有那么大。个人觉得设计模式不应该孤立学习，孤立学习看着不难，但感觉容易变成死记硬背。建议是在理解实现的时候领悟设计模式，重点理解几种常用和好用的设计模式即可。

- 初级
  - 设计模式预览
  - 重点的几种设计模式
- 中级
  - 重点的几种设计模式在实际中的应用
  - spring的设计模式 

## 函数式编程

函数式编程是相对于命令式编程的另外一种思想。是非常重要的一种思维、编码方式，很多语言都有，尤其前台开发里面。

- 初级
  - 概念理解
  - 使用
    - 函数式接口
    - 各种方法
- 中级
  - 概念深入理解
  - 实现原理理解
- 高级
  - jvm实现

## 工具使用

工具使用都是初级知识，并没有难点。难点在其他地方。

- 初级
  - jdk自带工具使用
  - 反编译工具
- 中级
  - 压力测试工具使用
  - 内存分析工具使用