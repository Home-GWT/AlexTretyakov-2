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


>При деплое GWT-проекта на Tomcat вываливается ошибка типа:
>
>- **Error:GWT Compiler: Element 'module' beginning on line 17 contains unexpected attribute 'type'**
>- **Error:GWT Compiler: Failure while parsing XML**
>
>При запуске GWT-проекта в консоли тоже вываливается ошибка типа:

[INFO] One or more required plugin parameters are invalid/missing for 'gwt:run'

[0] Inside the definition for plugin 'gwt-maven-plugin' specify the following:

<configuration>
  ...
  <runTarget>VALUE</runTarget>
</configuration>

-OR-

on the command line, specify: '-DrunTarget=VALUE'
>(Возможно эта ошибка связана с тайм-зоной и на разных компьютерах ведет себя по разному...
>
> [it is only relevant to a small geographic area, a specific moment in time, or an extraordinarily narrow situation that is not generally applicable to the worldwide audience of the internet](http://stackoverflow.com/questions/15764203/gwt-compiler-errors)
>
>[gwt-maven-plugin](http://blog.soat.fr/2013/01/gwt-tips-12-compiling-debugging-et-logging/)
>
>[GWT 2.6.0-rc1 error compiling](https://groups.google.com/forum/#!topic/google-web-toolkit/18hhCitwKFE))
>
>Перехожу, в консоли, в рабочую папку проекта и запускаю GWT-проекта в режиме **Dev Mode**:
>
> **mvn gwt:run -DrunTarget=hellogwt**
>
>Дальше в веб-броузере перехожу по ссылке: [http://127.0.0.1:8888/](http://127.0.0.1:8888/)

![result.png](result.png)
