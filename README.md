Разрабатываем приложение на Spring и GWT. Часть 2 - Добавляем GWT
-----------------------------------------------------------------
* `hellogwt-2 - Alex Tretyakov Blog`: [http://alextretyakov.blogspot.com/2011/10/spring-gwt-2-gwt.html](http://alextretyakov.blogspot.com/2011/10/spring-gwt-2-gwt.html)
* `hellogwt-2 - Revision 6: /trunk`: [http://hellogwt-2.googlecode.com/svn/trunk/](http://hellogwt-2.googlecode.com/svn/trunk/)
> В процессе написания приложения будут использоваться:
>
>- Spring 3.0.5
>- GWT 2.4.0
>- Maven 3.0.3
>- Tomcat 6.0.33 ([http://localhost:8080/hellogwt/](http://localhost:8080/hellogwt/))

>Для интеграции Spring и GWT мы будем использовать библиотеку [spring4gwt](http://code.google.com/p/spring4gwt/). Её нет в репозитории Maven, поэтому ее нужно скачать [отсюда](http://code.google.com/p/spring4gwt/downloads/list) и добавить в директорию **WEB-INF/lib** нашего проекта.
>Библиотеку [spring4gwt](http://code.google.com/p/spring4gwt/) в проект можно добавить в локальный репозиторий Maven и указать зависимость от нее в **pom.xml**. Для этого нужно в директории с библиотекой выполнить следующую команду:
>
>***mvn install:install-file -Dfile=spring4gwt-0.0.1.jar -DgroupId=com.google.code -DartifactId=spring4gwt -Dversion=0.0.1 -Dpackaging=jar***

![result.png](result.png)
