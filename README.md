<div align="center">
  <img src="./media/pictures/bruce_banner.jpg" alt="Bruce banner" width="100%" />

  <h1>Bruce</h1>
  <p><strong>Кибер-прошивка для ESP32 и M5Stack.</strong> Offensive tooling, аппаратные эксперименты и универсальная платформа для совместимых устройств.</p>

  <p>
    <img src="https://img.shields.io/badge/ESP32-firmware-111827?style=for-the-badge&logo=espressif&logoColor=22C55E" alt="ESP32 firmware" />
    <img src="https://img.shields.io/badge/M5Stack-supported-111827?style=for-the-badge&logoColor=22C55E" alt="M5Stack supported" />
    <img src="https://img.shields.io/badge/Cardputer-ready-111827?style=for-the-badge&logoColor=22C55E" alt="Cardputer ready" />
    <img src="https://img.shields.io/badge/red-team-tooling-22C55E?style=for-the-badge&labelColor=0B1220" alt="Red team tooling" />
  </p>
</div>

```text
> firmware: Bruce
> focus: wifi / ble / rf / rfid / ir / nrf24
> mission: flexible offensive and embedded experimentation on ESP32 devices
```

## обзор

`Bruce` — это универсальная прошивка для `ESP32`, заточенная под исследование протоколов, Red Team-задачи и практическую работу с линейкой `M5Stack` и похожими устройствами.

## Установка

### Самый простой способ

Самый удобный вариант установки — официальный Web Flasher:
- https://bruce.computer/flasher

### Локальная прошивка через `esptool.py`

Можно скачать готовый бинарник из `Releases` или `Actions` и прошить устройство локально:

```sh
esptool.py --port /dev/ttyACM0 write_flash 0x00000 Bruce-<device>.bin
```

### Для устройств `M5Stack`

Если вы уже используете `M5Launcher`, прошивку можно установить по `OTA`.

Также можно прошить устройство через [m5burner tool](https://docs.m5stack.com/en/download):
- откройте нужную категорию устройств;
- найдите `Bruce`;
- выберите официальную сборку автора и выполните прошивку.

## Сообщество и документация

- Discord: https://discord.gg/WJ9XF9czVT
- Wiki: https://github.com/pr3y/Bruce/wiki
- FAQ: https://github.com/pr3y/Bruce/wiki/FAQ

## Основные возможности

### Wi‑Fi

- подключение к Wi‑Fi и режим точки доступа;
- Wi‑Fi attacks, Beacon Spam и Target Attack;
- deauth-сценарии;
- Wardriving;
- `TelNet`, `SSH`, `TCP Client`, `TCP Listener`;
- `RAW Sniffer`, `Scan Hosts`, `Evil Portal`, `Wireguard Tunneling`;
- режимы `Brucegotchi`.

### BLE

- `BLE Scan`;
- `Bad BLE` и запуск Ducky-скриптов;
- BLE-клавиатура для поддерживаемых устройств;
- спам-режимы для `iOS`, `Windows`, `Samsung`, `Android`.

### RF / RFID / IR / FM / NRF24

- сканирование и повтор передачи радиосигналов;
- работа с `CC1101` и совместимыми RF-модулями;
- чтение и запись RFID-меток, поддержка `PN532` и `PN532Killer`;
- ИК-передача и прием;
- FM-функции;
- `NRF24 Jammer` и 2.4G spectrum.

### Дополнительно

- `JavaScript Interpreter`;
- `SD Card Manager` и `LittleFS Manager`;
- `WebUI`;
- `BADUsb`;
- `Openhaystack`;
- `iButton`;
- управление LED;
- часы, NTP и ручная настройка времени;
- обмен файлами и командами через `ESPNOW`.

## Поддерживаемые устройства

В репозитории есть поддержка и конфигурации для разных платформ, включая:
- `M5Stack Cardputer`;
- `M5StickC Plus / Plus2`;
- `M5Core`, `M5Core2`, `M5CoreS3`;
- `JCZN CYD-2432S028`;
- `Lilygo T-Embed`, `T-Embed CC1101`, `T-Deck`, `T-Display-S3`, `T-Watch-S3`.

Подробная таблица совместимости и аппаратных возможностей доступна в upstream-документации и wiki проекта.

## Как это выглядит

Идея `Bruce` выросла из сообщества вокруг устройств вроде `Flipper Zero`: хотелось получить более гибкую и доступную по цене платформу на базе `ESP32`, `Lilygo` и `M5Stack`, не теряя при этом функциональность для исследований и практики.

![Bruce Main Menu](./media/pictures/pic1.png)
![Bruce on M5Core](./media/pictures/core.png)
![Bruce on Stick](./media/pictures/stick.png)
![Bruce on CYD](./media/pictures/cyd.png)

Остальные изображения находятся в каталоге `./media/`.

## Благодарности

Спасибо всем, кто вносил вклад в проект, портировал его на новые устройства, расширял список функций и помогал с дизайном, платами и документацией.

## Дисклеймер

`Bruce` — инструмент для исследовательских, учебных и авторизованных задач в области информационной безопасности, поставляемый по лицензии `AGPL`.

Используйте прошивку только в рамках закона и только на системах, устройствах и сетях, для которых у вас есть явное разрешение. Любое несанкционированное или вредоносное применение запрещено. Разработчики не несут ответственности за неправильное использование. Все действия вы выполняете на свой риск.

## контакты

<p>
  <a href="https://github.com/GradusXaker"><img src="https://img.shields.io/badge/GitHub-GradusXaker-111827?style=flat-square&logo=github&logoColor=22C55E" alt="GitHub" /></a>
  <a href="https://vk.com/gradus_xaker"><img src="https://img.shields.io/badge/VK-gradus__xaker-111827?style=flat-square&logo=vk&logoColor=22C55E" alt="VK" /></a>
  <a href="mailto:gradus_xaker@mail.ru"><img src="https://img.shields.io/badge/email-write-111827?style=flat-square&logo=gmail&logoColor=22C55E" alt="Email" /></a>
</p>

