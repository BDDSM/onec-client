# Образ клиента 1С:Предприятие

## Сборка 

1. Создать файл `.env` в корне проекта. В качестве примера использовать `.env.example`. В файле должны быть определены переменные:
```
    ONEC_USERNAME=<ПОЛЬЗОВАТЕЛЬ_USERS.1C.V8.RU>
    ONEC_PASSWORD=<ПАРОЛЬ_ОТ_USERS.1C.V8.RU>
    ONEC_VERSION=8.3.14.199
```
2. Запустить сборку образа с помощью скрипта

```
    ./make.sh
```

4. Для полноценной работы клиента 1СЖПредприятие в контейнере необходимо запустить графический сервер, командой

```
    xstart
```

5. В файл /opt/1C/v8.3/x86_64/conf/nethasp.ini добавить путь к менеджеру лицензирования, например так:

```
    echo -e NH_SERVER_ADDR = 1.2.3.4. >> /opt/1C/v8.3/x86_64/conf/nethasp.ini
```