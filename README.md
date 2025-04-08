## 📦 ARM64 Static Build of udp2raw

➡️ [Download latest release](https://github.com/ae1897/udp2raw/releases/download/v2025.04.08-arm64/udp2raw) — statically compiled binary for Keenetic and other ARM64 (aarch64) devices.

---

### 🧾 What is this?

This is a **statically linked binary** of [`udp2raw`](https://github.com/wangyu-/udp2raw-tunnel), built for **ARM64 (aarch64)** architecture.  
It works out of the box on devices like:

- 🛜 **Keenetic KN-2710** routers  
- ☁️ **Ubuntu 22.04 ARM64 VPS**  
- 🧩 Other Linux ARM64-based devices (e.g. SBCs, embedded)

Perfect for **WireGuard traffic obfuscation**: bypass DPI, censorship, throttling.  
Supports `faketcp`, `udp`, `icmp` modes.

---

### 💾 File Info

- **File:** `udp2raw`  
- **Size:** 5.9 MB  
- **SHA256:** `18cab4a9b2eb67b4f8c807d0113ce8518735c6260bbc41d9913ce695da70c2b6`  
- **MD5:** `c9afe63d0e3ceb21cf4f0f4cb7229b1a`  

---

### ⚙️ Example usage

Client (on router):
```bash
/opt/udp2raw -c -l 127.0.0.1:1090 -r <SERVER_IP>:443 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

Server (on VPS):
```bash
udp2raw -s -l 0.0.0.0:443 -r 127.0.0.1:51820 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

---

## 🇷🇺 Описание на русском

Готовый бинарник `udp2raw` под архитектуру **ARM64 (aarch64)**. Скомпилирован **статически**, не требует внешних библиотек.

📌 Подходит для:
- роутеров **Keenetic KN-2710** (Linux aarch64 + BusyBox)
- VPS с **Ubuntu 22.04 ARM64**
- любых устройств с Linux на ARMv8 (64-бит)

🛡 Используется для **обфускации трафика WireGuard** (обход DPI, фильтрации). Поддерживает режимы: `faketcp`, `udp`, `icmp`.

---

### 📂 Информация о файле

- **Имя:** `udp2raw`  
- **Размер:** 5.9 МБ  
- **SHA256:** `18cab4a9b2eb67b4f8c807d0113ce8518735c6260bbc41d9913ce695da70c2b6`  
- **MD5:** `c9afe63d0e3ceb21cf4f0f4cb7229b1a`  

---

### 🛠 Примеры запуска

**Клиент (роутер):**
```bash
/opt/udp2raw -c -l 127.0.0.1:1090 -r <IP_сервера>:443 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

**Сервер (на VPS):**
```bash
udp2raw -s -l 0.0.0.0:443 -r 127.0.0.1:51820 --raw-mode faketcp -k radioactive --cipher-mode xor --auth-mode simple
```

---

🧩 Based on: [wangyu-/udp2raw-tunnel](https://github.com/wangyu-/udp2raw-tunnel)  
Built with ❤️ for the community.
