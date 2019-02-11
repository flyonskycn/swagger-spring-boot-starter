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
1. swagger.basePackage: 需要生成swagger文档的基础包
2. swagger.groupName: swagger分组名称，一般设置为spring.application.name
3. swagger.version: 版本号,默认为2.0
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
```java
@Api(tags= {"时间管理"})
@RestController
public class TimeController {
	
	@GetMapping("currentime")
	@ApiOperation("时间函数")
	public String currentime() {
		SimpleDateFormat sf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
		return sf.format(Calendar.getInstance().getTime());
	}
}
```
### 注意点
**通过spring mvc注解的controller,必须要设置名称，不能使用默认名称,如:@GetMapping("currentime"),否则swagger不能正确生成文档**

## 样例
[样例参见](https://github.com/flyonskycn/micro-service-study/tree/master/swaggerdemo)