[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2026.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

<div align="center">
  <h1>🖥️ ESP32-S3-4848S040-LVGL</h1>
  <p><strong>Быстрое создание своих страниц для дисплея ESP32-S3</strong></p>
  
  <a href="https://aliexpress.ru/item/1005008214872438.html">
    <img src="https://img.shields.io/badge/Купить%20на-AliExpress-orange?style=for-the-badge&logo=aliexpress" alt="AliExpress">
  </a>
</div>

> ⚠️ **Важно**: Перед прошивкой на ESPHome обязательно посмотрите LOG устройства и сделайте **резервную копию (backup)**.

---

## 📌 Ссылки на устройство

| Платформа | Ссылка |
|-----------|--------|
| 🌐 AliExpress | [ESP32-S3-4848S040](https://aliexpress.ru/item/1005008214872438.html) |
| 📖 Обсуждение | [Home Assistant Community](https://community.home-assistant.io/t/guition-4-480x480-esp32-s3-4848s040-smart-display-with-lvgl/729271) |

---

## 🚀 Быстрый старт

### 1. Базовый конфиг

Используйте файл **`holl-informer.yaml`** как основу.

### 2. Создайте структуру папок

```bash
esphome/
└── packages/
    └── display/
        └── (скопируйте нужные пакеты)