# Spring Cloud



### 服务之间通讯解决方案

#### 同步

* RestFul
* RPC

#### 异步消息调用

##### 消息队列方式

* Kafka

  



### 服务注册与发现中心

* Eureka
* Consul
* Zookeeper



### 服务挂了如何解决

* 重试机制

  重新发送请求

* 限流

  客户端随机数，活动已结束

* 熔断机制

  超过流量限制

* 负载均衡

  

* 降级(本地缓存)

  功能直接下线





### 分布式锁应该具备的条件

* 分布式环境下，一个方法同一时间只能被一台机器上的一个线程执行
* 高可用的获取锁，释放锁
* 高性能的获取锁，释放锁
* 具备可重入性(一个任务并发使用而不担心数据错误)
* 具备锁失效机制，防止死锁
* 具备非阻塞锁特性，即没有获取到锁将直接返回获取锁失败



# 有道无术，术尚可求。有术无道，止于术。

技术不是问题，思想才是王道

* 应用程序的核心是业务，按照业务或客户需求组织资源
* 做有生命的产品，而不是项目
* 全栈化
* 后台服务贯彻 Single Responsibility Princple(单一职责原则)
* VM -> Docker
* DevOps



# 微服务架构服务治理组件

## 服务注册中心

* Eureka Server



## 服务提供者

* Eureka Client



## 服务消费者

* Ribbon + RestTemplate

* Feign

  > Feign 默认集成了 Ribbon，并和 Eureka 结合，默认实现了负载均衡效果



## 熔断器

* Hystrix



## 智能路由

* Zuul



## 配置管理

* Config



## 服务追踪组件

* ZipKin

  > 直接使用 Docker 比较方便
  >
  > [openzipkin dockerhub](https://hub.docker.com/u/openzipkin)
  >
  > [docker-zipkin github](https://github.com/openzipkin/docker-zipkin)
  >
  > ```bash
  > docker run -d -p 9411:9411 openzipkin/zipkin
  > docker stop <16>
  > docker rm <16>
  > ```





