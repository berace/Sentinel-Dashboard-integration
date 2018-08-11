# Sentinel-Dashboard-integration
dubbo项目接入阿里Sentinel
1. 引入相关包
    <!-- 限流衛兵 -->
		<dependency>
			<groupId>com.alibaba.csp</groupId>
			<artifactId>sentinel-dubbo-adapter</artifactId>
			<version>0.1.1</version>
		</dependency>
 2. 接入控制台
  <!-- 卫兵控制台接入 -->
		<dependency>
		    <groupId>com.alibaba.csp</groupId>
		    <artifactId>sentinel-transport-simple-http</artifactId>
		    <version>0.1.1</version>
		</dependency>
  3. 启动provider
  参数启动，vm args
  -Dcsp.sentinel.api.port=8720 -Dcsp.sentinel.dashboard.server=localhost:8080 -Dproject.name=dubbo-provider-demo
  4. 启动consumer
  参数启动，vm args
  -Dcsp.sentinel.api.port=8721 -Dcsp.sentinel.dashboard.server=localhost:8080 -Dproject.name=dubbo-consumer-demo
  
  注意：localhost:8080 是卫兵控制台的地址
  
  5. 启动控制台
  
  详见：
  https://github.com/alibaba/Sentinel/blob/master/sentinel-demo/sentinel-demo-dubbo/README.md#sentinel-dashboard
  
