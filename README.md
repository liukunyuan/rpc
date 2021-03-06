一个简单的RPC框架

RPC（Remote Procedure Call ）——远程过程调用，它是一种通过网络从远程计算机程序上请求服务，而不需要了解底层网络技术的协议。RPC协议假定某些传输协议的存在，如TCP或UDP，为通信程序之间携带信息数据。在OSI网络通信模型中，RPC跨越了传输层和应用层。RPC使得开发包括网络分布式多程序在内的应用程序更加容易。

框架——让编程人员便捷地使用框架所提供的功能，由于RPC的特性，聚焦于应用的分布式服务化开发，所以成为一个对开发人员无感知的接口代理，显然是RPC框架优秀的设计。
题目要求

1.要成为框架：对于框架的使用者，隐藏RPC实现。

2.网络模块可以自己编写，如果要使用IO框架，要求使用netty-4.0.23.Final。

3.支持异步调用，提供future、callback的能力。

4.能够传输基本类型、自定义业务类型、异常类型（要在客户端抛出）。

5.要处理超时场景，服务端处理时间较长时，客户端在指定时间内跳出本次调用。

6.提供RPC上下文，客户端可以透传数据给服务端。

7.提供Hook，让开发人员进行RPC层面的AOP。

注：为了降低第一题的难度，RPC框架不需要注册中心，客户端识别-DSIP的JVM参数来获取服务端IP。 
