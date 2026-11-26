# [RUS]

# XrayHub

XrayHub — клиент для Windows, который управляет подключениями через **Xray Core**. В приложении можно хранить серверные профили, подключаться в режиме прокси или TUN, задавать DNS и настраивать правила маршрутизации.

## Возможности

- Импорт профилей по ссылкам `vless://`, `vmess://`, `trojan://` и `ss://`.
- Импорт Xray JSON-конфигураций и HTTPS-подписок, в том числе подписок в Base64.
- Обновление подписок вручную или автоматически по заданному интервалу.
- Проверка отклика серверов.
- Два режима подключения: **Прокси** и **Туннель (TUN)**.
- Локальные SOCKS5- и HTTP-входы. По умолчанию используются порты `10808` и `10809`; порты можно изменить в настройках.
- Возможность включить системный прокси Windows в режиме «Прокси» и задать авторизацию локального SOCKS5.
- Настройка DNS, MTU и параметров Xray Core, включая Mux и фрагментацию.
- Тёмная и светлая темы, русский и английский интерфейс, работа через системный трей и журнал событий.

## Режимы подключения

### Прокси

XrayHub запускает локальные SOCKS5- и HTTP-входы. При включённой настройке системного прокси приложение также направляет трафик программ, использующих прокси Windows, через локальное подключение.

### Туннель (TUN)

Xray Core создаёт виртуальный сетевой интерфейс и обрабатывает проходящий через него трафик. В этом режиме доступны настройки DNS, MTU, обхода частных сетей, защиты от DNS-утечек и блокировки QUIC (UDP/443).

Для работы TUN требуются права администратора. Приложение запрашивает их при запуске.

## Маршрутизация

Пользовательские правила маршрутизации доступны в режиме **Туннель (TUN)**.

Можно выбрать маршрут по умолчанию и задать действия для отдельных доменов или приложений:

- **Прокси** — отправлять трафик через выбранный сервер.
- **Напрямую** — использовать прямое подключение.
- **Блокировать** — не пропускать соответствующий трафик.

Для приложений правило задаётся по исполняемому файлу (`.exe`). Правила приложений имеют приоритет над правилами доменов. Изменения правил сохраняются автоматически и применяются при следующем подключении.


# [ENG]

# XrayHub

XrayHub is a Windows client that manages connections via **Xray Core**. The application allows you to store server profiles, connect in proxy or TUN mode, set DNS, and configure routing rules.

## Features

- Importing profiles via links `vless://`, `vmess://`, `trojan://`, and `ss://`.
- Importing Xray JSON configurations and HTTPS subscriptions, including Base64-encoded subscriptions.
- Updating subscriptions manually or automatically at a specified interval.
- Checking server response.
- Two connection modes: **Proxy** and **Tunnel (TUN)**.
- Local SOCKS5 and HTTP inputs. By default, ports `10808` and `10809` are used; the ports can be changed in the settings.
- The ability to enable the Windows system proxy in “Proxy” mode and set up local SOCKS5 authorization.
- Configuration of DNS, MTU, and Xray Core parameters, including Mux and fragmentation.
- Dark and light themes, Russian and English interfaces, operation via the system tray and event log.

## Connection modes

### Proxy

XrayHub launches local SOCKS5 and HTTP inputs. When the system proxy setting is enabled, the application also routes the traffic of programs that use the Windows proxy through a local connection.

### Tunnel (TUN)

Xray Core creates a virtual network interface and processes the traffic passing through it. In this mode, you can configure DNS, MTU, private network bypass, DNS leak protection, and QUIC (UDP/443) blocking.

TUN requires administrator privileges. The application requests them at startup.

## Routing

Custom routing rules are available in the **Tunnel (TUN)** mode.

You can select a default route and define actions for individual domains or applications:

- **Proxy** — send traffic through the selected server.
- **Directly** — use a direct connection.
- **Block** — do not allow the corresponding traffic.

For applications, the rule is set based on the executable file (`.exe`). Application rules take precedence over domain rules. Changes to the rules are saved automatically and are applied during the next connection.
