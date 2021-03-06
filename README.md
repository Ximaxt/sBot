# sBot


### Базовая настройка
Создайте в папке sBot файл `app.js`

Откройте его любым редактором, и вставьте туда следующий код:
```JavaScript
const bot = require('./bot'); //Ядро бота
bot.init({
  botname: ['обращения','к боту','маленькими','буквами'], // Список обращений к боту, необязательно
  token: 'access_token', // Токен VK API, обязательно
  rucaptcha: 'rucaptcha_key', // Ключ для сервиса распознавания капчи RuCaptcha, необязательно
  status: 'Hello, World!', // Статус, который будет установлен при запуске,  необязательно
  dictmode: 0,  // Режим словаря, где 0 = проверка всего сообщения на совпадение, а 1 = проверка каждого отдельного слова, необязательно (по умолчанию - 0)
  dictmatch: 1 // Процент совпадения текста для словаря, где 0,5 - 50% и 1 - 100%, необязательно (по умолчанию - 1)
});
bot.dict.import({
    'Тест': 'Привет, я sBot!',
    'Привет': 'Здравствуй!'
});
```
Для получения токена VK API перейдите по ссылке, указанной в [tokenurl.txt](tokenurl.txt) и скопируйте результат из адресной строки, как показано на картинке:   
![Получение токена](http://i.imgur.com/vSb5TlU.png)


### Запуск бота
Для **Linux** перейдите в папку с sBot

Для **Windows** откройте папку sBot, нажмите правую кнопку мыши, удерживая Shift и выберите *Открыть окно команд*

Далее напишите `npm install && npm start`

*(Это установит необходимые пакеты и запустит бота)*

Теперь Вы можете написать боту "Тест" в личные сообщения или "_Обращение_, тест" в беседе и он ответит Вам "Привет, я sBot!". Аналогично с "Привет", на что будет ответ "Здравствуй!"

Чтобы узнать больше о настройке бота, читайте [Wiki](https://github.com/m4l3vich/sBot/wiki)

*Огромное спасибо @RedFoxCode за модуль closest-str <3*
