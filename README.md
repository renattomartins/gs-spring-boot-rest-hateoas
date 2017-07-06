# gs-spring-boot-rest-hateoas
This is a simple repository for future reference about how to build a Hypermedia-Driven RESTful Web Service with Spring Boot.

It was based in [Building a Hypermedia-Driven RESTful Web Service](https://spring.io/guides/gs/rest-hateoas/) tutorial.

### Instructions to run the application
1. Clone this repository
2. So, you must choose one of the two alternatives bellow to build and run the application:
    1. Alternative 1: Run the command `./gradlew bootRun` on root folder
    2. Alternative 2: Or you can build the JAR file using `./gradlew build` and then running the JAR file<br /> `java -jar build/libs/gs-spring-boot-rest-hateoas-0.1.0.jar`
3. After this, the service is up. If you visit http://localhost:8080/greeting you can see:
```javascript
 {"id": 1, "content": "Hello, World!"}
```

### About development environment

- Java 1.8.0_25
- Spring Boot 1.5.4
- Gradle 4.0
- Groovy 2.4.11
- Gradle Wrapper 3.5.1
- Ant 1.9.6
- Mac OS 10.12.5 x86_64
- Eclipse IDE Neon 4.6.3
- Atom 1.18.0 x64
- Git 2.8.1
- Tower 2.4.0 for OSx

## Some concepts

**Spring HATEOAS** - Create REST representations that follow the HATEOAS principle from your Spring-based applications. 

Curiosity: Spring HATEOAS respects various *X-FORWARDED-* headers. If you put a Spring HATEOAS service behind a proxy and properly configure it with *X-FORWARDED-HOST* headers, the resulting links will be properly formatted.

**HAL format** - HAL (Hypertext Application Language) is a simple format that gives a consistent and easy way to hyperlink between resources in your API.

## Some other details

### Used annotation
- @JsonCreator
- @JsonProperty("content")
- @RestController
- @RequestMapping("/greeting")
- @RequestParam(value = "name", required = false, defaultValue = "World")
- @SpringBootApplication

#### Related annotation
- @Configuration
- @EnableAutoConfiguration
- @EnableWebMvc
- @ComponentScan

#### Annotations used on test cases
- @RunWith(SpringRunner.class)
- @RunWith(SpringJUnit4ClassRunner.class)
- @SpringBootTest
- @SpringBootTest(webEnvironment = WebEnvironment.RANDOM_PORT)
- @LocalServerPort
- @AutoConfigureMockMvc
- @Autowired
- @Test
