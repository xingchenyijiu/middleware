## javaEE的发展

Oracle 的 Java EE布道师 David Delabassee透露，Oracle之所以要开源 Java EE，主要是想让它变得更敏捷，以适应快速发展的行业和技术需求。

事实上，尽管 JCP（Java Community Process）也在这方面做出了一些努力，但仍然无法赶上现代 IT市场快速发展的步伐。从 2013年 6月发布 Java EE 7以来，出现了很多新兴技术，比如 NoSQL、容器、微服务和无服务器架构，但它们都未能被包含在 Java EE当中。

在我看来，这一决定显得有点唐突，因为它与 Oracle 在 JavaOne 2016上发布的路线图完全背道而驰。当然，这一决定也表明了 Java EE 不再是 Oracle的首要关注点。Oracle似乎把更多的注意力放在新的开源项目 Fn上，Fn是一个无服务器框架，类似亚马逊的 Lambda和 IBM的 OpenWhisk（现在是 Apache项目）。

2017 年 9月 21日，Java EE正式发布。 Java EE 8的主要变更具体如下：

与 Java SE 8 同步：DateTime API、CompetableFuture和可重复注解。

CDI 2.0：异步事件、事件保序以及与其他规范更好的集成。

Servlet 4.0：支持 HTTP/2（服务器端推送）。

JAX-RS 2.1：服务器端发送事件、反应式扩展。

JSON Processing 1.1 和 JSON Binding 1.0。

安全：简单化、秘钥管理、现代化、OAuth2 和 OpenID支持。

总的来说，Java EE 8 更像是大跃进，而不是小步快跑。不过，云原生相关应用并没有包含在 Java EE 8中，如分布式跟踪、集中式配置、健康监测、回路断路器、负载均衡。

 Java EE 的现状是怎样的？

对于大多数企业来说，Java EE 仍然是一个非常有价值的平台：完善而灵活的编程模型。单一的依赖管理：通常一个 Maven 的 pom.xml不会包含超过 20行配置代码，即使项目很复杂。CDI 易用且强大。可以与大多数 IDE 集成。

有很多轻量级的应用服务器，比如 TomEE、Payara、Red Hat Wildfly和 IBM Liberty，它们不仅启动速度快，而且占用资源小。

可以使用 Java EE 来开发容器化的微服务，虽然不完美，但也不失为一种选择。Java EE 的不足在于：不够先进：尽管它还有一定的价值，但大部分开发者并不会将它作为开发云原生应用的首选。因为组件模型的差异，缺乏整体的一致性：Servlet、CDI、EJB……确切点说，CDI和 EJB之间的界限有点模糊，或许 CDI在未来会成为“第一类公民”。测试相对复杂。

