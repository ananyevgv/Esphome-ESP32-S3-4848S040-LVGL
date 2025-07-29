# Esphome-ESP32-S3-4848S040-LVGL  quickly create your own pages

https://aliexpress.ru/item/1005008214872438.html

[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2025.7.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

Добавлен BME680 и IR_LED и выбор сущности "light.toggle" "switch.toggle" "button.press"

kitchen-lighting.yaml указываем свои сенсоры, первоначальную страницу, фон для страниц 

создаем папку packages в esphome, копируем нужные пакеты в папку


Раставиляем страницы в желаемой очередности, barometr и  weather можно использовать 1 экземпляр

# смотри packages.yaml

```yaml
packages:
# Раставить страницы в желаемой очередности, weather  и barometr можно использовать 1 вариант

#############################################################################
#----Страничка погоды-----------------------------------------------------
#############################################################################
# Раставить страницы в желаемой очередности, barometr можно использовать 1 вариант
  #weather: !include packages/weather_anime.yaml # выбрать один из трех weather #jpg:3 689 528 байт без 2 603 377 байт
  weather: !include 
    file: packages/weather.yaml # выбрать один из трех weather
    vars:
      sensor_temperature: sensor.kitchen_t
      sensor_humidity: sensor.kitchen_humidity
      sensor_pressure: sensor.iaroslavskaia_pressure
      sensor_co2: sensor.holl_co2
      sensor_weather: weather.iaroslavskaia
      sensor_iaq: sensor.holl_iaq
      sensor_iaq_c: sensor.holl_iaq_classification
      sensor_voc: sensor.holl_voc
      sensor_lux: sensor.holl_p

      sensor_uv_index: sensor.iaroslavskaia_uv_index
      sensor_geomagnetic: sensor.iaroslavskaia_geomagnetic_field
      sensor_wind_speed: sensor.iaroslavskaia_wind_speed
      sensor_birch: sensor.iaroslavskaia_birch_pollen_index
      sensor_grass: sensor.iaroslavskaia_grass_pollen_index
      sensor_ragweed: sensor.iaroslavskaia_ragweed_pollen_index
      sensor_wind_bearing: sensor.iaroslavskaia_wind_bearing_2

  #weather: !include packages/weather_bme680.yaml # выбрать один из трех обязателен barometr_bme680_weather.yaml

#############################################################################
#----Часы----------------------------------------------------------
#############################################################################
  clock: !include packages/clock_page.yaml
  
#############################################################################
#----Страничка 4 кнопоки-----------------------------------------------------
#############################################################################
  button4: !include
    file: packages/button-4.yaml
    vars:
      background_button4: back6
      # !!!!!!! ИКОНКИ НЕ ДОЛЖНЫ повторятся !!!!!!!!!!
      button4_icon_0_0: "\U000F18DE" # ceiling_light_multiple_outline
      button4_icon_0_1: "󱊺" #string_lights
      button4_icon_1_0: "󰯪" #alarm_light_on
      button4_icon_1_1: "󱠝" #countertop_outline

      button4_entity_0_0: light.holl_led_0
      button4_entity_0_1: light.holl_led_1
      button4_entity_1_0: light.holl_led_2
      button4_entity_1_1: light.holl_led_3

      button4_text_0_0: "Кухня низ"
      button4_text_0_1: "Кухня верх"
      button4_text_1_0: "Холл низ"
      button4_text_1_1: "Холл верх"

      button4_action_0_0: "light.toggle"  # "switch.toggle" "button.press"
      button4_action_0_1: "light.toggle"  # "switch.toggle" "button.press"
      button4_action_1_0: "light.toggle"  # "switch.toggle" "button.press"
      button4_action_1_1: "light.toggle"  # "switch.toggle" "button.press"
        
      button4_checkable_0_0: "true" # light, switch. button"false"
      button4_checkable_0_1: "true" # light, switch. button"false"
      button4_checkable_1_0: "true" # light, switch. button"false"
      button4_checkable_1_1: "true" # light, switch. button"false"


```

|  1                                                         | 2                                                         | 
|------------------------------------------------------------|-----------------------------------------------------------|
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/bme680.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/board.jpg) |
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
