<div align="center">
  <h1>olcOS</h1>
  <p>Android 8+ · Kotlin · Jetpack Compose · WebRTC · VPN / SOCKS5</p>
  <p><strong>Beta</strong> · Функции и совместимость могут меняться.</p>
  <p><strong>Beta</strong> · Features and compatibility may change.</p>
  <h2><a href="#русский">Русский</a> &nbsp; / &nbsp; <a href="#english">English</a></h2>
  <p>Ваш телефон. Ваш сервер. Ваше подключение.</p>
  <p>Your phone. Your server. Your connection.</p>
</div>

---

## Русский

olcOS для Android — то же приложение, что [olcOS для iOS](https://github.com/Hotelk52339/olcos-ios): туннель через комнаты видеозвонков (Yandex Telemost, VK Звонки, SaluteJazz, Jitsi, WB Stream) и через Xray (VLESS + REALITY) на вашем собственном сервере.

### Установка

1. Скачайте последний `olcOS-android-<версия>.apk` со страницы [Releases](https://github.com/Hotelk52339/olcos-android/releases/latest).
2. Разрешите установку из этого источника (Android спросит сам) и установите. Новые версии ставятся поверх старых.
3. Приложение само скажет, когда выйдет новая версия (Настройки → Обновления).

### Свой сервер

Нужен любой VPS (Debian, Ubuntu, Fedora). Одна команда на сервере ставит всё и показывает QR-код приглашения:

```
curl -fsSL https://raw.githubusercontent.com/Hotelk52339/olcos-ios/main/install.sh | sudo bash
```

Отсканируйте его в olcOS: телефон станет владельцем сервера, и дальше всё делается из приложения: комнаты, протоколы, обновление ядра, приглашения для семьи (одна ссылка на каждое устройство, с доступом к управлению или без). Приглашения принимают и Android, и iPhone.

### Что умеет

- Два режима: **VPN** (всё устройство) и **прокси** (SOCKS5 для выбранных приложений, кнопка «Использовать в Telegram»).
- Подключения: ссылка `olcrtc://`, ссылка `vless://`, подписки и готовые списки, **приглашение с другого телефона** — все комнаты сервера, объединённое подключение «весь сервер» (несколько комнат сразу) и доступ к управлению сервером одной вставкой.
- Управление своим сервером: состояние и журналы, запуск и перезапуск комнат, смена комнаты (комнаты Jitsi, SaluteJazz, Telemost и VK создаются телефоном сами), добавление и удаление протоколов, новый ключ, обновление ядра, устройства с доступом.
- Проверка подключений и тест скорости по каждой комнате и всем вместе, маршрутизация «напрямую» для российских сайтов, журнал, QR и ссылки, виджет и плитка быстрых настроек.

### Исходники

Приложение собирается из того же Go-ядра, что и iOS-версия. Сборочный снимок: [olcos-android-build](https://github.com/Hotelk52339/olcos-android-build).

---

## English

olcOS for Android is the same app as [olcOS for iOS](https://github.com/Hotelk52339/olcos-ios): a tunnel through video-call rooms (Yandex Telemost, VK Calls, SaluteJazz, Jitsi, WB Stream) and through Xray (VLESS + REALITY) on your own server.

### Install

1. Download the latest `olcOS-android-<version>.apk` from [Releases](https://github.com/Hotelk52339/olcos-android/releases/latest).
2. Allow installs from this source when Android asks, and install. New versions install over old ones.
3. The app tells you when a new version is out (Settings → Updates).

### Your own server

Any VPS (Debian, Ubuntu, Fedora) will do. One command on the server installs everything and shows a QR code of an invite:

```
curl -fsSL https://raw.githubusercontent.com/Hotelk52339/olcos-ios/main/install.sh | sudo bash
```

Scan it with olcOS: the phone becomes the server's owner and everything else is done from the app: rooms, protocols, the core update, invites for the family (one link per device, with or without management access). Both Android and iPhone accept invites.

### Features

- Two modes: **VPN** (the whole device) and **proxy** (SOCKS5 for chosen apps, with "Use in Telegram").
- Connections: an `olcrtc://` link, a `vless://` link, subscriptions and ready-made lists, an **invite from another phone**: every room of the server, the whole-server connection (several rooms at once) and server access, with one paste.
- Your own server: state and logs, start and restart rooms, change a room (Jitsi, SaluteJazz, Telemost and VK rooms are made by the phone), add and remove protocols, a new key, a core update, devices with access.
- Connection checks and a speed test room by room and all together, direct routing for Russian sites, a log, QR and links, a widget and a quick-settings tile.

### Source

The app builds from the same Go core as the iOS app. The build snapshot: [olcos-android-build](https://github.com/Hotelk52339/olcos-android-build).
