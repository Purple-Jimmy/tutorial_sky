# 注册中心_consul
特性:服务发现  健康检查  k/v存储  多数据中心

## 安装(windows)
1. 下载地址https://www.hashicorp.com/products/consul
2. 解压,例D:\consul_1.7.2_windows_amd64
3. 添加环境变量 Path
4. cmd窗口命令执行:consul agent -dev,访问http://localhost:8500
5. cmd窗口命令执行:consul.exe agent -server ui -bootstrap -client 0.0.0.0 -data-dir="E:\consul" -bind X.X.X.X(其中X.X.X.X为服务器ip,即可使用http://X.X.X.X:8500)



## 安装(docker)




## 集成consul
1. 添加依赖
```
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-consul-discovery</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```
2. 在启动类上添加注解@EnableDiscoveryClient,是consul能够发现服务
