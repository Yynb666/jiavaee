1. Spring框架的作用
轻量：Spring是轻量级的，基本的版本大小为2MB
控制反转：Spring通过控制反转实现了松散耦合，对象们给出它们的依赖，而不是创建或查找依赖的对象们。
面向切面的编程AOP:Spring支持面向切面的编程，并且把应用业务逻辑和系统服务分开。
容器：Spring包含并管理应用中对象的生命周期和配置
MVC框架： Spring-MVC
事务管理：Spring提供一个持续的事务管理接口，可以扩展到上至本地事务下至全局事务JTA
异常处理：Spring提供方便的API把具体技术相关的异常
Sping的容器可以分为两种类型
BeanFactory：（org.springframework.beans.factory.BeanFactory接口定义）是最简答的容器，提供了基本的DI支持。最常用的BeanFactory实现就是XmlBeanFactory类，它根据XML文件中的定义加载beans，该容器从XML文件读取配置元数据并用它去创建一个完全配置的系统或应用。
ApplicationContext应用上下文：（org.springframework.context.ApplicationContext）基于BeanFactory之上构建，并提供面向应用的服务。
springMVC全称是spring web mvc，是Spring框架的一部分,是一个MVC模式的WEB开发框架，使用了MVC架构模式的思想，将web层进行职责解耦。
SpringMVC是基于Spring功能之上添加的Web框架，想用SpringMVC必须先依赖Spring，springmvc仅给spring的表现层提供支持。
MVC（Model-View-Controller，模型－视图－控制器）指把页面、后台的交付分成3层来组成，是一种解决页面代码和后台代码分离的设计思想！

MVC里面的M指的是Model（通常包含bean、dao(mapper)、service）；V指的是View，视图层，视图层主要的技术（JSP、HTML）；C指的是Controller，控制层。控制层不负责具体数据、逻辑的处理和运算，它只负责将Model层的结果返回给对应的视图层去展示。

在JavaWeb阶段， Controller层指的就是Servlet； View层指的就是JSP或者HTML; Model层指的就是bean、dao、service。

在J2EE阶段，Controller层指的就是SpringMVC、Structs1\2； View层不变还是主流的页面展示技术; Model层包括bean、mybatis、service。
1、 概念：Java当中的一个持久层框架。
2、 特点、优势：
（1）把java代码和SQL代码做了一个完全分离。
（2）良好支持复杂对象的映射（输入映射、输出映射）
（3）使用动态SQL，可以预防SQL注入。
3、 原理：
（1）创建mybatis-config.xml配置文件
（2）创建sqlSessionFactory
（3）编写数据库表对应的实体类
（4）创建mybatis的sql映射文件，在这个文件中，把实体类的属性和数据库表的列联系起来，并且可以编写sql语句
（5）从sqlSessionFactory的实例获取session
（6）session内部通过Executor执行器执行操作。Executor会用到mapped statement对象，这个对象是对数据库存储的封装，包括：sql语句、输入参数、输出结果类型
（7）关闭session
