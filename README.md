# Esphome-ESP32-S3-4848S040-LVGL  quickly create your own pages

# TO-DO draw polygon in LVGL

kitchen-lighting.yaml указываем свои сенсоры, первоначальную страницу, фон для страниц 

создаем папку packages в esphome, копируем нужные пакеты в папку


Раставиляем страницы в желаемой очередности, barometr и  weather можно использовать 1 экземпляр
```yaml
packages:
# Раставить страницы в желаемой очередности, weather  и barometr можно использовать 1 вариант
смотри packages.yaml

```

|  1                                                         | 2                                                         | 
|------------------------------------------------------------|-----------------------------------------------------------|
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather_anime.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/boiler.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/termostat.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/bar.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/clock.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/uv.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/geo.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/uv2.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/geomag2.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/birch.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/grass.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/ragweed.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/wind.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/humm2.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/lg.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/kith.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/holl.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/but4.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/but6.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/but12.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/but16.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/sl-4g.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/sl-4v.jpg) | 

https://aliexpress.ru/item/1005006335587633.html

https://github.com/Limych/ha-gismeteo

https://community.home-assistant.io/t/guition-4-480x480-esp32-s3-4848s040-smart-display-with-lvgl/729271

https://github.com/albert-canfield/HA-panel-esphome

https://github.com/GlennGoddard/CanvasGaugeBackgrounds

# Weather_anime позаимствован от сюда, картинки там же
https://github.com/alaltitov/display
