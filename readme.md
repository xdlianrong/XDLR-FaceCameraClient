# 抓拍机客户端
这是社会治理文明赋能演示项目的抓拍机客户端模块，用来链接若干个抓拍机，在抓拍机之间同步数据，并根据抓拍机识别到的行为，与区块链网络做相应的交互。

### 场景说明

客户端程序采集用户文明行为，将文明行为记录上链，形成积分。当用户需要消费的时候，通过客户端识别消费行为，客户端与区块链网络交互，用户有足够多的积分记录，客户端就会控制售货机出货。

### 构建部署

使用[Gradle](https://guides.gradle.org/building-java-applications/#execute_the_build)构建project

```
// 构建
gradlew build

// 运行
gradlew run
```


### 配置
1. 抓拍机和客户端连至同一个路由器
2. 检查抓拍机状态，浏览器方式访问抓拍机，用户名admin
3. 保证售货机正常配货
4. 运行客户端

### 待做事项

1. 添加底图部分代码稳定性有待提高，有时候会出现底图添加不成功的问题
2. 关于底图质量，针对熟人，如果后续抓拍到的人脸图像质量比抓拍机底库中图片质量高（level字段）
   可尝试更新人脸底库图片
3. 完善日志文件系统，记录客户端的运行情况。
4. 客户端与抓拍机关闭连接时需要先注销，节省抓拍机连接资源。