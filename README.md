<h2>VKSpammer</h2>
<h3>Бот для спама в личные сообщения участникам группы</h3>

——————

### Главное

* Перед использованием, настройте конфиг, вставьте токен от страницы (получить можно на vkhost.github.io)

#### Конфиг (что можно менять):

```
vk_session = vk_api.VkApi(token="") # Сюда токен от страницы, получить можно на vkhost.github.io
messg = "random msg" # Сюда сообщение, которым спамить
print(f"User {usr} closed private messages") # Здесь можно настроить кастом сообщение о закрытом ЛС
time.sleep(7) # Здесь можно настроить задержку перед следующим сообщением (желательно не трогать, чтобы не отлететь за активность)
```

#### Запуск бота:

```
1. pip3 install vk_api
2. python3 spammerBot.py
```

#### Скриншот работы бота:
![](https://i.imgur.com/S2lcDkf.png "Screenshot")

## Лицензия

Copyright © 2022 <a href="https://github.com/foammys">foammys</a>

Проект распространяется под лицензией <a href="https://github.com/foammys/vk-phising-page/blob/main/LICENSE">MIT</a>
