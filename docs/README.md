## Overview of AspectCore Project

### 什么是AspectCore Project ?
[AspectCore Project](https://github.com/aspectcore) 是适用于[Asp.Net Core](https://docs.microsoft.com/en-us/aspnet/core/) 平台的轻量级 [Aop(Aspect-oriented programming)](https://en.wikipedia.org/wiki/Aspect-oriented_programming) 解决方案，它更好的遵循Asp.Net Core的模块化开发理念，使用AspectCore可以更容易构建低耦合易扩展的Web应用程序。

在.Net Framework和Asp.Net Framework中，我们可以使用[Castle DynamicProxy](https://github.com/castleproject/Core/blob/master/docs/dynamicproxy.md) 或者CLR提供的 [Remoting.Proxies](https://msdn.microsoft.com/en-us/library/system.runtime.remoting.proxies.aspx)  很容易的实现 [Aop(Aspect-oriented programming)](https://en.wikipedia.org/wiki/Aspect-oriented_programming)。但是在中，我们要实现Aop