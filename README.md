# hse-ab-homework-6

Разработать REST сервис для хранения паролей

Сервис должен поддерживать следующие операции:
+ Создать новую запись. На вход принимать название записи*, логин, пароль*, ссылка // * обязательные поля
+ Получить список всех записей - метод должен возвращать только id и названия. Должна быть версия с пагинацией
+ Получить конкретную запись - возвращает все поля
+ Обновить запись по Id

Формать сущности **Запись** следующий 
+ id: UUID
+ name: String
+ login: String
+ password: String
+ url: String

Формат запросов/ответов - JSON

Сущности пока хранить просто в in-memory коллекции 

Если не передан обязательный параметр - возвращать 400 код с человекочитаемой ошибкой (что посмотреть - https://www.baeldung.com/spring-boot-bean-validation, https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc/)
Если запись по id не найдена - 404 код

Написать сервисные тесты (@SpringBootTest), которые вызывают ваши эндпоинты (пример https://sysout.ru/testirovanie-spring-boot-prilozheniya-s-testresttemplate/)

Проект должен собираться с помощью maven/gradle. Тесты должны проходить в пайплайне

