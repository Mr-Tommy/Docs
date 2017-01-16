## AspectCore Project 简介

### 什么是AspectCore Project ?
[AspectCore Project](https://github.com/aspectcore) 是适用于[Asp.Net Core](https://docs.microsoft.com/en-us/aspnet/core/) 平台的轻量级 [Aop(Aspect-oriented programming)](https://en.wikipedia.org/wiki/Aspect-oriented_programming) 解决方案，它更好的遵循Asp.Net Core的模块化开发理念，使用AspectCore可以更容易构建低耦合、易扩展的Web应用程序。

### 为什么要设计AspectCore ?
在传统.Net Framework和Asp.Net Framework中，我们使用[Castle DynamicProxy](https://github.com/castleproject/Core/blob/master/docs/dynamicproxy.md) 或者CLR提供的 [Remoting.Proxies](https://msdn.microsoft.com/en-us/library/system.runtime.remoting.proxies.aspx)  可以轻松的实现 Aop 来分离关注点从而降低业务逻辑和基础框架功能的耦合。然而在Asp.Net Core中，不仅缺乏细粒度的Aop支持(`Middleware`和`Filter`都是Asp.Net Core的内置Aop实现，但仅适合在Web层使用)，Castle也迟迟未能友好的支持Asp.Net Core。

因此 AspectCore 提供了一个全新的轻量级和模块化的Aop解决方案，下面是AspectCore的基本特性：
* 提供抽象的Aop接口，基于该接口，可以轻松的使用自己的代理类实现替换默认的实现
* 框架不包含IoC，也不依赖具体的IoC实现，可以使用Asp.Net Core的[内置依赖注入](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection)或任何兼容 Asp.Net Core的第三方IoC来集成 AspectCore 到 Asp.Net Core 应用程序中
* 高性能的异步拦截器系统
* 灵活的配置系统
* 基于`Service`的而非基于实现类的切面构造
* 支持跨平台的Asp.Net Core环境

### AspectCore Project 架构设计
<img src="images/aspectcofe-architecture.png" alt="深入理解C#" height="320"/>

从上图可以看出，[AspectCore Abstractions](https://github.com/AspectCore/Lite.Abstractions) 是AspectCore Project的核心，向下通过IoC来集成到Asp.Net Core应用程序中，向上提供配置系统，动态代理系统，模型验证系统以及更多的扩展系统。

目前已完成的组件包括：
* [AspectCore.Lite.Abstractions](http://www.nuget.org/packages/AspectCore.Lite.Abstractions/) 提供Aop的抽象接口
* [AspectCore.Lite.Abstractions.Resolution](http://www.nuget.org/packages/AspectCore.Lite.Abstractions.Resolution/) 默认的Aop实现
* [AspectCore.Lite.Container.DependencyInjection](http://www.nuget.org/packages/AspectCore.Lite.Container.DependencyInjection/) AspectCore的DependencyInjection支持
* [AspectCore.Lite.Container.Autofac](AspectCore.Lite.Container.Autofac) AspectCore的Autofac支持


















