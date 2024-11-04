# Финальное задание на курсе "Go-разработчик с нуля" от Яндекс Практикум

## Описание проекта

Этот проект выполнен Владимировым Андреем как финальное задание на курсе "Go-разработчик с нуля" от Яндекс Практикум. Он представляет собой веб-приложение планировщик для управления задачами. Планировщик хранит задачи, каждая из них содержит дату дедлайна и заголовок с комментарием. Задачи могут повторяться по заданному правилу: ежегодно или через какое-то количество дней. Если отметить такую задачу как выполненную, она переносится на следующую дату в соответствии с правилом. Обычные задачи при выполнении будут просто удаляться. 
API содержит следующие операции:
добавить задачу;
получить список задач;
удалить задачу;
получить параметры задачи;
изменить параметры задачи;
отметить задачу как выполненную.

## Описание директорий и файлов

-   **`/database`**: Содержит функции для создания и управления базой данных SQLite для хранения задач с повторениями. Он позволяет создавать, получать, обновлять и удалять задачи.
-   **`/handlers`**: Содержит обработчики HTTP-запросов для управления задачами в приложении. Он реализует:
1. Получение следующей даты задачи на основе текущей даты и правил повторения.
2. Создание, получение, обновление и удаление задач через соответствующие HTTP-методы (POST, GET, PUT, DELETE).
3. Валидацию входных данных, включая формат даты и правила повторения.
4. Работу с базой данных, используя функции из пакета database для взаимодействия с SQLite.
-   **`/models`**: Содержит структуру задачи.
-   **`/utils`**: Содержит функцию вычисления следующей даты задачи для повторяющихся задач.
-   **`/tests`**: Содержит тесты для различных компонентов приложения.
-   **`/web`**: В этой директории хранятся статические файлы фронтенда, такие как HTML и CSS.

## Задачи со звездочкой

Реализована возможность определять порт для подключения и путь к файлу базы данных  через переменную окружения.

## Запуск проекта локально

### Шаги для запуска:

1. Склонируйте репозиторий:

    ```bash
    git clone <URL вашего репозитория>
    cd <название папки>
    ```

2. Запустите приложение с помощью Go:

    ```bash
    go run .
    ```

3. Откройте браузер и перейдите по адресу:
    ```
    http://localhost:7540
    ```


## Запуск тестов

Для запуска тестов выполните следующую команду:

```bash
go test ./tests -v
```

Для очистки кэша перед повторными тестами:

```bash
go clean -testcache
```


