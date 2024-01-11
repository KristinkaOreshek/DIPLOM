# Дипломный проект профессии «Тестировщик»
### Запуск SUT, авто-тестов и генерация репорта
### Подключение SUT к PostgreSQL
1.  Запустить Docker Desktop

2.  Открыть проект в IntelliJ IDEA

3.  В терминале в корне проекта запустить контейнеры:

docker-compose up --build

4.  Запустить приложение:

java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar

5.  Открыть второй терминал

6.  Запустить тесты:

.\gradlew clean test -DdbUrl=jdbc:postgresql://localhost:5432/app

7.  Создать отчёт Allure и открыть в браузере

.\gradlew allureServe

8.  Закрыть отчёт:

CTRL + C -> y -> Enter

9.  Перейти в первый терминал

10.  Остановить приложение:

CTRL + C

11.  Остановить контейнеры:

docker-compose down

### Подключение SUT к MySQL
1.  Запустить Docker Desktop

2.  Открыть проект в IntelliJ IDEA

3.  В терминале в корне проекта запустить контейнеры:

docker-compose up --build

4.  Запустить приложение:
java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar


5.  Открыть второй терминал

6.  Запустить тесты:

.\gradlew clean test -DdbUrl=jdbc:mysql://localhost:3306/app

7.  Создать отчёт Allure и открыть в браузере

.\gradlew allureServe

8.  Закрыть отчёт:

CTRL + C -> y -> Enter

9.  Перейти в первый терминал

10.  Остановить приложение:

CTRL + C

11.  Остановить контейнеры:

docker-compose down
