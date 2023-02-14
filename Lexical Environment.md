Лексическое окружение это специальный скрытый объект, все переменные объявленные внутри функции попадают сюда при выполнении функции.

Лексическое окружение состоит из 2 частей
1. [[Environment Record]]
2. Ссылка на внешнее лексическое окружение.

Переменные заданые через let или const попадают в этот объект только после объявления перменных во время исполнения машинного кода.

[[Function Declaration]] сразу попадают в [[Environment Record]], поэтому их можно использовать до объявления.

Каждый вызов функции создаёт новый Lexical Environment.


#programming/web/frontend/js