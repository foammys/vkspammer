<h2>VKSpammer</h2>
<h3>Бот для спама в личные сообщения участникам группы</h3>

——————

### Главное

* Перед использованием, настройте конфиг, вставьте токен от страницы (получить можно на vkhost.github.io)

#### Конфиг:

```
# -*- coding: utf-8 -*-
import vk_api # Не трогать
import time # Не трогать
import random # Не трогать
from vk_api.longpoll import VkLongPoll, VkEventType # Не трогать
group_id = input('Group ID: ') # Не трогать
vk_session = vk_api.VkApi(token="") # Сюда токен от страницы, получить можно на vkhost.github.io
longpoll = VkLongPoll(vk_session) # Не трогать
vk = vk_session.get_api() # Не трогать
usrs = vk.groups.getMembers(group_id=group_id,sort="id_desc") # Не трогать
usrs = usrs["items"] # Не трогать
for usr in usrs: # Не трогать
    messg = "random msg" # Сюда сообщение, которым спамить
    try:
        vk.messages.send(user_id=usr, random_id=random.randint(1,15000), message=messg) # Не трогать
    except: # Не трогать
        print(f"User {usr} closed private messages") # Здесь можно настроить кастом сообщение о закрытом ЛС
        pass # Не трогать
    time.sleep(7) # Здесь можно настроить задержку перед следующим сообщением (желательно не трогать, чтобы не отлететь за активность)
```

#### Запуск бота:

```
1. pip3 install vk_api
2. python3 spammerBot.py
```

#### Скриншот работы бота:
![](https://i.imgur.com/S2lcDkf.png "Screenshot")
