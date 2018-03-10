## Spring Cloud

---

几大模块：服务发现（Eureka），断路器（Hystrix），智能路由（Zuul），客户端负载均衡（Ribbon）

spring --> spring boot --> spring cloud

### 一、手册

* [源码](https://github.com/spring-cloud/spring-cloud-netflix)
* [中文社区](http://bbs.springcloud.com.cn/)
* [源码分析](http://www.jianshu.com/u/6a622d516e32)
* [推荐博客](http://www.ityouknow.com/springcloud/2016/12/30/springcloud-collect.html)
* [Spring Cloud 构建微服务示例](https://github.com/aalansehaiyang/spring-cloud-example)
* [spring Cloud 核心组件](https://github.com/ityouknow/spring-cloud-examples)

	* [注册中心 Eureka](http://www.ityouknow.com/springcloud/2017/05/10/springcloud-eureka.html)
		* 生产中我们可能需要三台或者大于三台的注册中心来保证服务的稳定性，配置的原理其实都一样，将注册中心分别指向其它的注册中心
	* [服务注册与发现](http://blog.didispace.com/springcloud6/)
	* [熔断器 Hystrix](http://www.ityouknow.com/springcloud/2017/05/16/springcloud-hystrix.html)
	* [服务网关 Zuul](https://mp.weixin.qq.com/s/5PQ9iyPfYCEcJ5W7q0T2oQ)
		* 通过一个API网关根据请求的url，路由到相应的服务
		* [服务网关zuul初级篇](http://www.ityouknow.com/springcloud/2017/06/01/gateway-service-zuul.html)
	* [客户端负载均衡 Ribbon](http://blog.didispace.com/spring-cloud-starter-dalston-2-2/)
		* 通过在客户端中配置ribbonServerList来设置服务端列表去轮询访问以达到均衡负载的作用。
	* [客户端负载均衡 Feign](http://blog.didispace.com/spring-cloud-starter-dalston-2-3/)	
		* Feign是基于Ribbon实现的，所以它自带了客户端负载均衡功能，也可以通过Ribbon的IRule进行策略扩展。
		* 创建接口并用注解来配置它即可完成对Web服务接口的绑定。它具备可插拔的注解支持，包括Feign注解、JAX-RS注解。它也支持可插拔的编码器和解码器。Spring Cloud Feign还扩展了对Spring MVC注解的支持，同时还整合了Ribbon和Eureka来提供均衡负载的HTTP客户端实现。
	* config
		* 配置中心	
* [SpringCloud-Learning](https://github.com/dyc87112/SpringCloud-Learning)
* [SpringCloud.cc](https://springcloud.cc/spring-cloud-dalston.html)	

### 二、闲谈

* [Spring Cloud在国内中小型公司能用起来吗？](https://mp.weixin.qq.com/s/vnWXpH5pv-FAzLZfbgTGvg)

#### 三、坑

* [注册中心备份节点 unavailable-replicas问题](http://www.ccblog.cn/95.htm)