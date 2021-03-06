# 什么是akka

## 可拓展的实时事务处理

我们相信编写出正确的具有容错性和可扩展性的并发程序非常困难。大多数时候这是因为我们使用了错误的工具和错误的抽象级别。Akka就是为了改变这种状况而生的。
通过使用Actor模型我们提升了抽象级别，为构建正确的可扩展并发应用提供了一个更好的平台。在容错性方面，我们采取了“let it crash”（让它崩溃）模型，
人们已经将这种模型用在了电信行业，构建出“自愈合”的应用和永不停机的系统，取得了巨大成功。Actor还为透明的分布式系统以及真正的可扩展高容错应用的基础提供了抽象。

Akka是开源项目，可以通过Apache 2许可获得

你可以在[官方网站](http://akka.io/downloads/)下载akka

## Akka实现了独特的混合模型

### Actors

Actors提供给你如下功能：

- 对并发和并行程序的简单的、高级别的抽象。
- 异步的、非阻塞的、高性能的事件驱动编程模型。
- 非常轻量的事件驱动处理（每GB内存可容纳几百万个actors）

### 容错

- 使用“let-it-crash”语义和监管者树形结构来实现容错。
- 监管者树形结构可以跨多个JVM来提供真正的高容错系统。
- 编写永不停机、自愈合的高容错系统非常优秀。

### 位置透明性

Akka的所有元素都为分布式环境而设计：所有actor都仅通过发送消息进行互操作，所有操作都是异步的。

### 持久化

actor在启动或者重启时，它接收的消息可以被选择性的持久化或者置换。这可以允许actors恢复它们的状态，甚至是在jvm出现冲突之后或者是迁移到另一个节点之后。

## Akka可以以两种不同的方式来使用

- 以库的形式：在web应用中使用，放到` WEB-INF/lib` 中或者作为一个普通的Jar包放进classpath目录。
- 以微内核的形式：你可以将应用放进一个独立的内核。


