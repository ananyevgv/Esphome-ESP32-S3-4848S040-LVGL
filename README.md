# Esphome-ESP32-S3-4848S040-LVGL  quickly create your own pages

# TO-DO draw polygon in LVGL

kitchen-lighting.yaml указываем свои сенсоры, первоначальную страницу, фон для страниц 




Раставиляем страницы в желаемой очередности, barometr и  weather можно использовать 1 экземпляр
```yaml
packages:
# Раставить страницы в желаемой очередности, weather  и barometr можно использовать 1 вариант
  #weather: !include packages/weather_anime.yaml # выбрать один из трех weather #jpg:3 689 528 байт без 2 603 377 байт
  weather: !include packages/weather.yaml # выбрать один из трех weather
  #weather: !include packages/weather_bme680.yaml # выбрать один из трех обязателен barometr_bme680_weather.yaml

# Универсальные необходимо выбрать свои сущности и иконки для их
  #button4: !include packages/button-4.yaml
  #button6: !include packages/button-6.yaml
  #button8: !include packages/button-8.yaml
  #button10: !include packages/button-10.yaml
  #button12: !include packages/button-12.yaml
  #button16: !include packages/button-16.yaml
  #slider4v: !include packages/slider-4v.yaml
  #slider4g: !include packages/slider-4g.yaml
  #slider4b: !include packages/slider-4b.yaml

  kitchen: !include packages/kitchen_light.yaml # 30 844
  holl: !include packages/holl_light.yaml # 29 420
  boiler: !include packages/boiler.yaml
  lg: !include packages/lg_light.yaml  #495 288
  termostat: !include packages/termostat.yaml
 # clock: !include packages/clock_page.yaml

# выбрать один из четырех barometr
  barometr: !include packages/barometr.yaml # выбрать один из четырех barometr
  #barometr: !include packages/barometr_page.yaml # выбрать один из четырех barometr
  #barometr: !include packages/barometr_bme680_page.yaml  # выбрать один из четырех barometr
  #barometr: !include packages/barometr_bme680_weather.yaml  # выбрать один из четырех barometr  
 

  geomag: !include packages/geomag.yaml
  #geomag: !include packages/geomag-page.yaml # Фоновый рисунок
  UV: !include packages/UV.yaml
  #UV: !include packages/UV-page.yaml # Фоновый рисунок
  wind: !include packages/wind.yaml 

  birch: !include packages/birch.yaml
  grass: !include packages/grass.yaml
  ragweed: !include packages/ragweed.yaml

```

|  1                                                         | 2                                                         | 
|------------------------------------------------------------|-----------------------------------------------------------|
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather_anime.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/boiler.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/termostat.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/bar.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/clock.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/uv.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/geo.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/humm.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/lg.jpg) | 
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
