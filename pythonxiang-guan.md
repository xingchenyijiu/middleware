# Python相关

中间件是一个Python程序员用来处理Django的请求和响应的框架级别的钩子，它是一个轻量，低级别的插件系统，用于全局范围内改变Django的输入，输出。每个中间件组件都负责做一些特定的功能。

说的直白一点是中间件就是帮我们程序员在视图函数执行之前和执行之后都可以一些额外的操作，它是一个自定义的类，类中定义了几个方法，Django框架会在请求的特定时间去执行这些方法。

在Python项目中一直都在有使用中间件，在django项目中的setting.py文件中看到MIDDLEWARE配置项。

**自定义中间件的规则**

1.要继承MIDDLEWAREMIXIN类，

2.要重写父类方法

3.将类添加到setting.py文件中MIDDLEWARE配置项里  
父类的五个方法（主要process\_request   process\_response\)process\_request\(self，request\)process\_view\(self,request,view\_func,view\_args,view\_kwargs\)process\_template\_response\(self,request,response\)process\_exception\(self,request,exception\)process\_response\(self,request,response\)返回值可以是一个NONE，或者HttpResponse对象，如果是none，继续按照django定义的向下执行，如果返回是Httpresponse对象，则直接将该对象返回给用户。



**中间件的使用场景**

1.做IP限制

放在中间件类的列表中，阻止某些ip访问；

2.URL访问过滤

如果用户访问的是logo视图（放过）

如果访问其他视图，需要检测是否已经有session，已经有了放行，如果没有返回login，这样就省的在多个视图函数上写装饰器了！

3.缓存

客户端请求来了，中间件去缓存看看有没有数据，有直接返回给用户，没有再去逻辑层执行视图函数。



