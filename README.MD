## Домашнее работа к лекции «Работа с PostgreSQL из Python»  
Для заполнения таблицы используются данные сгенерированные chatGPT из файла data.json  
Для обновления номера/номеров телефона клиента мною был выбран вариант, где старые номера телефонов сначала удаляются, а затем добавляются новые (от 1 до беск.). Благодаря такому подходу удалось избежать некоторые проблемы:
- У пользователя несколько номеров, а в функцию передается только 1. Не ясно, какой из номеров исправлять. 
- У пользователя нет номеров, соотвественно для него не создавалась запись в таблице phone. (При использовании LEFT JOIN для выборки клиентов и их номеров для отсутствующего телефона будет выведено значение NULL)
- Количество передаваемых номеров больше, чем существует номеров у клиента.