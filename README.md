Задание состоит из формы и таблицы. Внизу можно найти файл сервера
Форма имеет 2 поля longitude, latitude (0 <= n <= 180).
При сабмите отправляет данные на сервер, получает коэфициенты, что будут использоваться ниже.

GET /rates?longitude=x&latitude=y
{
    "rate1": 12
    "rate2": 14
}
Данные для таблицы:

GET /people?page=x&size=y
{
  "meta": {
    "total": 1000,
    "page": 1,
    "size": 10,
  },
  "data": [
    {
      "firstName": "George",
      "middleName": "RR",
      "lastName": "Martin",
      "birthday": "1948-09-20"
      "rate3": 34,
      "rate4": 16
    }
  ]
}

Отобразить колонки:
Full Name: fitstName + middleName + lastName
Birthday: Sep 20, 1948
Index1:  rate1^rate3 / rate3^rate1
Index2: fib(rate4) / fib(rate2)

Таблица и форма должны работать одновременно
Можно использовать любые библиотеки. Их количество и количество самого кода не ограничевается
Интерфейс должен быть понятен в использовании и приятен глазу
Сервер оттестирован и работает как требуется
Приложение должно разворачиваться с помощью коммады

$ yarn install && yarn build && serve -s build
$ node server.js
