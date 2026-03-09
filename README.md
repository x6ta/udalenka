# Удалёнка 🖥️

Бесплатный удалённый доступ к рабочему столу. Open-source.

Форк [RustDesk](https://github.com/rustdesk/rustdesk) с полной русификацией.

## Возможности

- 🖥️ **Удалённый рабочий стол** — управляйте компьютером из любой точки мира
- 📁 **Передача файлов** — обмен файлами между машинами
- 🔒 **End-to-end шифрование** — ваши данные защищены
- 🌐 **Кроссплатформенность** — Windows, macOS, Linux, Android, iOS
- 🏠 **Свой сервер** — полная независимость от облачных сервисов
- 🆓 **Бесплатно** — open-source под лицензией AGPLv3

## Быстрый старт

### Установка клиента

Скачайте последнюю версию со страницы [Releases](https://github.com/x6ta/udalenka/releases).

### Свой сервер

```bash
# Docker (рекомендуется)
docker run -d --name udalenka-server \
  -p 21115:21115 -p 21116:21116 -p 21116:21116/udp \
  -p 21117:21117 -p 21118:21118 -p 21119:21119 \
  rustdesk/rustdesk-server hbbs

docker run -d --name udalenka-relay \
  -p 21117:21117 \
  rustdesk/rustdesk-server hbbr
```

### Сборка из исходников

```bash
# Зависимости (Ubuntu/Debian)
sudo apt install -y g++ gcc git curl wget nasm yasm \
  libgtk-3-dev clang libxcb-randr0-dev libxdo-dev \
  libxfixes-dev libxcb-shape0-dev libxcb-xfixes0-dev \
  libasound2-dev libpulse-dev cmake

# Сборка
git clone https://github.com/x6ta/udalenka.git
cd udalenka
cargo build --release
```

## Лицензия

AGPLv3 — см. [LICENSE](LICENSE)

## Благодарности

Основано на [RustDesk](https://github.com/rustdesk/rustdesk) — отличном open-source проекте удалённого рабочего стола.
