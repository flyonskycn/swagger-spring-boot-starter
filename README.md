# swagger-spring-boot-starter

## 使用步骤：
1.引入依赖
    ```
    <dependency>
	    <groupId>org.flyonsky.boot</groupId>
	    <artifactId>swagger-spring-boot-starter</artifactId>
	    <version>2.0.7.RELEASE</version>
	</dependency>
	```
2.配置
swagger.basePackage:需要生成swagger文档的基础包
swagger.groupName:swagger分组名称，一般设置为spring.application.name
swagger.version:版本号,默认为2.0
3.在需要的标记的方法增加swagger注解