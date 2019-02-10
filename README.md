# swagger-spring-boot-starter

## 项目依赖
swagger-spring-boot-starter依赖于[autoconfigure项目](https://github.com/flyonskycn/autoconfigure)

## 使用步骤：
### 引入依赖
```xml
<dependency>
    <groupId>org.flyonsky.boot</groupId>
    <artifactId>swagger-spring-boot-starter</artifactId>
    <version>2.0.7.RELEASE</version>
</dependency>
```
### 基本配置
#### swagger.basePackage: 需要生成swagger文档的基础包
#### swagger.groupName: swagger分组名称，一般设置为spring.application.name
#### swagger.version: 版本号,默认为2.0
### 开启swagger注解
```java
@SpringCloudApplication
@EnableSwagger2
public class Application {

	public static void main(String[] args) {
		new SpringApplicationBuilder(Application.class).run(args);
	}
}
```
### 在需要的标记的方法增加swagger注解