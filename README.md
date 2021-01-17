You will find it at t.me/Skill_Progect2_TeleBot
или @Skill_Progect2_TeleBot

Бот возвращает цену на определённое количество валюты (евро, доллар или рубль).
При написании бота была использована библиотека pytelegrambotapi.
Человек должен отправить сообщение боту в виде <имя валюты, цену которой он хочет узнать> <имя валюты, в которой надо узнать цену первой валюты> <количество первой валюты>.
При вводе команды /start или /help пользователю выводятся инструкции по применению бота.
При вводе команды /values выводится информация о всех доступных валютах в читаемом виде.
Для взятия курса валют было использовано API exchangeratesapi, запросы к нему отправляются с помощью библиотеки Requests.
Для парсинга полученных ответов использована библиотека JSON.
При ошибке пользователя (введена неправильная или несуществующая валюта, неправильно введено число, слишком много параметров в команде) вызывается исключение ConvertionException с текстом пояснения ошибки.
Текст любой ошибки с указанием типа ошибки отправляется пользователю в сообщения.
Для отправки запросов к API описан класс со статическим методом get_price(), который принимает три аргумента: имя валюты, цену на которую надо узнать, — quote, имя валюты, цену в которой надо узнать, — base, количество переводимой валюты — amount, и возвращает нужное произведение в валюте.
