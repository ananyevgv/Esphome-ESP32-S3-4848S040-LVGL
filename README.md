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
  button4: !include
    file: packages/display/button-4.yaml
    vars:
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
  button6: !include
    file: packages/display/button-6.yaml
    vars:
      # Кнопки 0 ряд !!!!!!! ИКОНКИ НЕ ДОЛЖНЫ повторятся !!!!!!!!!!
        button6_icon_0_0: "\U000F18DE" # ceiling_light_multiple_outline
        button6_entity_0_0: light.holl_led_0
        button6_text_0_0: "Кухня низ"
        
        button6_icon_0_1: "󱊺" #string_lights
        button6_entity_0_1: light.holl_led_1
        button6_text_0_1: "Кухня верх"
        
        
      # Кнопки 1 ряд
        button6_icon_1_0: "󱞓" #chandelier
        button6_entity_1_0: light.holl_led_4
      
        button6_icon_1_1: "󰠠" #lightning_bolt_circle
        button6_entity_1_1: light.holl_led_5
        
      
        button6_icon_1_2: "󱇜" #window_open_variant
        button6_entity_1_2: light.holl_led_6
      
        button6_icon_1_3: "󰣳" #nas
        button6_entity_1_3: light.holl_led_7
  
  
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
