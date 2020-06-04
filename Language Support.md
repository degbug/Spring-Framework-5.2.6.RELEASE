# Language Support

## **1. Kotlin** 

<!-- tabs:start -->

#### ** English **

[Kotlin](https://kotlinlang.org/) is a statically typed language that targets the JVM (and other platforms) which allows writing concise and elegant code while providing very good [interoperability](https://kotlinlang.org/docs/reference/java-interop.html) with existing libraries written in Java.
#### ** Chinese **

Kotlin](https://kotlinlang.org/)是一种静态类型化语言，它以JVM(和其他平台)为目标，允许编写简洁而优雅的代码，同时提供了与现有的Java库的良好[互操作性](https://kotlinlang.org/docs/reference/java-interop.html)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The Spring Framework provides first-class support for Kotlin and lets developers write Kotlin applications almost as if the Spring Framework was a native Kotlin framework.
#### ** Chinese **

Spring框架为Kotlin提供了一流的支持，让开发者在编写Kotlin应用程序时几乎可以像Spring框架是一个原生的Kotlin框架一样。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The easiest way to build a Spring application with Kotlin is to leverage Spring Boot and its [dedicated Kotlin support](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-kotlin.html). [This comprehensive tutorial](https://spring.io/guides/tutorials/spring-boot-kotlin/) will teach you how to build Spring Boot applications with Kotlin using [start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project).
#### ** Chinese **

使用Kotlin构建Spring应用程序最简单的方法是利用Spring Boot和它的[专门的Kotlin支持](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-kotlin.html)。 本篇综合教程](https://spring.io/guides/tutorials/spring-boot-kotlin/)将教你如何使用[start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project)使用Kotlin构建Spring Boot应用程序。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

As of Spring Framework 5.2, most of the code samples of the reference documentation are provided in Kotlin in addition to Java.
#### ** Chinese **

从Spring Framework 5.2开始，除了Java之外，大部分参考文档的代码示例都是用Kotlin提供的。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Feel free to join the #spring channel of [Kotlin Slack](https://slack.kotlinlang.org/) or ask a question with `spring` and `kotlin` as tags on [Stackoverflow](https://stackoverflow.com/questions/tagged/spring+kotlin) if you need support.
#### ** Chinese **

如果您需要支持，请随时加入 [Kotlin Slack](https://slack.kotlinlang.org/)的 #spring 频道，或者在 [Stackoverflow](https://stackoverflow.com/questions/tagged/spring+kotlin)(https://stackoverflow.com/questions/tagged/spring+kotlin)上以 `spring` 和 `kotlin` 作为标签提出问题。

<!-- tabs:end -->


### **1.1. Requirements** 

<!-- tabs:start -->

#### ** English **

Spring Framework supports Kotlin 1.3 and requires [`kotlin-stdlib`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-stdlib) (or one of its variants, such as [`kotlin-stdlib-jdk8`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-stdlib-jdk8)) and [`kotlin-reflect`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-reflect) to be present on the classpath. They are provided by default if you bootstrap a Kotlin project on [start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project).
#### ** Chinese **

Spring Framework 支持 Kotlin 1.3，并且需要在 classpath 中存在 [`kotlin-stdlib`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-stdlib)（或其变体之一，如 [`kotlin-stdlib-jdk8`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-stdlib-jdk8)）和 [`kotlin-reflect`](https://bintray.com/bintray/jcenter/org.jetbrains.kotlin%3Akotlin-reflect)。如果你在[start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project)上引导一个Kotlin项目，那么它们是默认提供的。

<!-- tabs:end -->


### **1.2. Extensions** 

<!-- tabs:start -->

#### ** English **

Kotlin [extensions](https://kotlinlang.org/docs/reference/extensions.html) provide the ability to extend existing classes with additional functionality. The Spring Framework Kotlin APIs use these extensions to add new Kotlin-specific conveniences to existing Spring APIs.
#### ** Chinese **

Kotlin [extensions](https://kotlinlang.org/docs/reference/extensions.html)提供了扩展现有类的功能。Spring Framework Kotlin APIs使用这些扩展来为现有的Spring APIs添加新的Kotlin特有的便利。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The [Spring Framework KDoc API](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/) lists and documents all available the Kotlin extensions and DSLs.
#### ** Chinese **

Spring Framework KDoc API](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/)列出并记录了所有可用的 Kotlin 扩展和 DSL。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Keep in mind that Kotlin extensions need to be imported to be used. This means, for example, that the `GenericApplicationContext.registerBean` Kotlin extension is available only if `org.springframework.context.support.registerBean` is imported. That said, similar to static imports, an IDE should automatically suggest the import in most cases.
#### ** Chinese **

请记住，Kotlin扩展需要被导入才能使用。这意味着，例如，只有在导入了`org.springframework.context.support.registerBean`的情况下，才可以使用`GenericApplicationContext.registerBean` Kotlin扩展。也就是说，与静态导入类似，在大多数情况下，IDE应该会自动建议导入。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For example, [Kotlin reified type parameters](https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters) provide a workaround for JVM [generics type erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html), and the Spring Framework provides some extensions to take advantage of this feature. This allows for a better Kotlin API `RestTemplate`, for the new `WebClient` from Spring WebFlux, and for various other APIs.
#### ** Chinese **

例如，[Kotlin reified type parameters](https://kotlinlang.org/docs/reference/inline-functions.html#reified-type-parameters)为JVM[generics type erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html)提供了一种工作方法，而Spring框架提供了一些扩展来利用这一特性。这使得Kotlin API `RestTemplate`、Spring WebFlux的新`WebClient`以及其他各种API都能得到更好的应用。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Other libraries, such as Reactor and Spring Data, also provide Kotlin extensions for their APIs, thus giving a better Kotlin development experience overall.
#### ** Chinese **

其他库，如Reactor和Spring Data等，也为其API提供了Kotlin扩展，从而使Kotlin的开发体验整体上有了更好的体验。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To retrieve a list of `User` objects in Java, you would normally write the following:
#### ** Chinese **

要在Java中检索一个`用户`对象的列表，通常情况下，你会写以下内容。

<!-- tabs:end -->


```
Flux<User> users  = client.get().retrieve().bodyToFlux(User.class)
```

<!-- tabs:start -->

#### ** English **

With Kotlin and the Spring Framework extensions, you can instead write the following:
#### ** Chinese **

通过Kotlin和Spring框架的扩展，你可以写以下内容。

<!-- tabs:end -->


```
val users = client.get().retrieve().bodyToFlux<User>()
// or (both are equivalent)
val users : Flux<User> = client.get().retrieve().bodyToFlux()
```

<!-- tabs:start -->

#### ** English **

As in Java, `users` in Kotlin is strongly typed, but Kotlin’s clever type inference allows for shorter syntax.
#### ** Chinese **

和Java中一样，Kotlin中的`users`也是强类型化的，但Kotlin巧妙的类型推理允许更短的语法。

<!-- tabs:end -->


### **1.3. Null-safety** 

<!-- tabs:start -->

#### ** English **

One of Kotlin’s key features is [null-safety](https://kotlinlang.org/docs/reference/null-safety.html), which cleanly deals with `null` values at compile time rather than bumping into the famous `NullPointerException` at runtime. This makes applications safer through nullability declarations and expressing “value or no value” semantics without paying the cost of wrappers, such as `Optional`. (Kotlin allows using functional constructs with nullable values. See this [comprehensive guide to Kotlin null-safety](https://www.baeldung.com/kotlin-null-safety).)
#### ** Chinese **

Kotlin的关键特性之一是[null-safety](https://kotlinlang.org/docs/reference/null-safety.html)，它可以在编译时干净利落地处理`null`值，而不是在运行时碰到著名的`NullPointerException`。这使得应用程序通过nullability声明和表达 "值或无值 "语义而不需要支付包装器的成本，例如`Optional`，从而使应用程序更加安全。(Kotlin允许使用具有nullable值的函数构造。参见这个[Kotlin null-safety综合指南](https://www.baeldung.com/kotlin-null-safety)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Although Java does not let you express null-safety in its type-system, the Spring Framework provides [null-safety of the whole Spring Framework API](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#null-safety) via tooling-friendly annotations declared in the `org.springframework.lang` package. By default, types from Java APIs used in Kotlin are recognized as [platform types](https://kotlinlang.org/docs/reference/java-interop.html#null-safety-and-platform-types), for which null-checks are relaxed. [Kotlin support for JSR-305 annotations](https://kotlinlang.org/docs/reference/java-interop.html#jsr-305-support) and Spring nullability annotations provide null-safety for the whole Spring Framework API to Kotlin developers, with the advantage of dealing with `null`-related issues at compile time.
#### ** Chinese **

虽然Java不允许在其类型系统中表达null-safety，但Spring框架通过在`org.springframework.lang`包中声明的工具友好型注释提供了[整个Spring框架API的null-safety](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#null-safety)。默认情况下，Kotlin中使用的Java API的类型被识别为[平台类型](https://kotlinlang.org/docs/reference/java-interop.html#null-safety-and-platform-types)，对于这些类型，null-checks是放宽的。 Kotlin 支持 JSR-305 注释](https://kotlinlang.org/docs/reference/java-interop.html#jsr-305-support)和 Spring nullability 注释为 Kotlin 开发者提供了整个 Spring Framework API 的 null-safety，其优点是可以在编译时处理 `null`相关的问题。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Libraries such as Reactor or Spring Data provide null-safe APIs to leverage this feature.
#### ** Chinese **

Reactor或Spring Data等库提供了null-safe API来利用这一特性。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You can configure JSR-305 checks by adding the `-Xjsr305` compiler flag with the following options: `-Xjsr305={strict|warn|ignore}`.
#### ** Chinese **

您可以通过添加 `-Xjsr305` 编译器标志来配置 JSR-305 检查。 `-Xjsr305={strict|warn|ignore}`。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For kotlin versions 1.1+, the default behavior is the same as `-Xjsr305=warn`. The `strict` value is required to have Spring Framework API null-safety taken into account in Kotlin types inferred from Spring API but should be used with the knowledge that Spring API nullability declaration could evolve even between minor releases and that more checks may be added in the future.
#### ** Chinese **

对于kotlin 1.1+版本，默认行为与`-Xjsr305=warn`相同。`strict`值是在从Spring API推断出的Kotlin类型中考虑到Spring Framework API的null-safety的必要条件，但在使用时应考虑到Spring API的null-safety声明可能会在不同的小版本之间演变，而且未来可能会增加更多的检查。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Generic type arguments, varargs, and array elements nullability are not supported yet, but should be in an upcoming release. See [this discussion](https://github.com/Kotlin/KEEP/issues/79) for up-to-date information.
#### ** Chinese **

通用类型参数、varargs和数组元素的可空性还不支持，但应该会在即将发布的版本中出现。最新的信息请参见[本讨论](https://github.com/Kotlin/KEEP/issues/79)。

<!-- tabs:end -->


### **1.4. Classes and Interfaces** 

<!-- tabs:start -->

#### ** English **

The Spring Framework supports various Kotlin constructs, such as instantiating Kotlin classes through primary constructors, immutable classes data binding, and function optional parameters with default values.
#### ** Chinese **

Spring框架支持各种Kotlin构造，如通过主构造函数实例化Kotlin类，不可变类数据绑定，以及带默认值的函数可选参数等。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Kotlin parameter names are recognized through a dedicated `KotlinReflectionParameterNameDiscoverer`, which allows finding interface method parameter names without requiring the Java 8 `-parameters` compiler flag to be enabled during compilation.
#### ** Chinese **

Kotlin参数名通过专用的`KotlinReflectionParameterNameDiscoverer`来识别，它允许查找接口方法的参数名，而不需要在编译过程中启用Java 8 `-parameters`编译器标志。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The [Jackson Kotlin module](https://github.com/FasterXML/jackson-module-kotlin), which is required for serializing or deserializing JSON data, is automatically registered when found in the classpath, and a warning message is logged if Jackson and Kotlin are detected without the Jackson Kotlin module being present.
#### ** Chinese **

Jackson Kotlin模块](https://github.com/FasterXML/jackson-module-kotlin)，在classpath中发现JSON数据序列化或反序列化JSON数据时，会自动注册，如果检测到JSON和Kotlin模块不存在，会记录一条警告消息。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You can declare configuration classes as [top level or nested but not inner](https://kotlinlang.org/docs/reference/nested-classes.html), since the later requires a reference to the outer class.
#### ** Chinese **

你可以将配置类声明为[顶层或嵌套但不是内层](https://kotlinlang.org/docs/reference/nested-classes.html)，因为后者需要引用外层类。

<!-- tabs:end -->


### **1.5. Annotations** 

<!-- tabs:start -->

#### ** English **

The Spring Framework also takes advantage of [Kotlin null-safety](https://kotlinlang.org/docs/reference/null-safety.html) to determine if an HTTP parameter is required without having to explicitly define the `required` attribute. That means `@RequestParam name: String?` is treated as not required and, conversely, `@RequestParam name: String` is treated as being required. This feature is also supported on the Spring Messaging `@Header` annotation.
#### ** Chinese **

Spring框架还利用了[Kotlin null-safety](https://kotlinlang.org/docs/reference/null-safety.html)来确定HTTP参数是否需要，而不需要显式定义`required`属性。这意味着`@RequestParam name: String?`被视为不需要，反之，`@RequestParam name: String`被视为需要。Spring Messaging `@Header`注释也支持此功能。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

In a similar fashion, Spring bean injection with `@Autowired`, `@Bean`, or `@Inject` uses this information to determine if a bean is required or not.
#### ** Chinese **

以类似的方式，使用`@Autowired`、`@Bean`或`@Inject`的Spring bean注入，使用这些信息来确定是否需要一个bean。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For example, `@Autowired lateinit var thing: Thing` implies that a bean of type `Thing` must be registered in the application context, while `@Autowired lateinit var thing: Thing?` does not raise an error if such a bean does not exist.
#### ** Chinese **

例如，`@Autowired lateinit var thing: Thing`暗示必须在应用程序上下文中注册一个类型为`Thing`的Bean，而`@Autowired lateinit var thing: Thing?`如果这样的Bean不存在，则不会产生错误。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Following the same principle, `@Bean fun play(toy: Toy, car: Car?) = Baz(toy, Car)` implies that a bean of type `Toy` must be registered in the application context, while a bean of type `Car` may or may not exist. The same behavior applies to autowired constructor parameters.
#### ** Chinese **

根据同样的原理，`@Bean fun play(tooy: Toy, car: Car?) = Baz(tooy, Car)`意味着类型为`Toy`的Bean必须在应用程序上下文中注册，而类型为`Car`的Bean可能存在也可能不存在。同样的行为也适用于自动连接的构造函数参数。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you use bean validation on classes with properties or a primary constructor parameters, you may need to use [annotation use-site targets](https://kotlinlang.org/docs/reference/annotations.html#annotation-use-site-targets), such as `@field:NotNull` or `@get:Size(min=5, max=15)`, as described in [this Stack Overflow response](https://stackoverflow.com/a/35853200/1092077).
#### ** Chinese **

如果您在具有属性或主构造函数参数的类上使用Bean验证，可能需要使用[注解使用站点目标](https://kotlinlang.org/docs/reference/annotations.html#annotation-use-site-targets)，如`@field:NotNull`或`@get:Size(min=5, max=15)`，如[this Stack Overflow response](https://stackoverflow.com/a/35853200/1092077)中描述的那样。

<!-- tabs:end -->


### **1.6. Bean Definition DSL** 

<!-- tabs:start -->

#### ** English **

Spring Framework supports registering beans in a functional way by using lambdas as an alternative to XML or Java configuration (`@Configuration` and `@Bean`). In a nutshell, it lets you register beans with a lambda that acts as a `FactoryBean`. This mechanism is very efficient, as it does not require any reflection or CGLIB proxies.
#### ** Chinese **

Spring Framework 支持通过使用 lambdas 作为 XML 或 Java 配置（`@Configuration` 和 `@Bean`）的替代品，以功能化的方式注册 Bean。简而言之，它可以让你用一个作为`FactoryBean`的lambda来注册Bean。这种机制非常有效，因为它不需要任何反射或CGLIB代理。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

In Java, you can, for example, write the following:
#### ** Chinese **

例如，在Java中，你可以写出以下内容。

<!-- tabs:end -->


```java
class Foo {}

class Bar {
    private final Foo foo;
    public Bar(Foo foo) {
        this.foo = foo;
    }
}

GenericApplicationContext context = new GenericApplicationContext();
context.registerBean(Foo.class);
context.registerBean(Bar.class, () -> new Bar(context.getBean(Foo.class)));
```

<!-- tabs:start -->

#### ** English **

In Kotlin, with reified type parameters and `GenericApplicationContext` Kotlin extensions, you can instead write the following:
#### ** Chinese **

在Kotlin中，通过重构类型参数和`GenericApplicationContext` Kotlin扩展，你可以写以下内容。

<!-- tabs:end -->


```java
class Foo

class Bar(private val foo: Foo)

val context = GenericApplicationContext().apply {
    registerBean<Foo>()
    registerBean { Bar(it.getBean()) }
}
```

<!-- tabs:start -->

#### ** English **

When the class `Bar` has a single constructor, you can even just specify the bean class, the constructor parameters will be autowired by type:
#### ** Chinese **

当类`Bar`有一个单独的构造函数时，你甚至可以只需指定Bean类，构造函数参数将按类型自动触发。

<!-- tabs:end -->


```
val context = GenericApplicationContext().apply {
    registerBean<Foo>()
    registerBean<Bar>()
}
```

<!-- tabs:start -->

#### ** English **

In order to allow a more declarative approach and cleaner syntax, Spring Framework provides a [Kotlin bean definition DSL](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.context.support/-bean-definition-dsl/) It declares an `ApplicationContextInitializer` through a clean declarative API, which lets you deal with profiles and `Environment` for customizing how beans are registered.
#### ** Chinese **

为了允许更多的声明性方法和更干净的语法，Spring框架提供了一个[Kotlin bean定义DSL](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.context.support/-bean-definition-dsl/) 它通过一个干净的声明式API声明一个`ApplicationContextInitializer`，让你可以处理profile和`Environment`，用于自定义Bean的注册方式。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

In the following example notice that:
#### ** Chinese **

在下面的例子中，请注意：

<!-- tabs:end -->


```java
class Foo
class Bar(private val foo: Foo)
class Baz(var message: String = "")
class FooBar(private val baz: Baz)

val myBeans = beans {
    bean<Foo>()
    bean<Bar>()
    bean("bazBean") {
        Baz().apply {
            message = "Hello world"
        }
    }
    profile("foobar") {
        bean { FooBar(ref("bazBean")) }
    }
    bean(::myRouter)
}

fun myRouter(foo: Foo, bar: Bar, baz: Baz) = router {
    // ...
}
```
<!-- tabs:start -->

#### ** English **

- Type inference usually allows to avoid specifying the type for bean references like `ref("bazBean")`

- It is possible to use Kotlin top level functions to declare beans using callable references like `bean(::myRouter)` in this example

- When specifying `bean<Bar>()` or `bean(::myRouter)`, parameters are autowired by type

- The `FooBar` bean will be registered only if the `foobar` profile is active


#### ** Chinese **

- 类型推理通常可以避免指定bean引用的类型，如`ref("bazBean")`</x>

- 可以使用Kotlin顶层函数来声明Bean，使用可调用的引用来声明Bean，比如这个例子中的`bean(:::myRouter)`

- 当指定`bean<Bar>()`或`bean(:::myRouter)`时，参数按类型自动布线

- `FooBar` bean只有在`foobar`配置文件处于活动状态时才会被注册。


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

This DSL is programmatic, meaning it allows custom registration logic of beans through an `if` expression, a `for` loop, or any other Kotlin constructs.
#### ** Chinese **

这个 DSL 是程序化的，这意味着它允许通过 `if`表达式、`for`循环或任何其他 Kotlin 构造来定制 Bean 的注册逻辑。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You can then use this `beans()` function to register beans on the application context, as the following example shows:
#### ** Chinese **

然后你可以使用这个`beans()`函数在应用程序上下文中注册bean，如下图所示。

<!-- tabs:end -->


```
val context = GenericApplicationContext().apply {
    myBeans.initialize(this)
    refresh()
}
```

<!-- tabs:start -->

#### ** English **

Spring Boot is based on JavaConfig and [does not yet provide specific support for functional bean definition](https://github.com/spring-projects/spring-boot/issues/8115), but you can experimentally use functional bean definitions through Spring Boot’s `ApplicationContextInitializer` support. See [this Stack Overflow answer](https://stackoverflow.com/questions/45935931/how-to-use-functional-bean-definition-kotlin-dsl-with-spring-boot-and-spring-w/46033685#46033685) for more details and up-to-date information. See also the experimental Kofu DSL developed in [Spring Fu incubator](https://github.com/spring-projects/spring-fu).
#### ** Chinese **

Spring Boot基于JavaConfig，[还没有提供对功能豆定义的具体支持](https://github.com/spring-projects/spring-boot/issues/8115)，但你可以通过Spring Boot的`ApplicationContextInitializer`支持实验性地使用功能豆定义。更多细节和最新信息，请参见[this Stack Overflow答案](https://stackoverflow.com/questions/45935931/how-to-use-functional-bean-definition-kotlin-dsl-with-spring-boot-and-spring-w/46033685#46033685)。也请参见[Spring Fu incubator](https://github.com/spring-projects/spring-fu)中开发的实验性 Kofu DSL。

<!-- tabs:end -->


### **1.7. Web** 

### **1.7.1. Router DSL** 

<!-- tabs:start -->

#### ** English **

Spring Framework comes with a Kotlin router DSL available in 3 flavors:
#### ** Chinese **

Spring Framework自带的Kotlin路由器DSL有3种口味。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- WebMvc.fn DSL with [router { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.servlet.function/router.html)

- WebFlux.fn [Reactive](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web-reactive.html#webflux-fn) DSL with [router { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/router.html)

- WebFlux.fn [Coroutines](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#coroutines) DSL with [coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html)

#### ** Chinese **

- WebMvc.fn DSL与[路由器 { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.servlet.function/router.html)

- WebFlux.fn [Reactive](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web-reactive.html#webflux-fn) DSL with [router { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/router.html)

- WebFlux.fn [Coroutines](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#coroutines) DSL with [coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html)


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

These DSL let you write clean and idiomatic Kotlin code to build a `RouterFunction` instance as the following example shows:
#### ** Chinese **

这些 DSL 可以让你写出干净利落的 Kotlin 代码来构建一个 `RouterFunction`实例，如下图所示。

<!-- tabs:end -->


```java
@Configuration
class RouterRouterConfiguration {

    @Bean
    fun mainRouter(userHandler: UserHandler) = router {
        accept(TEXT_HTML).nest {
            GET("/") { ok().render("index") }
            GET("/sse") { ok().render("sse") }
            GET("/users", userHandler::findAllView)
        }
        "/api".nest {
            accept(APPLICATION_JSON).nest {
                GET("/users", userHandler::findAll)
            }
            accept(TEXT_EVENT_STREAM).nest {
                GET("/users", userHandler::stream)
            }
        }
        resources("/**", ClassPathResource("static/"))
    }
}
```

<!-- tabs:start -->

#### ** English **

This DSL is programmatic, meaning that it allows custom registration logic of beans through an `if` expression, a `for` loop, or any other Kotlin constructs. That can be useful when you need to register routes depending on dynamic data (for example, from a database).
#### ** Chinese **

这个 DSL 是程序化的，这意味着它允许通过 `if`表达式、`for`循环或其他任何 Kotlin 构造来定制 Bean 的注册逻辑。当你需要根据动态数据（例如来自数据库的数据）来注册路由时，这可能会很有用。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

See [MiXiT project](https://github.com/mixitconf/mixit/) for a concrete example.
#### ** Chinese **

具体例子见【MiXiT项目】(https://github.com/mixitconf/mixit/)。

<!-- tabs:end -->


### **1.7.2. MockMvc DSL** 

<!-- tabs:start -->

#### ** English **

A Kotlin DSL is provided via `MockMvc` Kotlin extensions in order to provide a more idiomatic Kotlin API and to allow better discoverability (no usage of static methods).
#### ** Chinese **

Kotlin DSL通过`MockMvc` Kotlin扩展提供了一个Kotlin DSL，目的是提供一个更加习惯性的Kotlin API，并允许更好的发现性（不使用静态方法）。

<!-- tabs:end -->


```
val mockMvc: MockMvc = ...
mockMvc.get("/person/{name}", "Lee") {
    secure = true
    accept = APPLICATION_JSON
    headers {
        contentLanguage = Locale.FRANCE
    }
    principal = Principal { "foo" }
}.andExpect {
    status { isOk }
    content { contentType(APPLICATION_JSON) }
    jsonPath("$.name") { value("Lee") }
    content { json("""{"someBoolean": false}""", false) }
}.andDo {
    print()
}
```

### **1.7.3. Kotlin Script Templates** 

<!-- tabs:start -->

#### ** English **

Spring Framework provides a [`ScriptTemplateView`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/web/servlet/view/script/ScriptTemplateView.html) which supports [JSR-223](https://www.jcp.org/en/jsr/detail?id=223) to render templates by using script engines.
#### ** Chinese **

Spring Framework提供了一个[`ScriptTemplateView`](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/web/servlet/view/script/ScriptTemplateView.html)，它支持[JSR-223](https://www.jcp.org/en/jsr/detail?id=223)通过使用脚本引擎渲染模板。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

By leveraging `kotlin-script-runtime` and `scripting-jsr223-embeddable` dependencies, it is possible to use such feature to render Kotlin-based templates with [kotlinx.html](https://github.com/Kotlin/kotlinx.html) DSL or Kotlin multiline interpolated `String`.
#### ** Chinese **

通过利用`kotlin-script-runtime`和`scripting-jsr223-embeddable`的依赖关系，可以使用这样的功能来渲染基于Kotlin的模板，使用[kotlinx.html](https://github.com/Kotlin/kotlinx.html) DSL或Kotlin多行插值`String`。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

`build.gradle.kts`
#### ** Chinese **

`build.gradle.kts`

<!-- tabs:end -->


```
dependencies {
    compile("org.jetbrains.kotlin:kotlin-script-runtime:${kotlinVersion}")
    runtime("org.jetbrains.kotlin:kotlin-scripting-jsr223-embeddable:${kotlinVersion}")
}
```

<!-- tabs:start -->

#### ** English **

Configuration is usually done with `ScriptTemplateConfigurer` and `ScriptTemplateViewResolver` beans.
#### ** Chinese **

配置通常用`ScriptTemplateConfigurer`和`ScriptTemplateViewResolver` bean来完成。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

`KotlinScriptConfiguration.kt`
#### ** Chinese **

`KotlinScriptConfiguration.kt`。

<!-- tabs:end -->


```java
@Configuration
class KotlinScriptConfiguration {

    @Bean
    fun kotlinScriptConfigurer() = ScriptTemplateConfigurer().apply {
        engineName = "kotlin"
        setScripts("scripts/render.kts")
        renderFunction = "render"
        isSharedEngine = false
    }

    @Bean
    fun kotlinScriptViewResolver() = ScriptTemplateViewResolver().apply {
        setPrefix("templates/")
        setSuffix(".kts")
    }
}
```

<!-- tabs:start -->

#### ** English **

See the [kotlin-script-templating](https://github.com/sdeleuze/kotlin-script-templating) example project for more details.
#### ** Chinese **

详情请参见[kotlin-script-templating](https://github.com/sdeleuze/kotlin-script-templating)示例项目。

<!-- tabs:end -->


### **1.8. Coroutines** 

<!-- tabs:start -->

#### ** English **

Kotlin [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) are Kotlin lightweight threads allowing to write non-blocking code in an imperative way. On language side, suspending functions provides an abstraction for asynchronous operations while on library side [kotlinx.coroutines](https://github.com/Kotlin/kotlinx.coroutines) provides functions like [`async { }`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/async.html) and types like [`Flow`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html).
#### ** Chinese **

Kotlin [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html)是Kotlin的轻量级线程，允许以必须的方式编写非阻塞代码。在语言方面，悬浮函数为异步操作提供了一个抽象，而在库方面，[kotlinx.coroutines](https://github.com/Kotlin/kotlinx.coroutines)提供了像[`async { }`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/async.html)这样的函数和像[`Flow`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html)这样的类型。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring Framework provides support for Coroutines on the following scope:
#### ** Chinese **

Spring框架在以下范围内提供了对Coroutines的支持。

<!-- tabs:end -->


### **1.8.1. Dependencies** 

<!-- tabs:start -->

#### ** English **

Coroutines support is enabled when `kotlinx-coroutines-core` and `kotlinx-coroutines-reactor` dependencies are in the classpath:
#### ** Chinese **

当 `kotlinx-coroutines-core`和`kotlinx-coroutines-reactor`依赖项在classpath中时，Coroutines支持被启用。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

`build.gradle.kts`
#### ** Chinese **

`build.gradle.kts`

<!-- tabs:end -->


```
dependencies {

    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-core:${coroutinesVersion}")
    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-reactor:${coroutinesVersion}")
}
```

<!-- tabs:start -->

#### ** English **

Version `1.3.0` and above are supported.
#### ** Chinese **

支持`1.3.0`及以上版本。

<!-- tabs:end -->


### **1.8.2. How Reactive translates to Coroutines?** 

<!-- tabs:start -->

#### ** English **

For return values, the translation from Reactive to Coroutines APIs is the following:
#### ** Chinese **

对于返回值，从 Reactive 到 Coroutines API 的翻译如下。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- [Deferred](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-deferred/index.html) and [Flow](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html) return values support in Spring WebFlux annotated `@Controller`

- Suspending function support in Spring WebFlux annotated `@Controller`

- Extensions for WebFlux [client](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.client/index.html) and [server](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/index.html) functional API.

- WebFlux.fn [coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html) DSL

- Suspending function and `Flow` support in RSocket `@MessageMapping` annotated methods

- Extensions for [`RSocketRequester`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.messaging.rsocket/index.html)

- `fun handler(): Mono<Void>` becomes `suspend fun handler()`

- `fun handler(): Mono<T>` becomes `suspend fun handler(): T` or `suspend fun handler(): T?` depending on if the `Mono` can be empty or not (with the advantage of being more statically typed)

- `fun handler(): Flux<T>` becomes `fun handler(): Flow<T>`

#### ** Chinese **

- 在Spring WebFlux注释的`@Controller`中支持[Deferred](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines/-deferred/index.html]和[Flow](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html)返回值。

- 在Spring WebFlux注释的`@Controller`中的悬浮函数支持

- WebFlux[客户端](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.client/index.html)和[服务器](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/index.html)功能API的扩展。

- WebFlux.fn [coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html) DSL

- 在RSocket `@MessageMessageMapping`注解的方法中支持悬浮函数和`Flow`</x>。

- [`RSocketRequester`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.messaging.rsocket/index.html)的扩展程序

- `fun handler(): Mono<Void>`变为`suspend fun handler()` `suspend fun handler()`

- `fun handler(): Mono<T>`变为`suspend fun handler(): T`或`suspend fun handler(): T?`，取决于`Mono`是否可以为空（优点是更多的静态键入）。

- `fun handler(): Flux<T>`变为`fun handler(): Flow<T>`变为<x>fun handler()


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

For input parameters:
#### ** Chinese **

对于输入参数：

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- If laziness is not needed, `fun handler(mono: Mono<T>)` becomes `fun handler(value: T)` since a suspending functions can be invoked to get the value parameter.

- If laziness is needed, `fun handler(mono: Mono<T>)` becomes `fun handler(supplier: suspend () → T)` or `fun handler(supplier: suspend () → T?)`

#### ** Chinese **

- 如果不需要懒惰，`fun handler(mono: Mono<T>)`就会变成`fun handler(value: T)`，因为可以调用悬浮函数来获取值参数。

- 如果需要偷懒，`fun handler(mono: Mono<T>)`就会变成`fun handler(supporter: suspend () → T)`或<x>fun handler(supporter: suspend () → T?


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

[`Flow`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html) is `Flux` equivalent in Coroutines world, suitable for hot or cold stream, finite or infinite streams, with the following main differences:
#### ** Chinese **

`Flow`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/index.html)是`Flux`在Coroutines世界中的等效，适用于热流或冷流、有限流或无限流，主要区别如下。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- `Flow` is push-based while `Flux` is push-pull hybrid

- Backpressure is implemented via suspending functions

- `Flow` has only a [single suspending ](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html)[`collect`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html)[ method](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html) and operators are implemented as [extensions](https://kotlinlang.org/docs/reference/extensions.html)

- [Operators are easy to implement](https://github.com/Kotlin/kotlinx.coroutines/tree/master/kotlinx-coroutines-core/common/src/flow/operators) thanks to Coroutines

- Extensions allow to add custom operators to `Flow`

- Collect operations are suspending functions

- [`map`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/map.html)[ operator](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/map.html) supports asynchronous operation (no need for `flatMap`) since it takes a suspending function parameter

#### ** Chinese **

- `Flow`是基于推动式的，而`Flux`是推拉式混合型的。

- 背压是通过悬挂功能实现的

- `Flow`只有一个[单吊挂](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html)[`collect`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html)[方法](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/collect.html)，而操作符是以[扩展](https://kotlinlang.org/docs/reference/extensions.html)的形式实现的。

- 运算子很容易实现](https://github.com/Kotlin/kotlinx.coroutines/tree/master/kotlinx-coroutines-core/common/src/flow/operators)感谢Coroutines

- 扩展允许在`Flow`中添加自定义操作符。

- 采集操作是暂停功能

- [`map`](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/map.html)[operator](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/map.html)支持异步操作（不需要`flatMap`），因为它需要一个悬浮函数参数


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

Read this blog post about [Going Reactive with Spring, Coroutines and Kotlin Flow](https://spring.io/blog/2019/04/12/going-reactive-with-spring-coroutines-and-kotlin-flow) for more details, including how to run code concurrently with Coroutines.
#### ** Chinese **

阅读这篇关于[用Spring、Coroutines和Kotlin Flow来进行反应式开发](https://spring.io/blog/2019/04/12/going-reactive-with-spring-coroutines-and-kotlin-flow)的博文，了解更多细节，包括如何与Coroutines并发运行代码。

<!-- tabs:end -->


### **1.8.3. Controllers** 

<!-- tabs:start -->

#### ** English **

Here is an example of a Coroutines `@RestController`.
#### ** Chinese **

下面是一个Coroutines`@RestController`的例子。

<!-- tabs:end -->


```java
@RestController
class CoroutinesRestController(client: WebClient, banner: Banner) {

    @GetMapping("/suspend")
    suspend fun suspendingEndpoint(): Banner {
        delay(10)
        return banner
    }

    @GetMapping("/flow")
    fun flowEndpoint() = flow {
        delay(10)
        emit(banner)
        delay(10)
        emit(banner)
    }

    @GetMapping("/deferred")
    fun deferredEndpoint() = GlobalScope.async {
        delay(10)
        banner
    }

    @GetMapping("/sequential")
    suspend fun sequential(): List<Banner> {
        val banner1 = client
                .get()
                .uri("/suspend")
                .accept(MediaType.APPLICATION_JSON)
                .awaitExchange()
                .awaitBody<Banner>()
        val banner2 = client
                .get()
                .uri("/suspend")
                .accept(MediaType.APPLICATION_JSON)
                .awaitExchange()
                .awaitBody<Banner>()
        return listOf(banner1, banner2)
    }

    @GetMapping("/parallel")
    suspend fun parallel(): List<Banner> = coroutineScope {
        val deferredBanner1: Deferred<Banner> = async {
            client
                    .get()
                    .uri("/suspend")
                    .accept(MediaType.APPLICATION_JSON)
                    .awaitExchange()
                    .awaitBody<Banner>()
        }
        val deferredBanner2: Deferred<Banner> = async {
            client
                    .get()
                    .uri("/suspend")
                    .accept(MediaType.APPLICATION_JSON)
                    .awaitExchange()
                    .awaitBody<Banner>()
        }
        listOf(deferredBanner1.await(), deferredBanner2.await())
    }

    @GetMapping("/error")
    suspend fun error() {
        throw IllegalStateException()
    }

    @GetMapping("/cancel")
    suspend fun cancel() {
        throw CancellationException()
    }

}
```

<!-- tabs:start -->

#### ** English **

View rendering with a `@Controller` is also supported.
#### ** Chinese **

还支持使用`@Controller`进行视图渲染。

<!-- tabs:end -->


```java
@Controller
class CoroutinesViewController(banner: Banner) {

    @GetMapping("/")
    suspend fun render(model: Model): String {
        delay(10)
        model["banner"] = banner
        return "index"
    }
}
```

### **1.8.4. WebFlux.fn** 

<!-- tabs:start -->

#### ** English **

Here is an example of Coroutines router defined via the [coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html) DSL and related handlers.
#### ** Chinese **

下面是一个通过[coRouter { }](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/kdoc-api/spring-framework/org.springframework.web.reactive.function.server/co-router.html)定义的Coroutines路由器的例子。 DSL和相关的处理程序；

<!-- tabs:end -->


```java
@Configuration
class RouterConfiguration {

    @Bean
    fun mainRouter(userHandler: UserHandler) = coRouter {
        GET("/", userHandler::listView)
        GET("/api/user", userHandler::listApi)
    }
}
```

```java
class UserHandler(builder: WebClient.Builder) {

    private val client = builder.baseUrl("...").build()

    suspend fun listView(request: ServerRequest): ServerResponse =
            ServerResponse.ok().renderAndAwait("users", mapOf("users" to
            client.get().uri("...").awaitExchange().awaitBody<User>()))

    suspend fun listApi(request: ServerRequest): ServerResponse =
                ServerResponse.ok().contentType(MediaType.APPLICATION_JSON).bodyAndAwait(
                client.get().uri("...").awaitExchange().awaitBody<User>())
}
```

### **1.8.5. Transactions** 

<!-- tabs:start -->

#### ** English **

Transactions on Coroutines are supported via the programmatic variant of the Reactive transaction management provided as of Spring Framework 5.2.
#### ** Chinese **

Coroutines上的事务通过Spring Framework 5.2提供的Reactive事务管理的程序化变体来支持。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For suspending functions, a `TransactionalOperator.executeAndAwait` extension is provided.
#### ** Chinese **

对于悬浮函数，提供了一个`TransactionalOperator.executeAndAwait`扩展。

<!-- tabs:end -->


```java
import org.springframework.transaction.reactive.executeAndAwait

class PersonRepository(private val operator: TransactionalOperator) {

    suspend fun initDatabase() = operator.executeAndAwait {
        insertPerson1()
        insertPerson2()
    }

    private suspend fun insertPerson1() {
        // INSERT SQL statement
    }

    private suspend fun insertPerson2() {
        // INSERT SQL statement
    }
}
```

<!-- tabs:start -->

#### ** English **

For Kotlin `Flow`, a `Flow<T>.transactional` extension is provided.
#### ** Chinese **

对于Kotlin `Flow`，提供了一个`Flow<T>.transactional`扩展。

<!-- tabs:end -->


```java
import org.springframework.transaction.reactive.transactional

class PersonRepository(private val operator: TransactionalOperator) {

    fun updatePeople() = findPeople().map(::updatePerson).transactional(operator)

    private fun findPeople(): Flow<Person> {
        // SELECT SQL statement
    }

    private suspend fun updatePerson(person: Person): Person {
        // UPDATE SQL statement
    }
}
```

### **1.9. Spring Projects in Kotlin** 

<!-- tabs:start -->

#### ** English **

This section provides some specific hints and recommendations worth for developing Spring projects in Kotlin.
#### ** Chinese **

本节提供了一些具体的提示和建议，值得在Kotlin中开发Spring项目。

<!-- tabs:end -->


### **1.9.1. Final by Default** 

<!-- tabs:start -->

#### ** English **

By default, [all classes in Kotlin are ](https://discuss.kotlinlang.org/t/classes-final-by-default/166)[`final`](https://discuss.kotlinlang.org/t/classes-final-by-default/166). The `open` modifier on a class is the opposite of Java’s `final`: It allows others to inherit from this class. This also applies to member functions, in that they need to be marked as `open` to be overridden.
#### ** Chinese **

默认情况下，【Kotlin中的所有类都是】(https://discuss.kotlinlang.org/t/classes-final-by-default/166)[`final`](https://discuss.kotlinlang.org/t/classes-final-by-default/166)。类上的`open`修改器与Java的`final`相反：它允许其他人继承这个类。这也适用于成员函数，因为它们需要被标记为`open`才能被覆盖。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

While Kotlin’s JVM-friendly design is generally frictionless with Spring, this specific Kotlin feature can prevent the application from starting, if this fact is not taken into consideration. This is because Spring beans (such as `@Configuration` annotated classes which by default need to be extended at runtime for technical reasons) are normally proxied by CGLIB. The workaround is to add an `open` keyword on each class and member function of Spring beans that are proxied by CGLIB, which can quickly become painful and is against the Kotlin principle of keeping code concise and predictable.
#### ** Chinese **

虽然Kotlin的JVM友好型设计一般与Spring无摩擦，但如果不考虑到这一事实，Kotlin的这一特殊特性可能会导致应用程序无法启动。这是因为Spring Bean（如`@Configuration`注释类，由于技术原因，默认情况下需要在运行时进行扩展）通常是由CGLIB代理的。变通的方法是在Spring beans的每个类和成员函数上添加一个`open`关键字，这可能很快就会变得很痛苦，而且有违Kotlin保持代码简洁和可预测性的原则。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

It is also possible to avoid CGLIB proxies for configuration classes by using `@Configuration(proxyBeanMethods = false)`. See [`proxyBeanMethods`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/context/annotation/Configuration.html#proxyBeanMethods--)[ Javadoc](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/context/annotation/Configuration.html#proxyBeanMethods--) for more details.
#### ** Chinese **

也可以通过使用`@Configuration(proxyBeanMethods = false)`来避免CGLIB代理配置类。更多详情请参见 [`proxyBeanMethods`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/context/annotation/Configuration.html#proxyBeanMethods--)[ Javadoc](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/context/annotation/Configuration.html#proxyBeanMethods--)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Fortunately, Kotlin provides a [`kotlin-spring`](https://kotlinlang.org/docs/reference/compiler-plugins.html#kotlin-spring-compiler-plugin) plugin (a preconfigured version of the `kotlin-allopen` plugin) that automatically opens classes and their member functions for types that are annotated or meta-annotated with one of the following annotations:
#### ** Chinese **

幸运的是，Kotlin提供了一个[`kotlin-spring`](https://kotlinlang.org/docs/reference/compiler-plugins.html#kotlin-spring-compiler-plugin)插件(`kotlin-allopen`插件的预配置版本)，它可以自动打开类及其成员函数，用于被注释或元注释的类型，并使用以下注释之一。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- `@Component`

- `@Async`

- `@Transactional`

- `@Cacheable`

#### ** Chinese **

- `@Component`</x>

- `@Async`

- `@Transactional`</x>

- `@Cacheable`


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

Meta-annotation support means that types annotated with `@Configuration`, `@Controller`, `@RestController`, `@Service`, or `@Repository` are automatically opened since these annotations are meta-annotated with `@Component`.
#### ** Chinese **

元注释支持意味着，由于这些注释是以 `@Configuration`、`@Controller`、`@RestController`、`@Service`或`@Repository`为元注释的类型会被自动打开，因为这些注释是以`@Component`为元注释的。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

[start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project) enables the `kotlin-spring` plugin by default. So, in practice, you can write your Kotlin beans without any additional `open` keyword, as in Java.
#### ** Chinese **

[start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project)默认启用了`kotlin-spring`插件。因此，在实践中，你可以像在Java中一样，不需要任何额外的`open`关键字就可以编写你的Kotlin Bean。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The Kotlin code samples in Spring Framework documentation do not explicitly specify `open` on the classes and their member functions. The samples are written for projects using the `kotlin-allopen` plugin, since this is the most commonly used setup.
#### ** Chinese **

Spring Framework 文档中的 Kotlin 代码示例没有在类及其成员函数上明确指定 `open`。这些示例是为使用`kotlin-allopen`插件的项目编写的，因为这是最常用的设置。

<!-- tabs:end -->


### **1.9.2. Using Immutable Class Instances for Persistence** 

<!-- tabs:start -->

#### ** English **

In Kotlin, it is convenient and considered to be a best practice to declare read-only properties within the primary constructor, as in the following example:
#### ** Chinese **

在Kotlin中，在主构造函数中声明只读属性是很方便的，也被认为是最好的做法，如下例所示。

<!-- tabs:end -->


```java
class Person(val name: String, val age: Int)
```

<!-- tabs:start -->

#### ** English **

You can optionally add [the ](https://kotlinlang.org/docs/reference/data-classes.html)[`data`](https://kotlinlang.org/docs/reference/data-classes.html)[ keyword](https://kotlinlang.org/docs/reference/data-classes.html) to make the compiler automatically derive the following members from all properties declared in the primary constructor:
#### ** Chinese **

你可以选择添加[the ](https://kotlinlang.org/docs/reference/data-classes.html)[`data`](https://kotlinlang.org/docs/reference/data-classes.html)[keyword](https://kotlinlang.org/docs/reference/data-classes.html)，使编译器自动从主构造函数中声明的所有属性中派生出以下成员。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- `equals()` and `hashCode()`

- `toString()` of the form `"User(name=John, age=42)"`

- `componentN()` functions that correspond to the properties in their order of declaration

- `copy()` function

#### ** Chinese **

- `equals()` 和 `hashCode()`

- `toString()`的形式`"User(name=John, age=42)"`

- `componentN()`函数按声明顺序对应属性的函数

- `copy()`函数


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

As the following example shows, this allows for easy changes to individual properties, even if `Person` properties are read-only:
#### ** Chinese **

正如下面的示例所示，这使得即使`Person`属性是只读的，也可以轻松更改单个属性。

<!-- tabs:end -->


```
data class Person(val name: String, val age: Int)

val jack = Person(name = "Jack", age = 1)
val olderJack = jack.copy(age = 2)
```

<!-- tabs:start -->

#### ** English **

Common persistence technologies (such as JPA) require a default constructor, preventing this kind of design. Fortunately, there is a workaround for this [“default constructor hell”](https://stackoverflow.com/questions/32038177/kotlin-with-jpa-default-constructor-hell), since Kotlin provides a [`kotlin-jpa`](https://kotlinlang.org/docs/reference/compiler-plugins.html#kotlin-jpa-compiler-plugin) plugin that generates synthetic no-arg constructor for classes annotated with JPA annotations.
#### ** Chinese **

常见的持久化技术（如JPA）需要一个默认的构造函数，从而阻止了这种设计。幸运的是，有一个解决这个问题的方法["default constructor hell"](https://stackoverflow.com/questions/32038177/kotlin-with-jpa-default-constructor-hell)，因为Kotlin提供了一个[`kotlin-jpa`](https://kotlinlang.org/docs/reference/compiler-plugins.html#kotlin-jpa-compiler-plugin)插件，可以为带有JPA注释的类生成合成无arg构造函数。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you need to leverage this kind of mechanism for other persistence technologies, you can configure the [`kotlin-noarg`](https://kotlinlang.org/docs/reference/compiler-plugins.html#how-to-use-no-arg-plugin) plugin.
#### ** Chinese **

如果你需要利用这种机制来实现其他持久化技术，你可以配置[`kotlin-noarg`](https://kotlinlang.org/docs/reference/compiler-plugins.html#how-to-use-no-arg-plugin)插件。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

As of the Kay release train, Spring Data supports Kotlin immutable class instances and does not require the `kotlin-noarg` plugin if the module uses Spring Data object mappings (such as MongoDB, Redis, Cassandra, and others).
#### ** Chinese **

从Kay发布列车开始，Spring Data支持Kotlin不可变类实例，如果模块使用Spring Data对象映射（如MongoDB、Redis、Cassandra等），则不需要`kotlin-noarg`插件。

<!-- tabs:end -->


### **1.9.3. Injecting Dependencies** 

<!-- tabs:start -->

#### ** English **

Our recommendation is to try to favor constructor injection with `val` read-only (and non-nullable when possible) [properties](https://kotlinlang.org/docs/reference/properties.html), as the following example shows:
#### ** Chinese **

我们的建议是尽量用`val`只读(并且在可能的情况下是不可空的)[properties](https://kotlinlang.org/docs/reference/properties.html)的构造函数注入，如下例所示。

<!-- tabs:end -->


```java
@Component
class YourBean(
    private val mongoTemplate: MongoTemplate,
    private val solrClient: SolrClient
)
```

<!-- tabs:start -->

#### ** English **

Classes with a single constructor have their parameters automatically autowired. That’s why there is no need for an explicit `@Autowired constructor` in the example shown above.
#### ** Chinese **

具有单个构造函数的类都有自动自动连线的参数。这就是为什么在上面的例子中不需要显式的`@Autowired构造函数`的原因。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you really need to use field injection, you can use the `lateinit var` construct, as the following example shows:
#### ** Chinese **

如果你真的需要使用字段注入，可以使用`lateinit var`构造，如下例所示。

<!-- tabs:end -->


```java
@Component
class YourBean {

    @Autowired
    lateinit var mongoTemplate: MongoTemplate

    @Autowired
    lateinit var solrClient: SolrClient
}
```

### **1.9.4. Injecting Configuration Properties** 

<!-- tabs:start -->

#### ** English **

In Java, you can inject configuration properties by using annotations (such as `@Value("${property}")`). However, in Kotlin, `$` is a reserved character that is used for [string interpolation](https://kotlinlang.org/docs/reference/idioms.html#string-interpolation).
#### ** Chinese **

在Java中，你可以通过使用注释注入配置属性（如`@Value("")`）。但是，在Kotlin中，`$`是一个保留字符，用于[字符串插值](https://kotlinlang.org/docs/reference/idioms.html#string-interpolation)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Therefore, if you wish to use the `@Value` annotation in Kotlin, you need to escape the `$` character by writing `@Value("\${property}")`.
#### ** Chinese **

因此，如果你想在Kotlin中使用`@Value`注释，你需要通过写`@Value("17536{property}")`来转义。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you use Spring Boot, you should probably use [`@ConfigurationProperties`](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html#boot-features-external-config-typesafe-configuration-properties) instead of `@Value` annotations.
#### ** Chinese **

如果您使用 Spring Boot，您可能应该使用 [`@ConfigurationProperties`](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html#boot-features-external-config-typesafe-configuration-properties)，而不是 `@Value` 注解。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

As an alternative, you can customize the property placeholder prefix by declaring the following configuration beans:
#### ** Chinese **

作为替代方案，你可以通过声明以下配置Bean来自定义属性占位符前缀。

<!-- tabs:end -->


```java
@Bean
fun propertyConfigurer() = PropertySourcesPlaceholderConfigurer().apply {
    setPlaceholderPrefix("%{")
}
```

<!-- tabs:start -->

#### ** English **

You can customize existing code (such as Spring Boot actuators or `@LocalServerPort`) that uses the `${…​}` syntax, with configuration beans, as the following example shows:
#### ** Chinese **
<!-- tabs:end -->


```java
@Bean
fun kotlinPropertyConfigurer() = PropertySourcesPlaceholderConfigurer().apply {
    setPlaceholderPrefix("%{")
    setIgnoreUnresolvablePlaceholders(true)
}

@Bean
fun defaultPropertyConfigurer() = PropertySourcesPlaceholderConfigurer()
```

### **1.9.5. Checked Exceptions** 

<!-- tabs:start -->

#### ** English **

Java and [Kotlin exception handling](https://kotlinlang.org/docs/reference/exceptions.html) are pretty close, with the main difference being that Kotlin treats all exceptions as unchecked exceptions. However, when using proxied objects (for example classes or methods annotated with `@Transactional`), checked exceptions thrown will be wrapped by default in an `UndeclaredThrowableException`.
#### ** Chinese **

Java和[Kotlin 异常处理](https://kotlinlang.org/docs/reference/exceptions.html)非常接近，主要的区别在于Kotlin将所有的异常视为未检查的异常。但是，当使用proxied对象时（例如用`@Transactional`注释的类或方法），抛出的检查过的异常将默认被封装在`UndeclaredThrowableException`中。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To get the original exception thrown like in Java, methods should be annotated with [`@Throws`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.jvm/-throws/index.html) to specify explicitly the checked exceptions thrown (for example `@Throws(IOException::class)`).
#### ** Chinese **

要获得像Java中那样的原始异常抛出，方法应该用[`@Throws`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.jvm/-throws/index.html)来注释，以明确指定所抛出的检查过的异常(例如`@Throws(IOException::class)`)。

<!-- tabs:end -->


### **1.9.6. Annotation Array Attributes** 

<!-- tabs:start -->

#### ** English **

Kotlin annotations are mostly similar to Java annotations, but array attributes (which are extensively used in Spring) behave differently. As explained in the [Kotlin documentation](https://kotlinlang.org/docs/reference/annotations.html) you can omit the `value` attribute name, unlike other attributes, and specify it as a `vararg` parameter.
#### ** Chinese **

Kotlin 注释大多与 Java 注释相似，但数组属性（在 Spring 中被广泛使用）的行为方式不同。正如[Kotlin文档](https://kotlinlang.org/docs/reference/annotations.html)中解释的那样，你可以省略`value`属性名，不像其他属性那样，可以指定为`vararg`参数。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To understand what that means, consider `@RequestMapping` (which is one of the most widely used Spring annotations) as an example. This Java annotation is declared as follows:
#### ** Chinese **

要理解这意味着什么，请以`@RequestMapping`（它是最广泛使用的Spring注释之一）为例。这个Java注释的声明如下。

<!-- tabs:end -->


```java
public @interface RequestMapping {

    @AliasFor("path")
    String[] value() default {};

    @AliasFor("value")
    String[] path() default {};

    RequestMethod[] method() default {};

    // ...
}
```

<!-- tabs:start -->

#### ** English **

The typical use case for `@RequestMapping` is to map a handler method to a specific path and method. In Java, you can specify a single value for the annotation array attribute, and it is automatically converted to an array.
#### ** Chinese **

`@RequestMapping`的典型用例是将处理程序方法映射到特定的路径和方法。在Java中，你可以为注解数组属性指定一个单一的值，并将其自动转换为数组。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

That is why one can write `@RequestMapping(value = "/toys", method = RequestMethod.GET)` or `@RequestMapping(path = "/toys", method = RequestMethod.GET)`.
#### ** Chinese **

这就是为什么可以写`@RequestMapping(value = "/toys", method = RequestMethod.GET)`或`@RequestMapping(path = "/toys", method = RequestMethod.GET)`。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

However, in Kotlin, you must write `@RequestMapping("/toys", method = [RequestMethod.GET])` or `@RequestMapping(path = ["/toys"], method = [RequestMethod.GET])` (square brackets need to be specified with named array attributes).
#### ** Chinese **

但是，在Kotlin中，你必须写`@RequestMapping("/toys", method = [RequestMethod.GET])`或`@RequestMapping(path = ["/toys"], method = [RequestMethod.GET])`（方括号中需要指定命名的数组属性）。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

An alternative for this specific `method` attribute (the most common one) is to use a shortcut annotation, such as `@GetMapping`, `@PostMapping`, and others.
#### ** Chinese **

这个特定的`method`属性（最常见的属性）的另一种选择是使用快捷方式注释，如`@GetMapping`、`@PostMapping`等。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If the `@RequestMapping` `method` attribute is not specified, all HTTP methods will be matched, not only the `GET` method.
#### ** Chinese **

如果没有指定 `@RequestMapping` `method`属性，那么所有的HTTP方法都将被匹配，而不仅仅是`GET`方法。

<!-- tabs:end -->


### **1.9.7. Testing** 

<!-- tabs:start -->

#### ** English **

This section addresses testing with the combination of Kotlin and Spring Framework. The recommended testing framework is [JUnit 5](https://junit.org/junit5/) along with [Mockk](https://mockk.io/) for mocking.
#### ** Chinese **

本节讨论的是使用Kotlin和Spring框架的组合进行测试。推荐的测试框架是[JUnit 5](https://junit.org/junit5/)和[Mockk](https://mockk.io/)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you are using Spring Boot, see [this related documentation](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-kotlin-testing).
#### ** Chinese **

如果您使用的是Spring Boot，请参阅[此相关文档](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-kotlin-testing)。

<!-- tabs:end -->


### **Constructor injection** 

<!-- tabs:start -->

#### ** English **

As described in the [dedicated section](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/testing.html#testcontext-junit-jupiter-di#spring-web-reactive), JUnit 5 allows constructor injection of beans which is pretty useful with Kotlin in order to use `val` instead of `lateinit var`. You can use [`@TestConstructor(autowireMode = AutowireMode.ALL)`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/test/context/TestConstructor.html) to enable autowiring for all parameters.
#### ** Chinese **

正如在[专门的章节](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/testing.html#testcontext-junit-jupiter-di#spring-web-reactive)中描述的那样，JUnit 5允许构造函数注入Bean，这在Kotlin中是非常有用的，可以使用`val`代替`lateinit var`。你可以使用[`@TestConstructor(autowireMode = AutowireMode.ALL)`](https://docs.spring.io/spring-framework/docs/5.2.6.RELEASE/javadoc-api/org/springframework/test/context/TestConstructor.html)来启用所有参数的自动布线。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

@SpringJUnitConfig(TestConfig::class)
#### ** Chinese **

@SpringJUnitConfig(TestConfig:::class)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

@TestConstructor(autowireMode = AutowireMode.ALL)
#### ** Chinese **

@TestConstructor(autowireMode = AutowireMode.ALL)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

class OrderServiceIntegrationTests(val orderService: OrderService, val customerService: CustomerService) { // tests that use the injected OrderService and CustomerService
#### ** Chinese **

class OrderServiceIntegrationTests(val orderService: OrderService, val customerService: CustomerService) { ///使用注入的OrderService和CustomerService的测试

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

}
#### ** Chinese **

}

<!-- tabs:end -->


### **`PER_CLASS`** ** Lifecycle** 

<!-- tabs:start -->

#### ** English **

Kotlin lets you specify meaningful test function names between backticks (` `). As of JUnit 5, Kotlin test classes can use the `@TestInstance(TestInstance.Lifecycle.PER_CLASS)` annotation to enable single instantiation of test classes, which allows the use of `@BeforeAll` and `@AfterAll` annotations on non-static methods, which is a good fit for Kotlin.
#### ** Chinese **

Kotlin允许你在backticks (` `)之间指定有意义的测试函数名称。从JUnit 5开始，Kotlin的测试类可以使用`@TestInstance(TestInstance.Lifecycle.PER_CLASS)`注解来实现测试类的单一实例化，这允许在非静态方法上使用`@BeforeAll`和`@AfterAll`注解，这对Kotlin来说是一个很好的契合点。

<!-- tabs:end -->




<!-- tabs:start -->

#### ** English **

You can also change the default behavior to `PER_CLASS` thanks to a `junit-platform.properties` file with a `junit.jupiter.testinstance.lifecycle.default = per_class` property.
#### ** Chinese **

您也可以通过`junit-platform.proper_class`文件中的`junit.jupiter.testinstance.lifecycle.default = per_class`属性，将默认行为改为`per_class`。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The following example demonstrates `@BeforeAll` and `@AfterAll` annotations on non-static methods:
#### ** Chinese **

下面的示例演示了非静态方法上的 `@BeforeAll` 和 `@AfterAll` 注释。

<!-- tabs:end -->


```java
@TestInstance(TestInstance.Lifecycle.PER_CLASS)
class IntegrationTests {

  val application = Application(8181)
  val client = WebClient.create("http://localhost:8181")

  @BeforeAll
  fun beforeAll() {
    application.start()
  }

  @Test
  fun `Find all users on HTML page`() {
    client.get().uri("/users")
        .accept(TEXT_HTML)
        .retrieve()
        .bodyToMono<String>()
        .test()
        .expectNextMatches { it.contains("Foo") }
        .verifyComplete()
  }

  @AfterAll
  fun afterAll() {
    application.stop()
  }
}
```

### **Specification-like Tests** 

<!-- tabs:start -->

#### ** English **

You can create specification-like tests with JUnit 5 and Kotlin. The following example shows how to do so:
#### ** Chinese **

你可以用JUnit 5和Kotlin创建类似于规范的测试。下面的例子显示了如何做到这一点。

<!-- tabs:end -->


```java
class SpecificationLikeTests {

  @Nested
  @DisplayName("a calculator")
  inner class Calculator {
     val calculator = SampleCalculator()

     @Test
     fun `should return the result of adding the first number to the second number`() {
        val sum = calculator.sum(2, 4)
        assertEquals(6, sum)
     }

     @Test
     fun `should return the result of subtracting the second number from the first number`() {
        val subtract = calculator.subtract(4, 2)
        assertEquals(2, subtract)
     }
  }
}
```

### **`WebTestClient`** ** Type Inference Issue in Kotlin** 

<!-- tabs:start -->

#### ** English **

Due to a [type inference issue](https://youtrack.jetbrains.com/issue/KT-5464), you must use the Kotlin `expectBody` extension (such as `.expectBody<String>().isEqualTo("toys")`), since it provides a workaround for the Kotlin issue with the Java API.
#### ** Chinese **

由于[类型推理问题](https://youtrack.jetbrains.com/issue/KT-5464)，你必须使用Kotlin `expectBody`扩展（如`.expectBody<String>().isEqualTo("toys")`），因为它提供了一个Java API的Kotlin问题的解决方法。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

See also the related [SPR-16057](https://jira.spring.io/browse/SPR-16057) issue.
#### ** Chinese **

另见相关的[SPR-16057](https://jira.spring.io/browse/SPR-16057)问题。

<!-- tabs:end -->


### **1.10. Getting Started** 

<!-- tabs:start -->

#### ** English **

The easiest way to learn how to build a Spring application with Kotlin is to follow [the dedicated tutorial](https://spring.io/guides/tutorials/spring-boot-kotlin/).
#### ** Chinese **

学习如何使用Kotlin构建一个Spring应用程序的最简单的方法是按照[专用教程](https://spring.io/guides/tutorials/spring-boot-kotlin/)。

<!-- tabs:end -->


### **1.10.1.** **`start.spring.io`** 

<!-- tabs:start -->

#### ** English **

The easiest way to start a new Spring Framework project in Kotlin is to create a new Spring Boot 2 project on [start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project).
#### ** Chinese **

在Kotlin中启动一个新的Spring Framework项目最简单的方法是在[start.spring.io](https://start.spring.io/#!language=kotlin&type=gradle-project)上创建一个新的Spring Boot 2项目。

<!-- tabs:end -->


### **1.10.2. Choosing the Web Flavor** 

<!-- tabs:start -->

#### ** English **

Spring Framework now comes with two different web stacks: [Spring MVC](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web.html#mvc) and [Spring WebFlux](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web-reactive.html#spring-web-reactive).
#### ** Chinese **

Spring Framework现在有两个不同的Web堆栈。 Spring MVC](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web.html#mvc)和[Spring WebFlux](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/web-reactive.html#spring-web-reactive)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring WebFlux is recommended if you want to create applications that will deal with latency, long-lived connections, streaming scenarios or if you want to use the web functional Kotlin DSL.
#### ** Chinese **

如果你想创建能够处理延迟、长效连接、流媒体场景的应用程序，或者你想使用Web功能的Kotlin DSL，推荐使用Spring WebFlux。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For other use cases, especially if you are using blocking technologies such as JPA, Spring MVC and its annotation-based programming model is the recommended choice.
#### ** Chinese **

对于其他用例，特别是当你使用JPA等阻塞技术时，推荐选择Spring MVC及其基于注释的编程模型。

<!-- tabs:end -->


### **1.11. Resources** 

<!-- tabs:start -->

#### ** English **

We recommend the following resources for people learning how to build applications with Kotlin and the Spring Framework:
#### ** Chinese **

我们为学习如何使用Kotlin和Spring框架构建应用程序的人推荐以下资源。

<!-- tabs:end -->


### **1.11.1. Examples** 

<!-- tabs:start -->

#### ** English **

The following Github projects offer examples that you can learn from and possibly even extend:
#### ** Chinese **

下面的Github项目提供了一些例子，你可以从中学习，甚至有可能进行扩展。

<!-- tabs:end -->


### **1.11.2. Issues** 

<!-- tabs:start -->

#### ** English **

The following list categorizes the pending issues related to Spring and Kotlin support:
#### ** Chinese **

下面的列表对与Spring和Kotlin支持相关的未决问题进行了分类。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- [Kotlin language reference](https://kotlinlang.org/docs/reference/)

- [Kotlin Slack](https://slack.kotlinlang.org/) (with a dedicated #spring channel)

- [Stackoverflow, with ](https://stackoverflow.com/questions/tagged/spring+kotlin)[`spring`](https://stackoverflow.com/questions/tagged/spring+kotlin)[ and ](https://stackoverflow.com/questions/tagged/spring+kotlin)[`kotlin`](https://stackoverflow.com/questions/tagged/spring+kotlin)[ tags](https://stackoverflow.com/questions/tagged/spring+kotlin)

- [Try Kotlin in your browser](https://try.kotlinlang.org/)

- [Kotlin blog](https://blog.jetbrains.com/kotlin/)

- [Awesome Kotlin](https://kotlin.link/)

- [spring-boot-kotlin-demo](https://github.com/sdeleuze/spring-boot-kotlin-demo): Regular Spring Boot and Spring Data JPA project

- [mixit](https://github.com/mixitconf/mixit): Spring Boot 2, WebFlux, and Reactive Spring Data MongoDB

- [spring-kotlin-functional](https://github.com/sdeleuze/spring-kotlin-functional): Standalone WebFlux and functional bean definition DSL

- [spring-kotlin-fullstack](https://github.com/sdeleuze/spring-kotlin-fullstack): WebFlux Kotlin fullstack example with Kotlin2js for frontend instead of JavaScript or TypeScript

- [spring-petclinic-kotlin](https://github.com/spring-petclinic/spring-petclinic-kotlin): Kotlin version of the Spring PetClinic Sample Application

- [spring-kotlin-deepdive](https://github.com/sdeleuze/spring-kotlin-deepdive): A step-by-step migration guide for Boot 1.0 and Java to Boot 2.0 and Kotlin

- [spring-cloud-gcp-kotlin-app-sample](https://github.com/spring-cloud/spring-cloud-gcp/tree/master/spring-cloud-gcp-kotlin-samples/spring-cloud-gcp-kotlin-app-sample): Spring Boot with Google Cloud Platform Integrations

- Spring Framework
#### ** Chinese **

- [Kotlin语言参考](https://kotlinlang.org/docs/reference/)

- Kotlin Slack](https://slack.kotlinlang.org/)（有专门的#spring频道）。

- [Stackoverflow, with ](https://stackoverflow.com/questions/tagged/spring+kotlin)[`spring`](https://stackoverflow.com/questions/tagged/spring+kotlin)[和](https://stackoverflow.com/questions/tagged/spring+kotlin)[`kotlin`](https://stackoverflow.com/questions/tagged/spring+kotlin)[标签](https://stackoverflow.com/questions/tagged/spring+kotlin)

- [在浏览器中试用Kotlin](https://try.kotlinlang.org/)

- [Kotlin博客](https://blog.jetbrains.com/kotlin/)

- [Awesome Kotlin](https://kotlin.link/)

- spring-bootlin-demo](https://github.com/sdeleuze/spring-boot-kotlin-demo)。常规Spring Boot和Spring Data JPA项目

- [mixit](https://github.com/mixitconf/mixit): Spring Boot 2, WebFlux, 和Reactive Spring Data MongoDB

- spring-kotlin-functional](https://github.com/sdeleuze/spring-kotlin-functional)。独立的 WebFlux 和功能豆定义 DSL

- spring-kotlin-fullstack](https://github.com/sdeleuze/spring-kotlin-fullstack)。WebFlux Kotlin fullstack示例，前端用Kotlin2js代替JavaScript或TypeScript。

- spring-petclinic-kotlin](https://github.com/spring-petclinic/spring-petclinic-kotlin)。Spring PetClinic样本应用程序的Kotlin版

- spring-kotlin-deepdive](https://github.com/sdeleuze/spring-kotlin-deepdive)。Boot 1.0和Java到Boot 2.0和Kotlin的分步迁移指南

- spring-cloud-gcp-kotlin-app-sample](https://github.com/spring-cloud/spring-cloud-gcp/tree/master/spring-cloud-gcp-kotlin-samples/spring-cloud-gcp-kotlin-app-sample): 与谷歌云平台集成的Spring Boot

- 春天框架

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Unable to use WebTestClient with mock server in Kotlin](https://github.com/spring-projects/spring-framework/issues/20606)
#### ** Chinese **

  - 在Kotlin中无法使用WebTestClient与模拟服务器](https://github.com/spring-projects/spring-framework/issues/20606)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Support null-safety at generics, varargs and array elements level](https://github.com/spring-projects/spring-framework/issues/20496)
#### ** Chinese **

  - [在属类、varargs和数组元素层面支持空安全](https://github.com/spring-projects/spring-framework/issues/20496)

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- Kotlin
#### ** Chinese **

- Kotlin

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Parent issue for Spring Framework support](https://youtrack.jetbrains.com/issue/KT-6380)
#### ** Chinese **

  - [支持Spring框架的母问题](https://youtrack.jetbrains.com/issue/KT-6380)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Kotlin requires type inference where Java doesn’t](https://youtrack.jetbrains.com/issue/KT-5464)
#### ** Chinese **

  - Kotlin需要类型推理，而Java不需要类型推理](https://youtrack.jetbrains.com/issue/KT-5464)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Smart cast regression with open classes](https://youtrack.jetbrains.com/issue/KT-20283)
#### ** Chinese **

  - [Smart cast regression with open classes](https://youtrack.jetbrains.com/issue/KT-20283)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Impossible to pass not all SAM argument as function](https://youtrack.jetbrains.com/issue/KT-14984)
#### ** Chinese **

  - 不可能将不是所有的SAM参数都作为函数传递](https://youtrack.jetbrains.com/issue/KT-14984)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Support JSR 223 bindings directly via script variables](https://youtrack.jetbrains.com/issue/KT-15125)
#### ** Chinese **

  - 直接通过脚本变量支持JSR 223绑定](https://youtrack.jetbrains.com/issue/KT-15125)

<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

  - [Kotlin properties do not override Java-style getters and setters](https://youtrack.jetbrains.com/issue/KT-6653)
#### ** Chinese **

  - Kotlin属性不覆盖Java风格的getter和setter](https://youtrack.jetbrains.com/issue/KT-6653)

<!-- tabs:end -->


## **2. Apache Groovy** 

<!-- tabs:start -->

#### ** English **

Groovy is a powerful, optionally typed, and dynamic language, with static-typing and static compilation capabilities. It offers a concise syntax and integrates smoothly with any existing Java application.
#### ** Chinese **

Groovy是一种强大的、可选类型化的动态语言，具有静态类型化和静态编译功能。它提供了一个简洁的语法，并与任何现有的Java应用程序顺利地集成在一起。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The Spring Framework provides a dedicated `ApplicationContext` that supports a Groovy-based Bean Definition DSL. For more details, see [The Groovy Bean Definition DSL](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#groovy-bean-definition-dsl).
#### ** Chinese **

Spring框架提供了一个专用的`ApplicationContext`，它支持基于Groovy的Bean Definition DSL。有关详细信息，请参阅[The Groovy Bean Definition DSL](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#groovy-bean-definition-dsl)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Further support for Groovy, including beans written in Groovy, refreshable script beans, and more is available in [Dynamic Language Support](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language).
#### ** Chinese **

进一步支持Groovy，包括用Groovy编写的Bean、可刷新的脚本Bean等，更多的支持请见[动态语言支持](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language)。

<!-- tabs:end -->


## **3. Dynamic Language Support** 

<!-- tabs:start -->

#### ** English **

Spring provides comprehensive support for using classes and objects that have been defined by using a dynamic language (such as Groovy) with Spring. This support lets you write any number of classes in a supported dynamic language and have the Spring container transparently instantiate, configure, and dependency inject the resulting objects.
#### ** Chinese **

Spring为使用动态语言（如Groovy）定义的类和对象提供了全面的支持。通过这种支持，您可以在支持的动态语言中编写任意数量的类，并让Spring容器透明地实例化、配置和依赖注入所产生的对象。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Spring’s scripting support primarily targets Groovy and BeanShell. Beyond those specifically supported languages, the JSR-223 scripting mechanism is supported for integration with any JSR-223 capable language provider (as of Spring 4.2), e.g. JRuby.
#### ** Chinese **

Spring 的脚本支持主要针对 Groovy 和 BeanShell。除了这些特定支持的语言之外，JSR-223脚本机制还支持与任何支持JSR-223的语言提供者（从Spring 4.2开始）集成，例如JRuby。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You can find fully working examples of where this dynamic language support can be immediately useful in [Scenarios](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios).
#### ** Chinese **

你可以在[场景](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios)中找到完全可行的例子，说明这种动态语言支持在哪里可以立即派上用场。

<!-- tabs:end -->


### **3.1. A First Example** 

<!-- tabs:start -->

#### ** English **

The bulk of this chapter is concerned with describing the dynamic language support in detail. Before diving into all of the ins and outs of the dynamic language support, we look at a quick example of a bean defined in a dynamic language. The dynamic language for this first bean is Groovy. (The basis of this example was taken from the Spring test suite. If you want to see equivalent examples in any of the other supported languages, take a look at the source code).
#### ** Chinese **

本章的主要内容是详细描述动态语言支持。在深入了解动态语言支持的所有来龙去脉之前，我们先看一个用动态语言定义的bean的快速例子。这个第一个Bean的动态语言是Groovy。这个例子的基础来自于Spring测试套件。如果你想看任何其他支持的语言的等效例子，请看一下源代码）。)

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The next example shows the `Messenger` interface, which the Groovy bean is going to implement. Note that this interface is defined in plain Java. Dependent objects that are injected with a reference to the `Messenger` do not know that the underlying implementation is a Groovy script. The following listing shows the `Messenger` interface:
#### ** Chinese **

下面的例子显示了Groovy bean要实现的`Messenger`接口。请注意，这个接口是用纯Java定义的。被注入引用`Messenger`的依赖对象并不知道底层实现是Groovy脚本。下面的列表显示了`Messenger`接口。

<!-- tabs:end -->


```java
package org.springframework.scripting;

public interface Messenger {

    String getMessage();
}
```

<!-- tabs:start -->

#### ** English **

The following example defines a class that has a dependency on the `Messenger` interface:
#### ** Chinese **

下面的示例定义了一个依赖`Messenger`接口的类。

<!-- tabs:end -->


```java
package org.springframework.scripting;

public class DefaultBookingService implements BookingService {

    private Messenger messenger;

    public void setMessenger(Messenger messenger) {
        this.messenger = messenger;
    }

    public void processBooking() {
        // use the injected Messenger object...
    }
}
```

<!-- tabs:start -->

#### ** English **

The following example implements the `Messenger` interface in Groovy:
#### ** Chinese **

下面的例子实现了Groovy中的`Messenger`接口。

<!-- tabs:end -->


```groovy
// from the file 'Messenger.groovy'
package org.springframework.scripting.groovy;

// import the Messenger interface (written in Java) that is to be implemented
import org.springframework.scripting.Messenger

// define the implementation in Groovy
class GroovyMessenger implements Messenger {

    String message
}
```

<!-- tabs:start -->

#### ** English **

To use the custom dynamic language tags to define dynamic-language-backed beans, you need to have the XML Schema preamble at the top of your Spring XML configuration file. You also need to use a Spring `ApplicationContext` implementation as your IoC container. Using the dynamic-language-backed beans with a plain `BeanFactory` implementation is supported, but you have to manage the plumbing of the Spring internals to do so.
#### ** Chinese **

要使用自定义动态语言标记来定义动态语言支持的Bean，您需要在Spring XML配置文件的顶部有XML Schema前言。您还需要使用 Spring `ApplicationContext` 实现作为 IoC 容器。支持使用动态语言支持的BeanFactory</x>BeanFactory</x>实现的动态语言支持的Bean，但你必须管理Spring内部的管道。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

For more information on schema-based configuration, see [XML Schema-based Configuration](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/appendix.html#xsd-configuration).
#### ** Chinese **

有关基于模式的配置的更多信息，请参阅[基于XML模式的配置](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/appendix.html#xsd-configuration)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Finally, the following example shows the bean definitions that effect the injection of the Groovy-defined `Messenger` implementation into an instance of the `DefaultBookingService` class:
#### ** Chinese **

最后，下面的例子显示了将Groovy定义的`Messenger`实现注入到`DefaultBookingService`类的实例中的Bean定义。

<!-- tabs:end -->


```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:lang="http://www.springframework.org/schema/lang"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans https://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/lang https://www.springframework.org/schema/lang/spring-lang.xsd">

    <!-- this is the bean definition for the Groovy-backed Messenger implementation -->
    <lang:groovy id="messenger" script-source="classpath:Messenger.groovy">
        <lang:property name="message" value="I Can Do The Frug" />
    </lang:groovy>

    <!-- an otherwise normal bean that will be injected by the Groovy-backed Messenger -->
    <bean id="bookingService" class="x.y.DefaultBookingService">
        <property name="messenger" ref="messenger" />
    </bean>

</beans>
```

<!-- tabs:start -->

#### ** English **

The `bookingService` bean (a `DefaultBookingService`) can now use its private `messenger` member variable as normal, because the `Messenger` instance that was injected into it is a `Messenger` instance. There is nothing special going on here — just plain Java and plain Groovy.
#### ** Chinese **

`bookingService` bean (a `DefaultBookingService`) 现在可以像正常情况下使用它的私有`messenger`成员变量，因为被注入的`Messenger`实例是一个`Messenger`实例。这里没有什么特别的地方--只是普通的Java和普通的Groovy。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Hopefully, the preceding XML snippet is self-explanatory, but do not worry unduly if it is not. Keep reading for the in-depth detail on the whys and wherefores of the preceding configuration.
#### ** Chinese **

希望前面的XML片段是不言自明的，但如果不是，也不要过分担心。请继续阅读，了解前面的配置的原因和细节。

<!-- tabs:end -->


### **3.2. Defining Beans that Are Backed by Dynamic Languages** 

<!-- tabs:start -->

#### ** English **

This section describes exactly how you define Spring-managed beans in any of the supported dynamic languages.
#### ** Chinese **

本节具体介绍了如何在任何支持的动态语言中定义Spring管理的Bean。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Note that this chapter does not attempt to explain the syntax and idioms of the supported dynamic languages. For example, if you want to use Groovy to write certain of the classes in your application, we assume that you already know Groovy. If you need further details about the dynamic languages themselves, see [Further Resources](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-resources) at the end of this chapter.
#### ** Chinese **

请注意，本章并不试图解释所支持的动态语言的语法和成语。例如，如果你想用Groovy来编写你的应用程序中的某些类，我们假设你已经知道Groovy。如果你需要更多关于动态语言本身的细节，请参阅本章末尾的[更多资源](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-resources)。

<!-- tabs:end -->


### **3.2.1. Common Concepts** 

<!-- tabs:start -->

#### ** English **

The steps involved in using dynamic-language-backed beans are as follows:
#### ** Chinese **

使用动态语言支持的豆子的步骤如下。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Write the test for the dynamic language source code (naturally).Then write the dynamic language source code itself.Define your dynamic-language-backed beans by using the appropriate `<lang:language/>` element in the XML configuration (you can define such beans programmatically by using the Spring API, although you will have to consult the source code for directions on how to do this, as this chapter does not cover this type of advanced configuration). Note that this is an iterative step. You need at least one bean definition for each dynamic language source file (although multiple bean definitions can reference the same dynamic language source file).
#### ** Chinese **

编写动态语言源码的测试（自然地）.然后编写动态语言源码本身.在XML配置中使用适当的`<lang:lang:language/>`元素来定义动态语言支持的Bean（你可以通过使用Spring API来编程定义这样的Bean，不过你必须参考源代码来了解如何做，因为本章不涉及这种类型的高级配置）。注意，这是一个迭代的步骤。每个动态语言源文件至少需要一个Bean定义（尽管多个Bean定义可以引用同一个动态语言源文件）。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The first two steps (testing and writing your dynamic language source files) are beyond the scope of this chapter. See the language specification and reference manual for your chosen dynamic language and crack on with developing your dynamic language source files. You first want to read the rest of this chapter, though, as Spring’s dynamic language support does make some (small) assumptions about the contents of your dynamic language source files.
#### ** Chinese **

前两个步骤（测试和编写动态语言源文件）不在本章的范围内。请参阅你所选择的动态语言的语言规范和参考手册，然后继续开发你的动态语言源文件。不过，你首先要阅读本章的其余部分，因为Spring的动态语言支持确实对动态语言源文件的内容做了一些（小的）假设。

<!-- tabs:end -->


### **The <lang:language/> element** 

<!-- tabs:start -->

#### ** English **

The final step in the list in the [preceding section](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-beans-concepts) involves defining dynamic-language-backed bean definitions, one for each bean that you want to configure (this is no different from normal JavaBean configuration). However, instead of specifying the fully qualified classname of the class that is to be instantiated and configured by the container, you can use the `<lang:language/>` element to define the dynamic language-backed bean.
#### ** Chinese **

在[上一节](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-beans-concepts)的列表中的最后一步涉及到定义动态语言支持的bean定义，每个要配置的bean都有一个（这与普通的JavaBean配置没有什么不同）。但是，您可以使用 `<lang:lang:language/>` 元素来定义动态语言支持的bean，而不是指定要被容器实例化和配置的类的完全限定的类名，而是使用 `<lang:lang:language/>` 元素来定义动态语言支持的bean。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Each of the supported languages has a corresponding `<lang:language/>` element:
#### ** Chinese **

每个支持的语言都有一个相应的`<lang:language/>`元素。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- `<lang:groovy/>` (Groovy)

- `<lang:bsh/>` (BeanShell)

- `<lang:std/>` (JSR-223, e.g. with JRuby)

#### ** Chinese **

- `<lang:groovy/>` (Groovy)

- `<lang:bsh/>` (BeanShell)

- `<lang:std/>` (JSR-223，例如与JRuby一起使用的JSR-223)


<!-- tabs:end -->

<!-- tabs:start -->

#### ** English **

The exact attributes and child elements that are available for configuration depends on exactly which language the bean has been defined in (the language-specific sections later in this chapter detail this).
#### ** Chinese **

可用于配置的确切属性和子元素取决于Bean是用哪种语言定义的（本章后面的特定语言部分会详细介绍）。

<!-- tabs:end -->


### **Refreshable Beans** 

<!-- tabs:start -->

#### ** English **

One of the (and perhaps the single) most compelling value adds of the dynamic language support in Spring is the “refreshable bean” feature.
#### ** Chinese **

Spring中动态语言支持的一个（也可能是唯一的）最引人注目的增值功能是 "可刷新豆 "功能。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

A refreshable bean is a dynamic-language-backed bean. With a small amount of configuration, a dynamic-language-backed bean can monitor changes in its underlying source file resource and then reload itself when the dynamic language source file is changed (for example, when you edit and save changes to the file on the file system).
#### ** Chinese **

可刷新Bean是一个动态语言支持的Bean。通过少量的配置，一个动态语言支持的Bean可以监控其底层源文件资源的变化，然后在动态语言源文件发生变化时（例如，当你编辑和保存文件系统上的文件变化时），就可以重新加载自己。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

This lets you deploy any number of dynamic language source files as part of an application, configure the Spring container to create beans backed by dynamic language source files (using the mechanisms described in this chapter), and (later, as requirements change or some other external factor comes into play) edit a dynamic language source file and have any change they make be reflected in the bean that is backed by the changed dynamic language source file. There is no need to shut down a running application (or redeploy in the case of a web application). The dynamic-language-backed bean so amended picks up the new state and logic from the changed dynamic language source file.
#### ** Chinese **

这使得您可以将任意数量的动态语言源文件作为应用程序的一部分进行部署，配置Spring容器以创建由动态语言源文件支持的Bean（使用本章中描述的机制），然后（以后，当需求发生变化或其他外部因素发生变化时）编辑一个动态语言源文件，并将它们所做的任何变化反映到由已更改的动态语言源文件支持的Bean中。无需关闭运行中的应用程序（如果是web应用程序，则无需重新部署）。这样修改后的动态语言支持的Bean会从更改后的动态语言源文件中获取新的状态和逻辑。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

This feature is off by default.
#### ** Chinese **

此功能默认是关闭的。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Now we can take a look at an example to see how easy it is to start using refreshable beans. To turn on the refreshable beans feature, you have to specify exactly one additional attribute on the `<lang:language/>` element of your bean definition. So, if we stick with [the example](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-a-first-example) from earlier in this chapter, the following example shows what we would change in the Spring XML configuration to effect refreshable beans:
#### ** Chinese **

现在我们可以看一个例子，看看要开始使用可刷新Bean有多容易。要开启可刷新Bean功能，你必须在Bean定义的`<lang:language/>`元素中指定一个额外的属性。因此，如果我们坚持使用本章前面的[例子](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-a-first-example)，下面的例子显示了我们要在Spring XML配置中改变什么来启用可刷新Bean。

<!-- tabs:end -->


```xml
<beans>

    <!-- this bean is now 'refreshable' due to the presence of the 'refresh-check-delay' attribute -->
    <lang:groovy id="messenger"
            refresh-check-delay="5000" <!-- switches refreshing on with 5 seconds between checks -->
            script-source="classpath:Messenger.groovy">
        <lang:property name="message" value="I Can Do The Frug" />
    </lang:groovy>

    <bean id="bookingService" class="x.y.DefaultBookingService">
        <property name="messenger" ref="messenger" />
    </bean>

</beans>
```

<!-- tabs:start -->

#### ** English **

That really is all you have to do. The `refresh-check-delay` attribute defined on the `messenger` bean definition is the number of milliseconds after which the bean is refreshed with any changes made to the underlying dynamic language source file. You can turn off the refresh behavior by assigning a negative value to the `refresh-check-delay` attribute. Remember that, by default, the refresh behavior is disabled. If you do not want the refresh behavior, do not define the attribute.
#### ** Chinese **

这真的是你所要做的一切。`refresh-check-delay`属性定义在`messenger` bean的定义中，它是指在对底层动态语言源文件进行任何更改后，Bean被刷新的毫秒数。你可以通过给`refresh-check-delay`属性指定一个负值来关闭刷新行为。记住，默认情况下，刷新行为是被禁用的。如果您不想要刷新行为，请不要定义该属性。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If we then run the following application, we can exercise the refreshable feature. (Please excuse the “jumping-through-hoops-to-pause-the-execution” shenanigans in this next slice of code.) The `System.in.read()` call is only there so that the execution of the program pauses while you (the developer in this scenario) go off and edit the underlying dynamic language source file so that the refresh triggers on the dynamic-language-backed bean when the program resumes execution.
#### ** Chinese **

如果我们随后运行下面的应用程序，我们就可以行使刷新功能。(请原谅下面这段代码中的 "跳过圈圈到暂停执行 "的诡计。) `System.in.read()`调用只是为了让程序的执行暂停，而你（这个场景中的开发者）去编辑底层动态语言源文件，这样当程序恢复执行时，刷新就会在动态语言支持的Bean上触发。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The following listing shows this sample application:
#### ** Chinese **

下面列举的是这个申请样本。

<!-- tabs:end -->


```java
import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;
import org.springframework.scripting.Messenger;

public final class Boot {

    public static void main(final String[] args) throws Exception {
        ApplicationContext ctx = new ClassPathXmlApplicationContext("beans.xml");
        Messenger messenger = (Messenger) ctx.getBean("messenger");
        System.out.println(messenger.getMessage());
        // pause execution while I go off and make changes to the source file...
        System.in.read();
        System.out.println(messenger.getMessage());
    }
}
```

<!-- tabs:start -->

#### ** English **

Assume then, for the purposes of this example, that all calls to the `getMessage()` method of `Messenger` implementations have to be changed such that the message is surrounded by quotation marks. The following listing shows the changes that you (the developer) should make to the `Messenger.groovy` source file when the execution of the program is paused:
#### ** Chinese **

在这个例子中，假设所有对 `Messenger`实现的`getMessage()`方法的调用都必须进行修改，使消息被引号包围。下面列出了当程序暂停执行时，您（开发人员）应该对 `Messenger.groovy`源文件进行的修改。

<!-- tabs:end -->


```groovy
package org.springframework.scripting

class GroovyMessenger implements Messenger {

    private String message = "Bingo"

    public String getMessage() {
        // change the implementation to surround the message in quotes
        return "'" + this.message + "'"
    }

    public void setMessage(String message) {
        this.message = message
    }
}
```

<!-- tabs:start -->

#### ** English **

When the program runs, the output before the input pause will be `I Can Do The Frug`. After the change to the source file is made and saved and the program resumes execution, the result of calling the `getMessage()` method on the dynamic-language-backed `Messenger` implementation is `'I Can Do The Frug'` (notice the inclusion of the additional quotation marks).
#### ** Chinese **

程序运行时，输入暂停前的输出将是`I Can Do The Frug`。在对源文件进行了更改并保存后，程序恢复执行，在动态语言支持的`Messenger`实现上调用`getMessage()`方法的结果是`'I Can Do The Frug'`（注意，额外的引号被包含了）。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Changes to a script do not trigger a refresh if the changes occur within the window of the `refresh-check-delay` value. Changes to the script are not actually picked up until a method is called on the dynamic-language-backed bean. It is only when a method is called on a dynamic-language-backed bean that it checks to see if its underlying script source has changed. Any exceptions that relate to refreshing the script (such as encountering a compilation error or finding that the script file has been deleted) results in a fatal exception being propagated to the calling code.
#### ** Chinese **

如果在`refresh-check-delay`值的窗口内发生变化，那么对脚本的更改不会触发刷新。在动态语言支持的Bean上的方法被调用之前，对脚本的更改不会被实际接收。只有当一个方法被调用到动态语言支持的Bean上时，才会检查它的底层脚本源是否发生了变化。任何与刷新脚本有关的异常（如遇到编译错误或发现脚本文件被删除）都会导致一个致命的异常被传播到调用代码中。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The refreshable bean behavior described earlier does not apply to dynamic language source files defined with the `<lang:inline-script/>` element notation (see [Inline Dynamic Language Source Files](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-beans-inline)). Additionally, it applies only to beans where changes to the underlying source file can actually be detected (for example, by code that checks the last modified date of a dynamic language source file that exists on the file system).
#### ** Chinese **

前面描述的可刷新Bean行为不适用于用`<lang:inline-script/>`元素符号定义的动态语言源文件（参见[inline动态语言源文件](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-beans-inline)）。此外，它只适用于可以检测到底层源文件的变化的bean（例如，通过检查文件系统中存在的动态语言源文件的最后修改日期的代码）。

<!-- tabs:end -->


### **Inline Dynamic Language Source Files** 

<!-- tabs:start -->

#### ** English **

The dynamic language support can also cater to dynamic language source files that are embedded directly in Spring bean definitions. More specifically, the `<lang:inline-script/>` element lets you define dynamic language source immediately inside a Spring configuration file. An example might clarify how the inline script feature works:
#### ** Chinese **

动态语言支持还可以满足直接嵌入到Spring Bean定义中的动态语言源文件。更具体地说，`<lang:inline-script/>`元素可以让您在Spring配置文件中立即定义动态语言源。一个例子可以说明内联脚本功能的工作原理。

<!-- tabs:end -->


```xml
<lang:groovy id="messenger">
    <lang:inline-script>

package org.springframework.scripting.groovy;

import org.springframework.scripting.Messenger

class GroovyMessenger implements Messenger {
    String message
}

    </lang:inline-script>
    <lang:property name="message" value="I Can Do The Frug" />
</lang:groovy>
```

<!-- tabs:start -->

#### ** English **

If we put to one side the issues surrounding whether it is good practice to define dynamic language source inside a Spring configuration file, the `<lang:inline-script/>` element can be useful in some scenarios. For instance, we might want to quickly add a Spring `Validator` implementation to a Spring MVC `Controller`. This is but a moment’s work using inline source. (See [Scripted Validators](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios-validators) for such an example.)
#### ** Chinese **

如果我们把围绕着在Spring配置文件中定义动态语言源是否是一个好的做法的问题放在一边，那么`<lang:line-script/>`元素在某些场景中可能是有用的。例如，我们可能想快速添加一个Spring `Validator`实现到Spring MVC `Controller`中。这不过是使用内联源码的片刻之功。(参见[Scripted Validators](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios-validators)的例子。)

<!-- tabs:end -->


### **Understanding Constructor Injection in the Context of Dynamic-language-backed Beans** 

<!-- tabs:start -->

#### ** English **

There is one very important thing to be aware of with regard to Spring’s dynamic language support. Namely, you can not (currently) supply constructor arguments to dynamic-language-backed beans (and, hence, constructor-injection is not available for dynamic-language-backed beans). In the interests of making this special handling of constructors and properties 100% clear, the following mixture of code and configuration does not work:
#### ** Chinese **

关于Spring的动态语言支持，有一件非常重要的事情需要注意。也就是说，你不能（目前）向动态语言支持的Bean提供构造函数参数（因此，构造注入不能用于动态语言支持的Bean）。为了让这种对构造函数和属性的特殊处理100%的明确，下面的代码和配置混合在一起就不能使用。

<!-- tabs:end -->


```groovy
// from the file 'Messenger.groovy'
package org.springframework.scripting.groovy;

import org.springframework.scripting.Messenger

class GroovyMessenger implements Messenger {

    GroovyMessenger() {}

    // this constructor is not available for Constructor Injection
    GroovyMessenger(String message) {
        this.message = message;
    }

    String message

    String anotherMessage
}
```

```xml
<lang:groovy id="badMessenger"
    script-source="classpath:Messenger.groovy">
    <!-- this next constructor argument will not be injected into the GroovyMessenger -->
    <!-- in fact, this isn't even allowed according to the schema -->
    <constructor-arg value="This will not work" />

    <!-- only property values are injected into the dynamic-language-backed object -->
    <lang:property name="anotherMessage" value="Passed straight through to the dynamic-language-backed object" />

</lang>
```

<!-- tabs:start -->

#### ** English **

In practice this limitation is not as significant as it first appears, since setter injection is the injection style favored by the overwhelming majority of developers (we leave the discussion as to whether that is a good thing to another day).
#### ** Chinese **

在实践中，这个限制并不像最初看起来那么重要，因为绝大多数的开发者都喜欢使用setter注入式的注入方式（至于这是否是一件好事，我们把讨论留待日后再谈）。

<!-- tabs:end -->


### **3.2.2. Groovy Beans** 

<!-- tabs:start -->

#### ** English **

This section describes how to use beans defined in Groovy in Spring.
#### ** Chinese **

本节介绍如何在Spring中使用Groovy中定义的豆子。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The Groovy homepage includes the following description:
#### ** Chinese **

Groovy主页包括以下描述。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

“Groovy is an agile dynamic language for the Java 2 Platform that has many of the features that people like so much in languages like Python, Ruby and Smalltalk, making them available to Java developers using a Java-like syntax.”
#### ** Chinese **

"Groovy是一种用于Java 2平台的敏捷动态语言，它拥有Python、Ruby和Smalltalk等语言中人们非常喜欢的许多特性，使Java开发人员可以使用类似Java的语法来实现这些特性。"

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

If you have read this chapter straight from the top, you have already [seen an example](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-a-first-example) of a Groovy-dynamic-language-backed bean. Now consider another example (again using an example from the Spring test suite):
#### ** Chinese **

如果你直接读了这一章，你已经[看到了一个Groovy-dynamic-language-backed bean的例子](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-a-first-example)。现在考虑另一个例子（同样使用Spring测试套件中的一个例子）。

<!-- tabs:end -->


```java
package org.springframework.scripting;

public interface Calculator {

    int add(int x, int y);
}
```

<!-- tabs:start -->

#### ** English **

The following example implements the `Calculator` interface in Groovy:
#### ** Chinese **

下面的例子实现了Groovy中的`Calculator`接口。

<!-- tabs:end -->


```groovy
// from the file 'calculator.groovy'
package org.springframework.scripting.groovy

class GroovyCalculator implements Calculator {

    int add(int x, int y) {
        x + y
    }
}
```

<!-- tabs:start -->

#### ** English **

The following bean definition uses the calculator defined in Groovy:
#### ** Chinese **

下面的Bean定义使用Groovy中定义的计算器。

<!-- tabs:end -->


```
<-- from the file 'beans.xml' -->
<beans>
    <lang:groovy id="calculator" script-source="classpath:calculator.groovy"/>
</beans>
```

<!-- tabs:start -->

#### ** English **

Finally, the following small application exercises the preceding configuration:
#### ** Chinese **

最后，下面小编就来练习一下前面的配置。

<!-- tabs:end -->


```java
package org.springframework.scripting;

import org.springframework.context.ApplicationContext;
import org.springframework.context.support.ClassPathXmlApplicationContext;

public class Main {

    public static void Main(String[] args) {
        ApplicationContext ctx = new ClassPathXmlApplicationContext("beans.xml");
        Calculator calc = (Calculator) ctx.getBean("calculator");
        System.out.println(calc.add(2, 8));
    }
}
```

<!-- tabs:start -->

#### ** English **

The resulting output from running the above program is (unsurprisingly) `10`. (For more interesting examples, see the dynamic language showcase project for a more complex example or see the examples [Scenarios](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios) later in this chapter).
#### ** Chinese **

运行上述程序的结果是（毫不意外地）`10`。(更多有趣的例子，请看动态语言展示项目中的动态语言展示项目，以了解更复杂的例子，或者参见本章后面的例子[场景](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios))。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You must not define more than one class per Groovy source file. While this is perfectly legal in Groovy, it is (arguably) a bad practice. In the interests of a consistent approach, you should (in the opinion of the Spring team) respect the standard Java conventions of one (public) class per source file.
#### ** Chinese **

每个Groovy源文件中不能定义一个以上的类。虽然这在Groovy中是完全合法的，但这是（可以说）一种不好的做法。为了保持一致，你应该（在Spring团队看来）尊重标准的Java惯例，即每个源文件只定义一个（公共）类。

<!-- tabs:end -->


### **Customizing Groovy Objects by Using a Callback** 

<!-- tabs:start -->

#### ** English **

The `GroovyObjectCustomizer` interface is a callback that lets you hook additional creation logic into the process of creating a Groovy-backed bean. For example, implementations of this interface could invoke any required initialization methods, set some default property values, or specify a custom `MetaClass`. The following listing shows the `GroovyObjectCustomizer` interface definition:
#### ** Chinese **

`GroovyObjectCustomizer`接口是一个回调，它可以让你在创建Groovy支持的Bean的过程中加入额外的创建逻辑。例如，这个接口的实现可以调用任何必要的初始化方法，设置一些默认的属性值，或者指定一个自定义的`MetaClass`。下面的列表显示了`GroovyObjectCustomizer`接口的定义。

<!-- tabs:end -->


```java
public interface GroovyObjectCustomizer {

    void customize(GroovyObject goo);
}
```

<!-- tabs:start -->

#### ** English **

The Spring Framework instantiates an instance of your Groovy-backed bean and then passes the created `GroovyObject` to the specified `GroovyObjectCustomizer` (if one has been defined). You can do whatever you like with the supplied `GroovyObject` reference. We expect that most people want to set a custom `MetaClass` with this callback, and the following example shows how to do so:
#### ** Chinese **

Spring Framework 会实例化一个由 Groovy 支持的 Bean 实例，然后将创建的 `GroovyObject` 传递给指定的 `GroovyObjectCustomizer`（如果已经定义了的话）。你可以对提供的`GroovyObject`引用做任何你喜欢的事情。我们预计大多数人都希望通过这个回调设置一个自定义的`MetaClass`，下面的例子显示了如何做到这一点。

<!-- tabs:end -->


```java
public final class SimpleMethodTracingCustomizer implements GroovyObjectCustomizer {

    public void customize(GroovyObject goo) {
        DelegatingMetaClass metaClass = new DelegatingMetaClass(goo.getMetaClass()) {

            public Object invokeMethod(Object object, String methodName, Object[] arguments) {
                System.out.println("Invoking '" + methodName + "'.");
                return super.invokeMethod(object, methodName, arguments);
            }
        };
        metaClass.initialize();
        goo.setMetaClass(metaClass);
    }

}
```

<!-- tabs:start -->

#### ** English **

A full discussion of meta-programming in Groovy is beyond the scope of the Spring reference manual. See the relevant section of the Groovy reference manual or do a search online. Plenty of articles address this topic. Actually, making use of a `GroovyObjectCustomizer` is easy if you use the Spring namespace support, as the following example shows:
#### ** Chinese **

关于Groovy中元编程的完整讨论超出了Spring参考手册的范围。请参阅Groovy参考手册的相关章节，或者在网上进行搜索。有很多文章都在讨论这个话题。实际上，如果你使用Spring命名空间支持，使用`GroovyObjectCustomizer`是很容易的，就像下面的例子所示。

<!-- tabs:end -->


```xml
<!-- define the GroovyObjectCustomizer just like any other bean -->
<bean id="tracingCustomizer" class="example.SimpleMethodTracingCustomizer"/>

    <!-- ... and plug it into the desired Groovy bean via the 'customizer-ref' attribute -->
    <lang:groovy id="calculator"
        script-source="classpath:org/springframework/scripting/groovy/Calculator.groovy"
        customizer-ref="tracingCustomizer"/>
```

<!-- tabs:start -->

#### ** English **

If you do not use the Spring namespace support, you can still use the `GroovyObjectCustomizer` functionality, as the following example shows:
#### ** Chinese **

如果你不使用Spring命名空间支持，你仍然可以使用`GroovyObjectCustomizer`功能，如下例所示。

<!-- tabs:end -->


```xml
<bean id="calculator" class="org.springframework.scripting.groovy.GroovyScriptFactory">
    <constructor-arg value="classpath:org/springframework/scripting/groovy/Calculator.groovy"/>
    <!-- define the GroovyObjectCustomizer (as an inner bean) -->
    <constructor-arg>
        <bean id="tracingCustomizer" class="example.SimpleMethodTracingCustomizer"/>
    </constructor-arg>
</bean>

<bean class="org.springframework.scripting.support.ScriptFactoryPostProcessor"/>
```

<!-- tabs:start -->

#### ** English **

As of Spring Framework 4.3.3, you may also specify a Groovy `CompilationCustomizer` (such as an `ImportCustomizer`) or even a full Groovy `CompilerConfiguration` object in the same place as Spring’s `GroovyObjectCustomizer`.
#### ** Chinese **

从Spring Framework 4.3.3.3开始，您还可以指定一个Groovy `CompilationCustomizer`（如`ImportCustomizer`），甚至可以指定一个完整的Groovy `CompilerConfiguration`对象，在与Spring的`GroovyObjectCustomizer`相同的地方。

<!-- tabs:end -->


### **3.2.3. BeanShell Beans** 

<!-- tabs:start -->

#### ** English **

This section describes how to use BeanShell beans in Spring.
#### ** Chinese **

本节介绍如何在Spring中使用BeanShell豆子。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The [BeanShell homepage](https://beanshell.github.io/intro.html) includes the following description:
#### ** Chinese **

BeanShell主页](https://beanshell.github.io/intro.html)包括以下描述。

<!-- tabs:end -->


```
BeanShell is a small, free, embeddable Java source interpreter with dynamic language
features, written in Java. BeanShell dynamically executes standard Java syntax and
extends it with common scripting conveniences such as loose types, commands, and method
closures like those in Perl and JavaScript.
```

<!-- tabs:start -->

#### ** English **

In contrast to Groovy, BeanShell-backed bean definitions require some (small) additional configuration. The implementation of the BeanShell dynamic language support in Spring is interesting, because Spring creates a JDK dynamic proxy that implements all of the interfaces that are specified in the `script-interfaces` attribute value of the `<lang:bsh>` element (this is why you must supply at least one interface in the value of the attribute, and, consequently, program to interfaces when you use BeanShell-backed beans). This means that every method call on a BeanShell-backed object goes through the JDK dynamic proxy invocation mechanism.
#### ** Chinese **

与Groovy相比，BeanShell支持的Bean定义需要一些（小的）额外配置。BeanShell动态语言支持在Spring中的实现很有意思，因为Spring创建了一个JDK动态代理，它实现了`script-interfaces`元素的`<lang:bsh>`属性值中指定的所有接口（这就是为什么当你使用BeanShell支持的BeanShell的Bean时，你必须在属性值中至少提供一个接口，因此，当你使用BeanShell支持的Bean时，你必须提供一个接口，从而使程序向接口转化）。这意味着BeanShell支持的对象上的每个方法调用都要经过JDK的动态代理调用机制。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Now we can show a fully working example of using a BeanShell-based bean that implements the `Messenger` interface that was defined earlier in this chapter. We again show the definition of the `Messenger` interface:
#### ** Chinese **

现在我们可以展示一个基于BeanShell的Bean的工作示例，它实现了本章前面定义的`Messenger`接口。我们再次展示`Messenger`接口的定义。

<!-- tabs:end -->


```java
package org.springframework.scripting;

public interface Messenger {

    String getMessage();
}
```

<!-- tabs:start -->

#### ** English **

The following example shows the BeanShell “implementation” (we use the term loosely here) of the `Messenger` interface:
#### ** Chinese **

下面的例子展示了BeanShell的`Messenger`接口的 "实现"（我们在这里松散地使用这个术语）。

<!-- tabs:end -->


```java
String message;

String getMessage() {
    return message;
}

void setMessage(String aMessage) {
    message = aMessage;
}
```

<!-- tabs:start -->

#### ** English **

The following example shows the Spring XML that defines an “instance” of the above “class” (again, we use these terms very loosely here):
#### ** Chinese **

下面的例子是定义了上述 "类 "的 "实例 "的Spring XML(这里再来一次，我们把这些术语用得很松散)。

<!-- tabs:end -->


```xml
<lang:bsh id="messageService" script-source="classpath:BshMessenger.bsh"
    script-interfaces="org.springframework.scripting.Messenger">

    <lang:property name="message" value="Hello World!" />
</lang:bsh>
```

<!-- tabs:start -->

#### ** English **

See [Scenarios](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios) for some scenarios where you might want to use BeanShell-based beans.
#### ** Chinese **

请参阅[场景](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-scenarios)，了解一些你可能想使用基于BeanShell的BeanShell豆的场景。

<!-- tabs:end -->


### **3.3. Scenarios** 

<!-- tabs:start -->

#### ** English **

The possible scenarios where defining Spring managed beans in a scripting language would be beneficial are many and varied. This section describes two possible use cases for the dynamic language support in Spring.
#### ** Chinese **

在脚本语言中定义Spring管理的Bean会有很多可能的应用场景。本节介绍了Spring中动态语言支持的两个可能的用例。

<!-- tabs:end -->


### **3.3.1. Scripted Spring MVC Controllers** 

<!-- tabs:start -->

#### ** English **

One group of classes that can benefit from using dynamic-language-backed beans is that of Spring MVC controllers. In pure Spring MVC applications, the navigational flow through a web application is, to a large extent, determined by code encapsulated within your Spring MVC controllers. As the navigational flow and other presentation layer logic of a web application needs to be updated to respond to support issues or changing business requirements, it may well be easier to effect any such required changes by editing one or more dynamic language source files and seeing those changes being immediately reflected in the state of a running application.
#### ** Chinese **

有一组类可以从使用动态语言支持的Bean中受益，那就是Spring MVC控制器。在纯Spring MVC应用中，Web应用的导航流在很大程度上是由封装在Spring MVC控制器中的代码决定的。由于Web应用程序的导航流和其他表现层逻辑需要更新以响应支持问题或业务需求的变化，通过编辑一个或多个动态语言源文件，并看到这些变化立即反映在运行中的应用程序的状态中，可能会更容易实现任何此类所需的变化。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Remember that, in the lightweight architectural model espoused by projects such as Spring, you typically aim to have a really thin presentation layer, with all the meaty business logic of an application being contained in the domain and service layer classes. Developing Spring MVC controllers as dynamic-language-backed beans lets you change presentation layer logic by editing and saving text files. Any changes to such dynamic language source files is (depending on the configuration) automatically reflected in the beans that are backed by dynamic language source files.
#### ** Chinese **

请记住，在Spring等项目所倡导的轻量级架构模型中，你的目标通常是建立一个非常薄的展现层，而应用程序的所有业务逻辑都包含在域和服务层类中。将Spring MVC控制器开发成动态语言支持的Bean，可以让你通过编辑和保存文本文件来改变展现层逻辑。对这种动态语言源文件的任何更改都会自动反映在动态语言源文件支持的Bean中（取决于配置）。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To effect this automatic “pickup” of any changes to dynamic-language-backed beans, you have to enable the “refreshable beans” functionality. See [Refreshable Beans](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-refreshable-beans) for a full treatment of this feature.
#### ** Chinese **

要实现动态语言支持的Bean的任何变化的自动 "拾取"，你必须启用 "可刷新Bean "功能。关于这个功能的完整处理方法，请参阅[刷新豆子](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-refreshable-beans)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The following example shows an `org.springframework.web.servlet.mvc.Controller` implemented by using the Groovy dynamic language:
#### ** Chinese **

下面的示例显示了一个`org.springframework.web.servlet.mvc.Controller`，使用Groovy动态语言实现的<x>。

<!-- tabs:end -->


```groovy
// from the file '/WEB-INF/groovy/FortuneController.groovy'
package org.springframework.showcase.fortune.web

import org.springframework.showcase.fortune.service.FortuneService
import org.springframework.showcase.fortune.domain.Fortune
import org.springframework.web.servlet.ModelAndView
import org.springframework.web.servlet.mvc.Controller

import javax.servlet.http.HttpServletRequest
import javax.servlet.http.HttpServletResponse

class FortuneController implements Controller {

    @Property FortuneService fortuneService

    ModelAndView handleRequest(HttpServletRequest request,
            HttpServletResponse httpServletResponse) {
        return new ModelAndView("tell", "fortune", this.fortuneService.tellFortune())
    }
}
```

```xml
<lang:groovy id="fortune"
        refresh-check-delay="3000"
        script-source="/WEB-INF/groovy/FortuneController.groovy">
    <lang:property name="fortuneService" ref="fortuneService"/>
</lang:groovy>
```

### **3.3.2. Scripted Validators** 

<!-- tabs:start -->

#### ** English **

Another area of application development with Spring that may benefit from the flexibility afforded by dynamic-language-backed beans is that of validation. It can be easier to express complex validation logic by using a loosely typed dynamic language (that may also have support for inline regular expressions) as opposed to regular Java.
#### ** Chinese **

使用Spring开发应用程序的另一个可能受益于动态语言支持的Bean所提供的灵活性的领域是验证。通过使用松散类型的动态语言（也可以支持内联正则表达式）来表达复杂的验证逻辑，比普通的Java更容易。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

Again, developing validators as dynamic-language-backed beans lets you change validation logic by editing and saving a simple text file. Any such changes is (depending on the configuration) automatically reflected in the execution of a running application and would not require the restart of an application.
#### ** Chinese **

同样，将验证器开发成动态语言支持的Bean，可以通过编辑和保存一个简单的文本文件来改变验证逻辑。任何这样的更改都会自动反映在运行中的应用程序的执行中（取决于配置），而不需要重新启动应用程序。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To effect the automatic “pickup” of any changes to dynamic-language-backed beans, you have to enable the 'refreshable beans' feature. See [Refreshable Beans](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-refreshable-beans) for a full and detailed treatment of this feature.
#### ** Chinese **

要实现对动态语言支持的豆子的任何变化的自动 "拾取"，你必须启用 "可刷新豆子 "功能。请参阅[刷新Bean](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/languages.html#dynamic-language-refreshable-beans)来了解这个功能的完整和详细的处理方法。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The following example shows a Spring `org.springframework.validation.Validator` implemented by using the Groovy dynamic language (see [Validation using Spring’s Validator interface](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#validator) for a discussion of the `Validator` interface):
#### ** Chinese **

下面的例子显示了一个使用Groovy动态语言实现的Spring `org.springframework.validation.Validator`（关于`Validator`接口的讨论，请参见[使用Spring的Validator接口](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#validator)）。

<!-- tabs:end -->


```java
import org.springframework.validation.Validator
import org.springframework.validation.Errors
import org.springframework.beans.TestBean

class TestBeanValidator implements Validator {

    boolean supports(Class clazz) {
        return TestBean.class.isAssignableFrom(clazz)
    }

    void validate(Object bean, Errors errors) {
        if(bean.name?.trim()?.size() > 0) {
            return
        }
        errors.reject("whitespace", "Cannot be composed wholly of whitespace.")
    }
}
```

### **3.4. Additional Details** 

<!-- tabs:start -->

#### ** English **

This last section contains some additional details related to the dynamic language support.
#### ** Chinese **

这最后一节包含了一些与动态语言支持相关的额外细节。

<!-- tabs:end -->


### **3.4.1. AOP — Advising Scripted Beans** 

<!-- tabs:start -->

#### ** English **

You can use the Spring AOP framework to advise scripted beans. The Spring AOP framework actually is unaware that a bean that is being advised might be a scripted bean, so all of the AOP use cases and functionality that you use (or aim to use) work with scripted beans. When you advise scripted beans, you cannot use class-based proxies. You must use [interface-based proxies](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#aop-proxying).
#### ** Chinese **

你可以使用Spring AOP框架来建议脚本化的Bean。实际上，Spring AOP 框架并不知道被建议的 bean 可能是一个脚本化的 bean，所以你使用的所有 AOP 用例和功能都可以使用脚本化的 bean。当你建议脚本化的Bean时，你不能使用基于类的代理。你必须使用[基于接口的代理](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#aop-proxying)。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

You are not limited to advising scripted beans. You can also write aspects themselves in a supported dynamic language and use such beans to advise other Spring beans. This really would be an advanced use of the dynamic language support though.
#### ** Chinese **

你并不限于给脚本化的Bean提供建议。你也可以用支持的动态语言编写方面，并使用这样的Bean为其他Spring Bean提供建议。这确实是对动态语言支持的高级使用。

<!-- tabs:end -->


### **3.4.2. Scoping** 

<!-- tabs:start -->

#### ** English **

In case it is not immediately obvious, scripted beans can be scoped in the same way as any other bean. The `scope` attribute on the various `<lang:language/>` elements lets you control the scope of the underlying scripted bean, as it does with a regular bean. (The default scope is [singleton](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes-singleton), as it is with “regular” beans.)
#### ** Chinese **

如果你还不清楚，脚本化的Bean可以像其他的Bean一样，以同样的方式进行scope。在各种 `<lang:lang:language/>` 元素上的 `scope` 属性可以让你控制底层脚本 Bean 的作用域，就像普通 Bean 一样。(默认的作用域是 [singleton](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes-singleton)，和 "普通 "Bean一样。)

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

The following example uses the `scope` attribute to define a Groovy bean scoped as a [prototype](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes-prototype):
#### ** Chinese **

下面的例子使用`scope`属性来定义一个Groovy Bean scope为[prototype](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes-prototype)。

<!-- tabs:end -->


```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:lang="http://www.springframework.org/schema/lang"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans https://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/lang https://www.springframework.org/schema/lang/spring-lang.xsd">

    <lang:groovy id="messenger" script-source="classpath:Messenger.groovy" scope="prototype">
        <lang:property name="message" value="I Can Do The RoboCop" />
    </lang:groovy>

    <bean id="bookingService" class="x.y.DefaultBookingService">
        <property name="messenger" ref="messenger" />
    </bean>

</beans>
```

<!-- tabs:start -->

#### ** English **

See [Bean Scopes](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes) in [The IoC Container](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans) for a full discussion of the scoping support in the Spring Framework.
#### ** Chinese **

有关Spring框架中的Scoping支持的完整讨论，请参阅[The IoC Container](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans)中的[Bean Scopes](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/core.html#beans-factory-scopes)。

<!-- tabs:end -->


### **3.4.3. The** **`lang`** ** XML schema** 

<!-- tabs:start -->

#### ** English **

The `lang` elements in Spring XML configuration deal with exposing objects that have been written in a dynamic language (such as Groovy or BeanShell) as beans in the Spring container.
#### ** Chinese **

Spring XML 配置中的 `lang` 元素处理将用动态语言（如 Groovy 或 BeanShell）编写的对象作为 beans 暴露在 Spring 容器中。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

These elements (and the dynamic language support) are comprehensively covered in [Dynamic Language Support](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/integration.html#dynamic-language). See that chapter for full details on this support and the `lang` elements.
#### ** Chinese **

这些元素（以及动态语言支持）在[动态语言支持](https://docs.spring.io/spring/docs/5.2.6.RELEASE/spring-framework-reference/integration.html#dynamic-language)中全面介绍了。有关此支持和`lang`元素的完整细节，请参见该章。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

To use the elements in the `lang` schema, you need to have the following preamble at the top of your Spring XML configuration file. The text in the following snippet references the correct schema so that the tags in the `lang` namespace are available to you:
#### ** Chinese **

要使用 `lang` 模式中的元素，您需要在 Spring XML 配置文件的顶部有以下前言。以下片段中的文本引用了正确的模式，以便您可以使用 `lang`命名空间中的标记。

<!-- tabs:end -->


```xml
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:lang="http://www.springframework.org/schema/lang"
    xsi:schemaLocation="
        http://www.springframework.org/schema/beans https://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/lang https://www.springframework.org/schema/lang/spring-lang.xsd">

    <!-- bean definitions here -->

</beans>
```

### **3.5. Further Resources** 

<!-- tabs:start -->

#### ** English **

The following links go to further resources about the various dynamic languages referenced in this chapter:
#### ** Chinese **

下面的链接是关于本章中提到的各种动态语言的进一步资源。

<!-- tabs:end -->


<!-- tabs:start -->

#### ** English **

- The [Groovy](https://www.groovy-lang.org/) homepage

- The [BeanShell](https://beanshell.github.io/intro.html) homepage

- The [JRuby](https://www.jruby.org/) homepage


#### ** Chinese **

- Groovy](https://www.groovy-lang.org/)的主页。

- BeanShell](https://beanshell.github.io/intro.html)首页

- JRuby](https://www.jruby.org/)主页


<!-- tabs:end -->

[回目录](Spring-Framework-5.2.6.RELEASE/summary.md)

[回首页](/README)
