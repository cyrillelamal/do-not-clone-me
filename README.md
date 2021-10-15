# Maven, JUnit

## Как создать такой же проект и что с ним делать

Следующие шаги можно выполнить гораздо проще, используя какой-нибудь пакетный менеджер, например `brew` - в macOS, `chocolatey` - в Windows, `apt-get` - в Ubuntu.

1. Установите JDK (Java Development Kit): [https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/). Обратите внимание на то, куда устанавливается JDK. 

    1. Добавьте в переменную окружения `PATH` путь к исполняемым JDK утилитам. Например в Windows.

    ```bat
    set PATH=%PATH%;C:\Program Files\OpenJDK\jdk-16.0.2\bin
    ```

    2. Установите переменную окружения `JAVA_HOME` с путем к JDK. Например в Windows.
    
    ```bat
    set JAVA_HOME=C:\Program Files\OpenJDK\jdk-16.0.2
    ```

    Все эти этапы подробно описаны в [инструкции по установке JDK](https://docs.oracle.com/en/java/javase/17/install/overview-jdk-installation.html#GUID-8677A77F-231A-40F7-98B9-1FD0B48C346A).

2. Установите Maven: [скачать](https://maven.apache.org/download.cgi) и [установить](https://maven.apache.org/install.html)

    1. Добавьте в переменную окружения `PATH` путь к Maven. Например в Windows.

    ```bat
    set PATH=%PATH%;C:\ProgramData\chocolatey\lib\maven\apache-maven-3.8.2\bin
    ```

3. Инициализируйте новый проект в интерактивном режиме, используя базовый шаблон.

Интерактивынй режим (как `npm init`):
```shell
mvn archetype:generate
```
На первом шаге вас попросят выбрать шаблон; значение по умолчанию - это и есть базовый шаблон.

Также можно создать Maven проект с помощью IDE или вручную (для этого воссоздайте структуру этого репозитория).

4. Перейдите в сгенерированную директорию проекта: вы готовы к использованию Maven, например:

```shell
mvn package
```

Исходные коды надо складывать в `src/main/java/**`, а тесты - в `test/java/**`. 

> [JUnit4 - Getting started](https://github.com/junit-team/junit4/wiki/Getting-started#create-the-class-under-test)

> Да, уже давно существует JUnit5, но он требует дополнительной настройки.
