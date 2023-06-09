# Проект по автоматизации тестирования для интернет-магазина "fix-price"
<a target="_blank" href="https://fix-price.com/">Вэб сайт fix-price!</a>

## :pushpin: Содержание:

- [Технологии и инструменты](#earth_africa-технологии-и-инструменты)
- [Реализованные проверки](#earth_africa-Реализованные-проверки)
- [Сборка в Jenkins](#earth_africa-Jenkins-job)
- [Запуск из терминала](#earth_africa-Запуск-тестов-из-терминала)
- [Allure отчет](#earth_africa-Allure-отчет)
- [Интеграция с Allure TestOps](#earth_africa-Интеграция-с-Allure-TestOps)
- [Интеграция с Jira](#earth_africa-Интеграция-с-Jira)
- [Отчет в Telegram](#earth_africa-Уведомление-в-Telegram-при-помощи-бота)

## :electric_plug:Технологии и инструменты

<p align="center">
<a href="https://www.jetbrains.com/idea/"><img src="images/logo/Idea.svg" width="50" height="50"  alt="IDEA"/></a>
<a href="https://www.java.com/"><img src="images/logo/Java.svg" width="50" height="50"  alt="Java"/></a>
<a href="https://github.com/"><img src="images/logo/GitHub.svg" width="50" height="50"  alt="Github"/></a>
<a href="https://junit.org/junit5/"><img src="images/logo/Junit5.svg" width="50" height="50"  alt="JUnit 5"/></a>
<a href="https://gradle.org/"><img src="images/logo/Gradle.svg" width="50" height="50"  alt="Gradle"/></a>
<a href="https://selenide.org/"><img src="images/logo/Selenide.svg" width="50" height="50"  alt="Selenide"/></a>
<a href="https://aerokube.com/selenoid/"><img src="images/logo/Selenoid.svg" width="50" height="50"  alt="Selenoid"/></a>
<a href="https://github.com/allure-framework/allure2"><img src="images/logo/Allure.svg" width="50" height="50"  alt="Allure"/></a>
<a href="https://qameta.io/"><img src="images/logo/Allure_TO.svg" width="50" height="50"  alt="Allure TestOps"/></a>
<a href="https://www.atlassian.com/ru/software/jira"><img src="images/logo/jira-logo.svg" width="50" height="50"  alt="Atlassian Jira"/></a>
<a href="https://www.jenkins.io/"><img src="images/logo/Jenkins.svg" width="50" height="50"  alt="Jenkins"/></a>
</p>

## :mag: Реализованные проверки

- ✓ Проверка работы корзины.
- ✓ Проверка раздела "Работа у нас".
- ✓ Проверка работы закладок.
- ✓ Проверка поиска товара.
- ✓ Проверка изменения города.

##  :rocket: Запуск тестов

### Локальный запуск тестов

```bash
gradle clean test
```

### Удаленный запуск тестов

```bash
gradle clean test -Denv = 'remote'
```

### Параметры сборки находятся в файле remote.properties

> <code>remoteUrl</code> – адрес удаленного сервера, на котором будут запускаться тесты.
>
> <code>browserName</code> – браузер, в котором будут выполняться тесты .
>
> <code>browserVersion</code> – версия браузера, в которой будут выполняться тесты .
>
> <code>browserSize</code> – размер окна браузера, в котором будут выполняться тесты .

###  Удаленный запуск (в Jenkins):
1.  Открыть <a target="_blank" href="https://jenkins.autotests.cloud/job/Students/job/alyonaefros_diplom_UI/">проект</a>

![This is an image](/images/screens/Jenkins1.png)

2. Выбрать пункт **Собрать с параметрами**
3. В случае необходимости изменить название файла properties
4. Нажать **Собрать**
5. Результат запуска сборки можно посмотреть в отчёте Allure

![This is an image](/images/screens/Jenkins22.png)

## <img src="images/logo/Allure.svg" width="25" height="25"  alt="Allure"/></a> Отчет в <a target="_blank" href="https://jenkins.autotests.cloud/job/Students/job/alyonaefros_diplom_UI/13/allure/">Allure report</a>

###  Главное окно

<p align="center">
<img title="Allure Overview Dashboard" src="images/screens/Allure_Report1.png">
</p>

###  Тесты

<p align="center">
<img title="Allure Tests" src="images/screens/Allure_Report2.png">
</p>

###  Графики

<p align="center">
<img title="Allure Graphics" src="images/screens/Allure_Report3.png">
</p>

## <img src="images/logo/Allure_TO.svg" width="25" height="25"  alt="Allure"/></a> Интеграция с <a target="_blank" href="https://allure.autotests.cloud/project/2295/dashboards">Allure TestOps</a>

### Dashboard с  результатами тестирования
<p align="center">
<img title="Allure Graphics" src="images/screens/allureTO-report.png">
</p>

### Пример отчёта выполнения одного из автотестов
<p align="center">
<img title="Allure Graphics" src="images/screens/allureTO_dashboard.png">
</p>

## <img src="images/logo/jira-logo.svg" width="25" height="25"  alt="Allure"/></a> Интеграция с <a target="_blank" href="https://jira.autotests.cloud/browse/HOMEWORK-706">Atlassian Jira</a>
<p align="center">
<img title="Jira" src="images/screens/Jira1.png">
</p>

## <img src="images/logo/Telegram.svg" width="25" height="25"  alt="Allure"/></a> Уведомление в Telegram о результатах прогона тестов

<p align="center">
<img title="Allure Overview Dashboard" src="images/screens/telegramNotif.jpg" >
</p>

### <img width="4%" style="vertical-align:middle" title="Selenoid" src="images/logo/Selenoid.svg"> Видео примера запуска тестов в Selenoid

К каждому тесту в отчете прилагается видео прогона.
<p align="center">
  <img title="Selenoid Video" src="images/screens/video.gif">
</p>
