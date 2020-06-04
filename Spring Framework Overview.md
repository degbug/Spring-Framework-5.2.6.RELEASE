# Spring Framework Overview

<!-- tabs:start -->

#### ** English **

Spring makes it easy to create Java enterprise applications. It provides everything you need to embrace the Java language in an enterprise environment, with support for Groovy and Kotlin as alternative languages on the JVM, and with the flexibility to create many kinds of architectures depending on an application’s needs. As of Spring Framework 5.1, Spring requires JDK 8+ (Java SE 8+) and provides out-of-the-box support for JDK 11 LTS. Java SE 8 update 60 is suggested as the minimum patch release for Java 8, but it is generally recommended to use a recent patch release.
#### ** Chinese **

Spring使创建Java企业级应用变得更加容易。它提供了在企业环境中拥抱Java语言所需的一切，支持Groovy和Kotlin作为JVM上的替代语言，并根据应用程序的需要灵活地创建多种架构。从Spring Framework 5.1开始，Spring需要JDK 8+（Java SE 8+），并提供了对JDK 11 LTS的开箱即用支持。建议将Java SE 8更新60作为Java 8的最低补丁版本，但一般建议使用最近的补丁版本。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring supports a wide range of application scenarios. In a large enterprise, applications often exist for a long time and have to run on a JDK and application server whose upgrade cycle is beyond developer control. Others may run as a single jar with the server embedded, possibly in a cloud environment. Yet others may be standalone applications (such as batch or integration workloads) that do not need a server.
#### ** Chinese **

Spring支持的应用场景非常广泛。在大型企业中，应用程序往往存在很长时间，必须在JDK和应用服务器上运行，其升级周期超出了开发人员的控制范围。其他的应用程序可能是以单个jar的形式运行，并嵌入服务器，可能是在云环境中运行。还有一些可能是独立的应用程序（如批处理或集成工作负载），不需要服务器。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring is open source. It has a large and active community that provides continuous feedback based on a diverse range of real-world use cases. This has helped Spring to successfully evolve over a very long time.
#### ** Chinese **

Spring是一个开放的源代码。它拥有一个庞大而活跃的社区，根据不同的现实世界用例提供持续的反馈。这帮助Spring在很长一段时间内成功地实现了进化。

<!-- tabs:end -->


## **1. What We Mean by "Spring"** 

<!-- tabs:start -->

#### ** English **

The term "Spring" means different things in different contexts. It can be used to refer to the Spring Framework project itself, which is where it all started. Over time, other Spring projects have been built on top of the Spring Framework. Most often, when people say "Spring", they mean the entire family of projects. This reference documentation focuses on the foundation: the Spring Framework itself.
#### ** Chinese **

"Spring "这个词在不同的语境下有不同的含义。它可以用来指的是Spring框架项目本身，也就是它的起源。随着时间的推移，其他的Spring项目都建立在Spring框架之上。大多数情况下，当人们说 "Spring "时，他们指的是整个项目家族。这篇参考文献主要介绍的是基础：Spring框架本身。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The Spring Framework is divided into modules. Applications can choose which modules they need. At the heart are the modules of the core container, including a configuration model and a dependency injection mechanism. Beyond that, the Spring Framework provides foundational support for different application architectures, including messaging, transactional data and persistence, and web. It also includes the Servlet-based Spring MVC web framework and, in parallel, the Spring WebFlux reactive web framework.
#### ** Chinese **

Spring框架被划分为多个模块。应用程序可以选择自己需要哪些模块。核心是核心容器的模块，包括配置模型和依赖注入机制。除此之外，Spring框架还为不同的应用架构提供了基础支持，包括消息传递、事务性数据和持久化以及web。它还包括基于Servlet的Spring MVC Web框架，以及与之并行的Spring WebFlux反应式Web框架。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

A note about modules: Spring’s framework jars allow for deployment to JDK 9’s module path ("Jigsaw"). For use in Jigsaw-enabled applications, the Spring Framework 5 jars come with "Automatic-Module-Name" manifest entries which define stable language-level module names ("spring.core", "spring.context" etc) independent from jar artifact names (the jars follow the same naming pattern with "-" instead of ".", e.g. "spring-core" and "spring-context"). Of course, Spring’s framework jars keep working fine on the classpath on both JDK 8 and 9+.
#### ** Chinese **

关于模块的说明。Spring的框架jar允许部署到JDK 9的模块路径（"Jigsaw"）。为了在支持Jigsaw的应用程序中使用，Spring Framework 5的jar自带 "Automatic-Module-Name "清单条目，它定义了独立于jar artifact名称的稳定的语言级模块名称（"spring.core"、"spring.context "等）（jar遵循相同的命名模式，用"-"代替"."，例如 "spring-core "和 "spring-context"）。当然，Spring的框架jar在JDK 8和9+的classpath上都能正常工作。

