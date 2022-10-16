# 1.The IoC Container

[原文 docs](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans)
> This chapter covers Spring’s Inversion of Control (IoC) container.

[日本語 docs](https://spring.pleiades.io/spring-framework/docs/current/reference/html/core.html#beans)
> この章では、Spring の制御の反転（IoC）コンテナーについて説明します。


# 1.1. Introduction to the Spring IoC Container and Beans （Spring IoC コンテナーと Bean の概要）

[原文 docs](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-introduction)
> This chapter covers the Spring Framework implementation of the Inversion of Control (IoC) principle. IoC is also known as dependency injection (DI). It is a process whereby objects define their dependencies (that is, the other objects they work with) only through constructor arguments, arguments to a factory method, or properties that are set on the object instance after it is constructed or returned from a factory method. The container then injects those dependencies when it creates the bean. This process is fundamentally the inverse (hence the name, Inversion of Control) of the bean itself controlling the instantiation or location of its dependencies by using direct construction of classes or a mechanism such as the Service Locator pattern.
> 
> The `org.springframework.beans` and `org.springframework.context` packages are the basis for Spring Framework’s IoC container. The `BeanFactory` interface provides an advanced configuration mechanism capable of managing any type of object. `ApplicationContext` is a sub-interface of BeanFactory. It adds:
> 
> * Easier integration with Spring’s AOP features
> * Message resource handling (for use in internationalization)
> * Event publication
> * Application-layer specific contexts such as the WebApplicationContext for use in web applications.
> 
> In short, the `BeanFactory` provides the configuration framework and basic functionality, and the `ApplicationContext` adds more enterprise-specific functionality. The `ApplicationContext` is a complete superset of the `BeanFactory` and is used exclusively in this chapter in descriptions of Spring’s IoC container. For more information on using the `BeanFactory` instead of the `ApplicationContext`, see the section covering the `BeanFactory` API.
> 
> In Spring, the objects that form the backbone of your application and that are managed by the Spring IoC container are called beans. A bean is an object that is instantiated, assembled, and managed by a Spring IoC container. Otherwise, a bean is simply one of many objects in your application. Beans, and the dependencies among them, are reflected in the configuration metadata used by a container.


[日本語 docs](https://spring.pleiades.io/spring-framework/docs/current/reference/html/core.html#beans-introduction)
> この章では、制御の反転（IoC）原則の Spring Framework 実装について説明します。IoC は、依存性注入（DI）とも呼ばれます。これは、コンストラクター引数、ファクトリメソッドへの引数、またはファクトリメソッドが構築または返された後にオブジェクトインスタンスに設定されるプロパティを通じてのみ、オブジェクトが依存関係（つまり、操作する他のオブジェクト）を定義するプロセスです。コンテナーは、Bean を作成するときにそれらの依存関係を注入します。このプロセスは、基本的に、クラスの直接構築または Service Locator パターンなどのメカニズムを使用して、Bean 自身がその依存関係のインスタンス化や場所を制御することの逆（そのため、Inversion of Control という名前）です。
> 
> `org.springframework.beans` および `org.springframework.context` パッケージは、Spring Framework の IoC コンテナーの基盤です。`BeanFactory` (Javadoc) インターフェースは、あらゆる型のオブジェクトを管理できる高度な設定メカニズムを提供します。`ApplicationContext` (Javadoc) は `BeanFactory` のサブインターフェースです。以下を追加します。
> 
> * Spring の AOP 機能との簡単な統合
> * メッセージリソースの処理 (国際化で使用するため)
> * イベント公開
> * Web アプリケーションで使用する WebApplicationContext などのアプリケーション層固有のコンテキスト。
> 
> つまり、`BeanFactory` は設定フレームワークと基本機能を提供し、`ApplicationContext` はより多くのエンタープライズ固有の機能を追加します。`ApplicationContext` は `BeanFactory` の完全なスーパーセットであり、この章で Spring の IoC コンテナーの説明でのみ使用されます。`ApplicationContext`, の代わりに `BeanFactory` を使用する方法の詳細については、`BeanFactory` API に関するセクションを参照してください。
> 
> Spring では、アプリケーションのバックボーンを形成し、Spring IoC コンテナーによって管理されるオブジェクトを Bean と呼びます。Bean は、Spring IoC コンテナーによってインスタンス化、アセンブル、管理されるオブジェクトです。それ以外の場合、Bean はアプリケーションの多くのオブジェクトの 1 つにすぎません。Bean とそれらの間の依存関係は、コンテナーが使用する設定メタデータに反映されます。

