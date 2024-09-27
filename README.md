# Esphome-ESP32-S3-4848S040-LVGL  (module)


kitchen-lighting.yaml указываем свои сенсоры, первоначальную страницу, фон для страниц 

(!!!!!!!!!!!!!!!!!!фоновый рисунок занимает приблизительно 1МБ!!!!!!!!!!!!!!)


Раставиляем страницы в желаемой очередности, barometr и  weather можно использовать 1 экземпляр
```yaml
packages:
  weather: !include packages/weather_anime.yaml # выбрать один из двух weather 
  weather: !include packages/weather_light.yaml # выбрать один из двух weather
  button4: !include packages/button-4.yaml универсальный (указать в файле свои названия, свичи, выбрать иконки)
  button8: !include packages/button-8.yaml универсальный (указать в файле свои названия, свичи, выбрать иконки)
  button10: !include packages/button-10.yaml универсальный (указать в файле свои названия, свичи, выбрать иконки)
  button12: !include packages/button-12.yaml универсальный (указать в файле свои названия, свичи, выбрать иконки)
  button16: !include packages/button-16.yaml универсальный (указать в файле свои названия, свичи, выбрать иконки)
  slider4v: !include packages/slider-4v.yaml универсальный (в процессе)
  slider4g: !include packages/slider-4g.yaml универсальный (в процессе)
  kitchen: !include packages/kitchen_light.yaml # 30 844
  holl: !include packages/holl_light.yaml # 29 420
  lg: !include packages/lg_light.yaml  #495 288
  clock: !include packages/clock_page.yaml
  barometr: !include packages/barometr_page.yaml # выбрать один из двух barometr
  barometr: !include packages/barometr_bme680_page.yaml  # выбрать один из двух barometr
  geomag: !include packages/geomag_page.yaml
  UV: !include packages/UV_page.yaml
  humm: !include packages/humm-page.yaml
```

|  1                                                         | 2                                                         | 
|------------------------------------------------------------|-----------------------------------------------------------|
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather_anime.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/weather.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/bar.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/clock.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/uv.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/geo.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/humm.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/lg.jpg) | 
|  ![1](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/kith.jpg) | ![2](https://github.com/ananyevgv/Esphome-ESP32-S3-4848S040-LVGL/blob/main/img/holl.jpg) | 


https://aliexpress.ru/item/1005006335587633.html

https://community.home-assistant.io/t/guition-4-480x480-esp32-s3-4848s040-smart-display-with-lvgl/729271

https://github.com/albert-canfield/HA-panel-esphome

# Weather_anime позаимствован от сюда, картинки там же
https://github.com/alaltitov/display
