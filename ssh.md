## SSH（Struts+Hibernate+Spring）：

SSH 通常指的是 Struts2 做控制器\(controller\)，spring 管理各层的组件，hibernate 负责持久化层。

### struts:

#### Struts框架是什么？

由于我们开发Web应用的复杂度随着系统的复杂度的要求越来越来复杂。特别是在代码重用，代码移植、代马可插扒等问题上出现了许多重复开发、维护困难等。从而提出了Struts开发框架。

它的设计目的是从整体上减轻构造企业Web应用的负担，并提供国际化和数据库连接池支持。

Struts 是一组相互协作的类、servlet 和 JSP 标记，它们组成一个可重用的 MVC 2 设计。这个定义表示 Struts 是一个框架，而不是一个库，但 Struts 也包含了丰富的标记库和独立于该框架工作的实用程序类。

Struts的目标是提供一个开发Web应用的开源框架。Struts鼓励基于M2模式（即MVC设计模式）来开发程序。

框架最简单的形式是指已开发过并已测试过的软件的程序块，这些程序块可以在多个软件开发工程中重用。框架提供了一个概括的体系结构模版，可以用这个模板来构建特定领域中的应用程序。

Framework概念并不是很新了，伴随着软件开发的发展，在多层的软件开发项目中，可重用、易扩展的，而且是经过良好测试的软件组件，越来越为人们所青睐。这意味着人们可以将充裕的时间用来分析、构建业务逻辑的应用上，而非繁杂的代码工程。

于是人们将相同类型问题的解决途径进行抽象，抽取成一个应用框架。这也就是我们所说的Framework。Framework的体系提供了一套明确机制，从而让开发人员很容易的扩展和控制整个framework开发上的结构。

#### Struts框架概览：

#### ![](/assets/impor.png)

Struts过程：

1.ActionServlet类控制导航流

2.ActionServlet根据URI来决定哪个Action类被用于处理请求,Action可以校验输入,并访问业务层以便从数据库检索信息

3.Action需要知道页面提交了哪些内容,所以由ActionServlet根据请求URI来决定将请求  
参数绑定到哪个ActionForm中,并传入Action。Action在完成业务逻辑后,返回一个ActionForward对象,ActionServlet根据ActionForward对象中的路径来调用页面完成响应

4.Struts将这些信息绑定在一个ActionMapping对象中,一个ActionMapping对应一个请求URI,当请求路径到达的时候,ActionServlet就会查询ActionMapping对象，ActionMapping对象将告诉ActionServlet哪个Action类会被调用、哪个ActionForm类被用于传递页面数据以及哪些ActionForward将被用于转向。

5.有关Action、ActionForm、ActionForward等信息，Struts通过一个配置文件struts-config.xml文件来定义。

#### Struts优点和缺点：

Struts框架详解 - 程序员中的华仔 - 博客园

var currentBlogId=257868;var currentBlogApp='jun9207',cb\_enable\_mathjax=false;var isLogined=false;

**采用Struts的优点**

在实际开发中，MVC框架开发相当费时，Struts 实现了MVC这种框架，但又扩充了该MVC框架。这样使得系统的开发就像“填空”一样进行，相当快速。

采用Strust可以加快开发速度、增强系统的灵活性、降低系统的藕合性

因为它的三个应用层松散地耦合在一起和易于系统的维护。

分工明确：业务层与表示层分开，使得管理人员可以在小组内分配责任。网页设计人员与JAVA程序员各司其职。

简化页面：使用标记，把逻辑处理的代码分离开来。

通过将问题划分为更小的组件，当技术空间或问题空间中出现变化时，您就有更多的机会重用代码。

**Struts的缺点**

有限的适用范围：Struts 是一种基于 Web 的 MVC 解决方案，所以必须用 HTML、JSP 文件和 Servlet 来实现它。

J2EE 应用程序支持

复杂性：在将问题分为几个部分的同时也引入了复杂性（在强健性增强的同时，也意味着复杂性的增加）。

#### Spring简介:

Spring是是开源框架，是轻量级的IoC和AOP的容器框架，主要是针对javaBean的生命周期进行管理的轻量级容器，可以单独使用，也可以和Struts框架，ibatis框架等组合使用。

#### Spring特性：

利用Spring来创建对象（JavaBean工厂）  
，用Spring构建业务逻辑层  
管理依赖关系  
适应需求变更  
，利用Spring创建数据访问对象（DAO），  
利用Spring进行事务处理  
![](/assets/2017091114512318.jpg)

### 

### Hibernate：

Hibernate 是一个高性能的对象关系型持久化存储和查询的服务，其遵循开源的 GNU Lesser General Public License \(LGPL\) 而且可以免费下载。这个教程将指导你如何以简单的方式使用 Hibernate 来开发基于数据库的 Web 应用程序。

Hibernate 将 Java 类映射到数据库表中，从 Java 数据类型中映射到 SQL 数据类型中，并把开发人员从 95% 的公共数据持续性编程工作中解放出来。

Hibernate 是传统 Java 对象和数据库服务器之间的桥梁，用来处理基于 O/R 映射机制和模式的那些对象。

![](https://7n.w3cschool.cn/attachments/image/wk/hibernate/hibernate_position.jpg "image")

