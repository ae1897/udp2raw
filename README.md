## 🇬🇧 English Description

**Precompiled binary of `udp2raw` for ARM64 (aarch64) architecture.**  
Statically compiled — no external libraries required. Suitable for routers and embedded devices running Linux on ARMv8 (e.g., Keenetic KN-2710).

**Purpose:** traffic obfuscation for WireGuard VPN to bypass DPI and firewalls.  
Supports `faketcp`, `udp`, and `icmp` raw modes.  
Ideal for combining with WireGuard on ARM-based routers.

**File size:** 5.9 MB  
**SHA256:** `18cab4a9b2eb67b4f8c807d0113ce8518735c6260bbc41d9913ce695da70c2b6`  
**MD5:** `c9afe63d0e3ceb21cf4f0f4cb7229b1a`

### 🔧 Example: client mode
```bash
/opt/udp2raw -c -l 127.0.0.1:1090 -r <server_ip>:443 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

### 🔧 Example: server mode
```bash
udp2raw -s -l 0.0.0.0:443 -r 127.0.0.1:51820 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

✅ Tested on **Ubuntu 22.04 ARM64** and **Keenetic KN-2710 (BusyBox + Linux 4.9)**  
Runs out of the box.

---

## 🇷🇺 Описание на русском

**Готовый бинарник `udp2raw` под архитектуру ARM64 (aarch64).**  
Скомпилирован статически, не требует внешних библиотек. Подходит для маршрутизаторов на ARMv8, например **Keenetic KN-2710**, а также других систем с Linux на архитектуре **aarch64**.

**Назначение:** обфускация WireGuard-трафика для обхода DPI и фильтрации.  
Поддерживаются режимы `faketcp`, `udp`, `icmp`. Удобно использовать в связке с WireGuard на роутерах.

**Размер файла:** 5.9 МБ  
**SHA256:** `18cab4a9b2eb67b4f8c807d0113ce8518735c6260bbc41d9913ce695da70c2b6`  
**MD5:** `c9afe63d0e3ceb21cf4f0f4cb7229b1a`

### 🔧 Пример запуска клиента
```bash
/opt/udp2raw -c -l 127.0.0.1:1090 -r <IP_сервера>:443 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

### 🔧 Пример запуска сервера
```bash
udp2raw -s -l 0.0.0.0:443 -r 127.0.0.1:51820 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

✅ Проверено на **Ubuntu 22.04 ARM64** и **Keenetic KN-2710 (BusyBox + Linux 4.9)**  
Работает «из коробки».
