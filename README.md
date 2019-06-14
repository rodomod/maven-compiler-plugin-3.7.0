#Установка Мавен

####Последнюю версию всегда можно скачать на странице загрузки на официальном сайте.
####Просто распаковываем архив в любую директорию.
####Далее необходимо создать переменную в Path, в которой необходимо указать путь к Maven.
####Заходим в Win + Pause – Дополнительно –
####Переменные среды – в верхнем окошке нажимаем Создать,
####вводим имя M2_HOME и значение допустим "C:\apache-maven-2.2.1".
####Далее там же
####создаем еще одну переменную M2 со значением %M2_HOME%\bin.
####Так же убеждаемся, что есть переменная JAVA_HOME с путем к JDK.
####Ее значение должно быть примерно таким "C:\Program Files\Java\jdk1.6.0_10\".
####И наконец в том же окошке создаем/модифицируем переменную Path,
####в нее необходимо просто написать %M2%, чтобы наша папочка с исполняемым файлом Maven была видна из командной строки.
####Теперь необходимо проверить работоспособность нашей установки.
####Для этого заходим в командную строку и вводим команду

✦ mvn -v  или

✦ mvn -version
####Должна появиться информация о версиях Maven, jre и операционной системе, что-то вроде:

✦ Maven version: 2.2.1

✦ Java version: 1.6.0_10

✦ OS name: "windows 2003" version: "5.2" arch: "x86" Family: "windows"

####Maven создаст вам локальный репозиторий в вашей личной папке,
####например в каталоге C:\Documents and Settings\username\.m2\repository
####Все, Maven готов к работе, можно приступать к созданию приложения.
####В данной статье мы рассмотрим процесс создания простой программы,

####Запускаем cmd.exe от Администратора.

✦0) mvn validate : проверка корректности метаинформации о проекте  .

✦1) mvn compile : компилирует исходники .

✦2) mvn test : прогоняет тесты классов из предыдущего шага .

✦3) mvn package : упаковка скомпилированных классов в формат war,jar... .

✦4) mvn integration-test : отправляет упакованные классы в среду интегрированного тестирования и прогоняет тесты .

✦5) mvn verify : проверяет корректность пакета и удовлетворение требованиям качества .

✦6) mvn install : загоняет пакет в локальный репозиторий,откуда он будет доступен для использования как зависимость в других проектах .
             
✦7) mvn deploy : отправляет пакет на удалённый production сервер,откуда другие разработчики его могут получить и использовать  .			 

✦8) mvn site : ... .

✦9) mvn clean install : перезапись проекта .

✦10) mvn relase:perform  : выполнить(запуск проекта)! .

====What is eng====>
# Apache Maven

  What is it?
  -----------

  Maven is a software project management and comprehension tool. Based on
  the concept of a Project Object Model (POM), Maven can manage a project's
  build, reporting and documentation from a central piece of information.

  Documentation
  -------------

  The most up-to-date documentation can be found at https://maven.apache.org/.

  Release Notes
  -------------

  The full list of changes can be found at https://maven.apache.org/docs/history.html.

  System Requirements
  -------------------

  JDK:
    1.7 or above (this is to execute Maven - it still allows you to build against 1.3
    and prior JDK's).
  Memory:
    No minimum requirement.
  Disk:
    Approximately 10MB is required for the Maven installation itself. In addition to
    that, additional disk space will be used for your local Maven repository. The size
    of your local repository will vary depending on usage but expect at least 500MB.
  Operating System:
    Windows:
      Windows 2000 or above.
    Unix based systems (Linux, Solaris and Mac OS X) and others:
      No minimum requirement.

  Installing Maven
  ----------------

  1) Unpack the archive where you would like to store the binaries, e.g.:

    Unix-based operating systems (Linux, Solaris and Mac OS X)
      tar zxvf apache-maven-3.x.y.tar.gz
    Windows
      unzip apache-maven-3.x.y.zip

  2) A directory called "apache-maven-3.x.y" will be created.

  3) Add the bin directory to your PATH, e.g.:

    Unix-based operating systems (Linux, Solaris and Mac OS X)
      export PATH=/usr/local/apache-maven-3.x.y/bin:$PATH
    Windows
      set PATH="c:\program files\apache-maven-3.x.y\bin";%PATH%

  4) Make sure JAVA_HOME is set to the location of your JDK

  5) Run "mvn --version" to verify that it is correctly installed.

  For complete documentation, see https://maven.apache.org/download.html#Installation

  Licensing
  ---------

  Please see the file called LICENSE.

  Maven URLS
  ----------

  Home Page:          https://maven.apache.org/
  Downloads:          https://maven.apache.org/download.html
  Release Notes:      https://maven.apache.org/docs/history.html
  Mailing Lists:      https://maven.apache.org/mail-lists.html
  Source Code:        https://gitbox.apache.org/repos/asf/maven.git
  Issue Tracking:     https://issues.apache.org/jira/browse/MNG
  Wiki:               https://cwiki.apache.org/confluence/display/MAVEN/
  Available Plugins:  https://maven.apache.org/plugins/

