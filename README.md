# tg-controller-deploy-template

## INFO

- Автор: Zeph1rr
- Язык: JavaScript
- Используемые библиотеки/фреймворки: nodejs, express, node-telegram-bot-api, reactjs, mui, seetalert2

## INSTALLATION

- Создать своего telgram бота с помощью @BotFather (Можно воспользоваться [инструкцией](https://botcreators.ru/blog/kak-sozdat-svoego-bota-v-botfather/))
- Скачать или склонировать репозиторий на linux машину с установленным docker-compose (git clone https://github.com/Zeph1rr/tg-controller-deploy-template.git)
- Настроить переменные окружения в соответствии с [инструкцией](#ENV) (Достаточно поменять только app_env, остальное для гибкости)
- Запустить программу с помощью docker-compose up -d
- Перейти в браузере по адресу ip.of.your.machine:external_port


## ENV

### Переменные окружения для сборки проекта (.env)

- PORT - Внутренний порт контйнера, на котором работает приложение (Оставить 3000)
- EXTERNAL_PORT - Порт машины, на которой запускается приложение, которое будет "слушать" входяший трафик (Можно любой, по умолчанию 5000)
- VERSION - Версия приложения. Посмотреть версии можно [здесь](https://hub.docker.com/repository/registry-1.docker.io/zeph1rrio/tg-controller/general)
- LOG_PATH - Папка внутри контейнера, куда складываются логи. Используется для пробрасывания volumes(По умолчанию /var/log/tg-controller
)

### Переменные окружения для приложения (app_env)

- BOT_TOKEN - Токен бота, полученный в первом шаге инструкции по установке
- CHATS - Список чатов, куда бот должен отправлять сообщения. Записываются через запятую без пробелов (chat_id1,chat_id2...) Свой chat_id посмотреть с помощью бота @username_to_id_bot
- NEED_CONSOLE_LOG - Переменная, отвечающая за вывод логов приложения в логи docker-compose, помимо записи в файл. (По умолчанию true)
- DEBUG_LEVEL - Уровень логирования. Возможные уровни можно прочитать [здесь](https://github.com/Zeph1rr/logging-middleware-express) (По умолчанию full)
- LOG_PATH - Папка внутри контейнера, куда складываются логи. Должна соответствовать такому же параметру из env (По умолчанию /var/log/tg-controller
)
- PORT - Внутренний порт контйнера, на котором работает приложение (Оставить 3000)
- TZ - Таймзона для корректного указания времени в логах. (По умолчанию Europe/Moscow)


## SCREENSHOTS

![Form](https://i.imgur.com/upmmpiY.png)

![Alert](https://i.imgur.com/FiykBPJ.png)

![Bot](https://i.imgur.com/fCjVdAa.png)