<!-- tabs:end -->


## **2. History of Spring and the Spring Framework** 

<!-- tabs:start -->

#### ** English **

Spring came into being in 2003 as a response to the complexity of the early [J2EE](https://en.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition) specifications. While some consider Java EE and Spring to be in competition, Spring is, in fact, complementary to Java EE. The Spring programming model does not embrace the Java EE platform specification; rather, it integrates with carefully selected individual specifications from the EE umbrella:
#### ** Chinese **

作为对早期[J2EE](https://en.wikipedia.org/wiki/Java_Platform,_Enterprise_Edition)规范的复杂性的回应，Spring于2003年诞生。虽然有些人认为Java EE和Spring是竞争关系，但实际上，Spring是Java EE的补充。Spring的编程模型并不包含Java EE平台规范，相反，它与EE保护伞中精心挑选的单独规范进行了整合。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- Servlet API ([JSR 340](https://jcp.org/en/jsr/detail?id=340))

- WebSocket API ([JSR 356](https://www.jcp.org/en/jsr/detail?id=356))

- Concurrency Utilities ([JSR 236](https://www.jcp.org/en/jsr/detail?id=236))

- JSON Binding API ([JSR 367](https://jcp.org/en/jsr/detail?id=367))

- Bean Validation ([JSR 303](https://jcp.org/en/jsr/detail?id=303))

- JPA ([JSR 338](https://jcp.org/en/jsr/detail?id=338))

- JMS ([JSR 914](https://jcp.org/en/jsr/detail?id=914))

- as well as JTA/JCA setups for transaction coordination, if necessary.

#### ** Chinese **

- Servlet API ([[JSR 340](https://jcp.org/en/jsr/detail?id=340))

- WebSocket API ([[JSR 356](https://www.jcp.org/en/jsr/detail?id=356))

- 并发实用工具([[JSR 236](https://www.jcp.org/en/jsr/detail?id=236))

- JSON绑定API ([[JSR 367](https://jcp.org/en/jsr/detail?id=367))

- Bean验证([[JSR 303](https://jcp.org/en/jsr/detail?id=303))

- JPA([[JSR 338](https://jcp.org/en/jsr/detail?id=338))

- JMS([[JSR 914](https://jcp.org/en/jsr/detail?id=914))

- 以及JTA/JCA设置，必要时进行交易协调；


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

The Spring Framework also supports the Dependency Injection ([JSR 330](https://www.jcp.org/en/jsr/detail?id=330)) and Common Annotations ([JSR 250](https://jcp.org/en/jsr/detail?id=250)) specifications, which application developers may choose to use instead of the Spring-specific mechanisms provided by the Spring Framework.
#### ** Chinese **

Spring框架还支持依赖注入([[JSR 330](https://www.jcp.org/en/jsr/detail?id=330))和通用注释([[JSR 250](https://jcp.org/en/jsr/detail?id=250)))规范，应用程序开发人员可以选择使用这些规范来代替Spring框架提供的Spring专用机制。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

As of Spring Framework 5.0, Spring requires the Java EE 7 level (e.g. Servlet 3.1+, JPA 2.1+) as a minimum - while at the same time providing out-of-the-box integration with newer APIs at the Java EE 8 level (e.g. Servlet 4.0, JSON Binding API) when encountered at runtime. This keeps Spring fully compatible with e.g. Tomcat 8 and 9, WebSphere 9, and JBoss EAP 7.
#### ** Chinese **

从Spring Framework 5.0开始，Spring至少需要Java EE 7级别（如Servlet 3.1+、JPA 2.1+），同时在运行时遇到Java EE 8级别的新API（如Servlet 4.0、JSON Binding API）时，提供开箱即用的集成。这使得Spring与Tomcat 8和9、WebSphere 9以及JBoss EAP 7等完全兼容。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Over time, the role of Java EE in application development has evolved. In the early days of Java EE and Spring, applications were created to be deployed to an application server. Today, with the help of Spring Boot, applications are created in a devops- and cloud-friendly way, with the Servlet container embedded and trivial to change. As of Spring Framework 5, a WebFlux application does not even use the Servlet API directly and can run on servers (such as Netty) that are not Servlet containers.
#### ** Chinese **

随着时间的推移，Java EE在应用程序开发中的作用也在不断发展。在Java EE和Spring的早期，应用程序的创建是为了部署到应用服务器上。如今，在Spring Boot的帮助下，应用程序以开发和云端友好的方式创建，Servlet容器被嵌入到了Servlet容器中，而且改变起来很简单。从Spring Framework 5开始，WebFlux应用程序甚至不直接使用Servlet API，可以在不是Servlet容器的服务器（如Netty）上运行。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring continues to innovate and to evolve. Beyond the Spring Framework, there are other projects, such as Spring Boot, Spring Security, Spring Data, Spring Cloud, Spring Batch, among others. It’s important to remember that each project has its own source code repository, issue tracker, and release cadence. See [spring.io/projects](https://spring.io/projects) for the complete list of Spring projects.
#### ** Chinese **

Spring不断创新，不断发展。在Spring框架之外，还有其他项目，如Spring Boot、Spring Security、Spring Data、Spring Cloud、Spring Batch等。需要记住的是，每个项目都有自己的源代码库、问题跟踪器和发布节奏。有关Spring项目的完整列表，请参阅[spring.io/projects](https://spring.io/projects)。

<!-- tabs:end -->


## **3. Design Philosophy** 

<!-- tabs:start -->

#### ** English **

When you learn about a framework, it’s important to know not only what it does but what principles it follows. Here are the guiding principles of the Spring Framework:
#### ** Chinese **

当你了解一个框架的时候，不仅要知道它的作用，而且要知道它所遵循的原则。以下是Spring框架的指导原则。

<!-- tabs:end -->


## **4. Feedback and Contributions** 

<!-- tabs:start -->

#### ** English **

For how-to questions or diagnosing or debugging issues, we suggest using StackOverflow, and we have a [questions page](https://spring.io/questions) that lists the suggested tags to use. If you’re fairly certain that there is a problem in the Spring Framework or would like to suggest a feature, please use the [GitHub Issues](https://github.com/spring-projects/spring-framework/issues).
#### ** Chinese **

对于如何解决问题或诊断或调试问题，我们建议使用StackOverflow，我们有一个[问题页面](https://spring.io/questions)，其中列出了建议使用的标签。如果你很确定Spring框架中存在问题，或者想推荐一个功能，请使用[GitHub问题](https://github.com/spring-projects/spring-framework/issues)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you have a solution in mind or a suggested fix, you can submit a pull request on [Github](https://github.com/spring-projects/spring-framework). However, please keep in mind that, for all but the most trivial issues, we expect a ticket to be filed in the issue tracker, where discussions take place and leave a record for future reference.
#### ** Chinese **

如果你有一个解决方案或建议的修复方案，你可以在[Github](https://github.com/spring-projects/spring-framework)上提交一个请求。但是，请记住，除了最琐碎的问题，我们希望在问题跟踪器中提交一个单子，在那里进行讨论，并留下记录，以备日后参考。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For more details see the guidelines at the [CONTRIBUTING](https://github.com/spring-projects/spring-framework/blob/master/CONTRIBUTING.md), top-level project page.
#### ** Chinese **

更多详情请参见[CONTRIBUTING](https://github.com/spring-projects/spring-framework/blob/master/CONTRIBUTING.md)顶级项目页面的指南。

<!-- tabs:end -->


## **5. Getting Started** 

<!-- tabs:start -->

#### ** English **

If you are just getting started with Spring, you may want to begin using the Spring Framework by creating a [Spring Boot](https://projects.spring.io/spring-boot/)-based application. Spring Boot provides a quick (and opinionated) way to create a production-ready Spring-based application. It is based on the Spring Framework, favors convention over configuration, and is designed to get you up and running as quickly as possible.
#### ** Chinese **

如果您刚刚开始使用Spring，您可能希望通过创建一个基于[Spring Boot](https://projects.spring.io/spring-boot/)的应用程序来开始使用Spring框架。Spring Boot提供了一种快速（也是有观点的）方法来创建一个基于Spring的生产型应用程序。它基于Spring框架，偏向于常规而非配置，旨在让你尽快启动和运行。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You can use [start.spring.io](https://start.spring.io/) to generate a basic project or follow one of the ["Getting Started" guides](https://spring.io/guides), such as [Getting Started Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/). As well as being easier to digest, these guides are very task focused, and most of them are based on Spring Boot. They also cover other projects from the Spring portfolio that you might want to consider when solving a particular problem.
#### ** Chinese **

你可以使用[start.spring.io](https://start.spring.io/)来生成一个基本的项目，或者按照["入门 "指南](https://spring.io/guides)中的一个指南，比如[Getting Started Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)。这些指南除了比较容易消化之外，还非常注重任务，而且大部分指南都是基于Spring Boot。它们还涵盖了Spring组合中的其他项目，在解决某个特定问题时，你可能会考虑到这些项目。

<!-- tabs:end -->



[下一章](Spring-Framework-5.2.6.RELEASE/Core%20Technologies/概述.md)


[回目录](Spring-Framework-5.2.6.RELEASE/summary.md)

[回首页](/README)
