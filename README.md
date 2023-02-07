# Инструкция TGParser

По поводу покупки софта: https://t.me/HolmenGS

## Возможности парсера
- Сбор всех каналов из 47 тематик на сайте [TGSTAT](https://tgstat.ru/).
- Фильтрация каналов по открытым комменатариям и минимальному охвату.
- Проверка в отфильтрованных каналах наличия анти-спам бота.
- Возобновление работы в случае блокировки аккаунта ТГ на этапе проверки анти-спам бота.

## Инструкция по установке
Перед использованием бота необходимо скачать [Python](https://www.python.org/ftp/python/3.11.1/python-3.11.1-amd64.exe). Во время установки не забудьте установить галочку напротив "Add python.exe to PATH".

![Установка Python](https://i.imgur.com/9Vdl03a.png)

После того как мы установили Python, заходим в папку с парсером и далее в папку "start". В этой папке мы запускаем файл "Ключ TGParser.exe" и ожидаем полной установки необходимых библиотек и генерации уникального ключа.

Как только появится надпись "Press any key to continue", это значит, что установка завершена. Закрываем окно с консолью и заходим в файл "key.txt", копируем полученный ключ и отправляем мне в [ЛС](https://t.me/HolmenGS).

## Инструкция по парсеру

Перед началом использования парсера, необходимо в папку *session* закинуть файл сессии (аккаунт). Сессия **обязательно** должна быть формата telethon и название сессии может быть любое.

Еще вам нужно будет настроить конфиг в папке под названием '*config.ini*'. В параметре **TEXT** у нас находится ссылка на канал ТГ, которую бот будет отправлять в комменты для проверки наличия анти-спам бота.

В разделе PROXY, тут мы указываем прокси, которые хотим использовать. Прокси должны быть формата HTTP(S). Если не хотим использовать прокси, то оставляем просто как есть (но лучше их использовать, ниже будет написано почему).

Также перед использованием парсера вам нужно скачать Google Chrome и обновить его до последней версии. Сделать это можно здесь: *chrome://settings/help* (Вставьте это в адресную строку Google Chrome).

Если вы захотите добавить каналы в исключение, которые не нужно парсить, вы можете вписать ссылки на каналы построчно в файле "*channels_exception.txt*", который хранится в папке *data*.

**Рекомендую вписывать только те каналы, которые вы получили при работе этого парсера** (при этом желательно сохранять такой же порядок, в котором вам их выдал парсер), т.к парсер исключает каналы по "особому режиму".

Как только мы закинули файл сессии, мы можем запускать парсер через файл "*TGParser.exe*", в открывшимся окне выбираем тематику, вписываем минимальное кол-во охватов для парсинга, кол-во страниц, которое мы хотим пропарсить (на каждой странице 102 канала. Чем больше страниц, тем дольше происходит парсинг), а также выбираем использовать ли прокси или нет (Вам нужно ввести '**Y**' (Yes) или '**N**' (No)).

![Вид рабочего софта](https://i.imgur.com/sHRT1th.png)

После того, как мы вписали все необходимые параметры, парсер начнет искать нужные каналы. О всех действиях парсер вас будет информировать.

![Софт в работе](https://i.imgur.com/YE0dMBv.png)

Как только парсер закончит работу, он оповестит вас об этом. Каналы, которые подходят под ваши критерии, и в которых можно спокойно размещать ссылки, будут находится в "*data/channels.txt*".

## Рабочие нюансы

Также во время работы парсера на этапе проверки антиспам бота в канале ТГ, у вас может забанить или отправить в спам-блок аккаунт ТГ, с которого идет проверка.

Если такое вдруг произошло, то вам нужно закрыть парсер, заменить аккаунт и во время следующего запуска бот вас спросит, продолжить ли работу.

Также во время парсинга каналов на сайте [TGSTAT](https://tgstat.ru), ваш IP-адрес, с которого вы запускаете парсер может быть заблокирован из-за большого кол-во запросов на сайт, поэтому лучше всего использовать прокси во время работы. Если вы не используете TGSTAT и вашего IP-адреса, то можете спокойно обходится и без прокси.