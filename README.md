# mini-service-discovery

一个小型服务注册中心。服务节点登记自己的地址，客户端按服务名（和版本）拿到节点列表，并用心跳看节点还在不在。

写于 2020 年，用来把注册、发现、心跳这三步接成一条线。

## 里面有什么

- `RegistryCenter`：`serverSignIn` / `serverSignOut`，以及按 `serviceId`、版本取 `ServiceDefinition`
- `IServiceDiscover`：注册中心对外的 RMI 接口
- `AppServer` / `AppClient`：服务提供方和调用方
- `ServersHeartCheck`：客户端侧的心跳检查

源码在 `mini-service-discovery/src`，包名 `com.mec.service_discover`。目录是当时的 Eclipse 工程。它依赖同系列的 `MyRmi.jar`（[mini-rmi](https://github.com/ailan-aoi/mini-rmi)）和 `Mycs.jar`（[mini-cs-framework](https://github.com/ailan-aoi/mini-cs-framework)）。

## 状态

学习代码，Java 包名和实现按最初上传的样子保留。仓库曾用名 `easyServiceFind`，旧地址会重定向到这里。
