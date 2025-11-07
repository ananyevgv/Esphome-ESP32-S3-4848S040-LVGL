# Esphome-ESP32-S3-4848S040-LVGL  quickly create your own pages

https://aliexpress.ru/item/1005008214872438.html

[![License][license-shield]][license]
[![ESPHome release][esphome-release-shield]][esphome-release]

[license-shield]: https://img.shields.io/static/v1?label=License&message=MIT&color=orange&logo=license
[license]: https://opensource.org/licenses/MIT
[esphome-release-shield]: https://img.shields.io/static/v1?label=ESPHome&message=2025.10.4&color=green&logo=esphome
[esphome-release]: https://GitHub.com/esphome/esphome/releases/

# Базовый конфиг 

holl-informer.yaml 

создаем папку packages в esphome, копируем нужные пакеты в папку , указываем первоначальную страницу, фон для страниц 

# основная страница

    file:packages/display/weather_anime.yaml или weather.yaml

# выбираем количество кнопок

    file: packages/display/dis_butt_x.yaml 
указываем иконки и id страниц

# добавляем необходимые сенсоры на основной экран + дополнительная страница сенсора

    file:packages/display/dishwasher.yaml или washing.yaml
    file: packages/display/barometr_page.yaml или file: packages/display/barometr.yaml 
    file: packages/display/thermometer.yaml
    file: packages/display/humm-out.yaml
    file: packages/display/geomag.yaml
    file: packages/display/UV.yaml
    file: packages/display/wind.yaml 
    file: packages/display/iaq.yaml
    file: packages/display/co2.yaml
    file: packages/display/voc.yaml
    file: packages/display/birch.yaml
    file: packages/display/grass.yaml
    file: packages/display/ragweed.yaml
    file: packages/display/humm.yaml
    file: packages/display/thermostat.yaml или file: packages/display/boiler.yaml
    file: packages/display/clock_page.yaml (указываем необходимость отображения даты)
    
    file: packages/display/door_bell.yaml (требует много ресурсов, при большом количестве страниц может не запустится)
    Этот компонент требует достаточного объема оперативной памяти как для загрузки изображения, так и для хранения декодированного изображения.
    
Раставляем страницы в желаемой последовательности
на главную страницу сенсоры добавляются автоматически при добавлении пакета

# Добавляем прочие страницы

    file: packages/display/button-x.yaml
    file: packages/display/shutter-x.yaml
    file: packages/display/slider-4x.yaml
указываем свои сущности("light.toggle" "switch.toggle" "button.press), типы действия

# Страница пульта ТВ LG

    file: packages/display/lg_light.yaml 

указываем свои коды и иконки (при необходимости поменять в скрипте тип команд)

# Основной слой, стиль, блокировка экрана 

    top:  !include packages/display/top_stl_blk.yaml  без блокировки top:  !include packages/display/top_stl.yam

# Обязательные пакеты    
     wifi: !include packages/display/wifi.yaml
     disp:  !include packages/display/display.yaml

# Страничка настроек 

    settings: !include packages/display/settings.yaml 

разворот экрана пока не работает

# Веб морда при необходимости
    web: !include included/web.yaml

# font

[MaterialDesign-Webfont](https://github.com/Templarian/MaterialDesign-Webfont/tree/master/fonts)

[DSEG](https://github.com/keshikan/DSEG/tree/master/src)

[icons](https://github.com/alaltitov/Guition-ESP32-S3-4848S040/blob/dev/src/assets/fonts)

# TODO 

BME680, rotation display, weather page, graph page, vacuum  page


# примеры смотри holl-informer.yaml и packages.yaml

|                                               |                                                 |                                                   |                                                 | 
|-----------------------------------------------|-------------------------------------------------|---------------------------------------------------|-------------------------------------------------|
|  ![1](./img/thermometer.jpg) | ![2](./img/weather.jpg) | ![3](./img/weather_anime.jpg) | ![4](./img/washing.jpg) |
|  ![1](./img/boiler.jpg) | ![2](./img/termostat.jpg) |  ![3](./img/bar.jpg) | ![4](./img/clock.jpg) | 
| ![1](./img/dishwasher.jpg) | ![2](./img/shutter4.jpg) | ![3](./img/uv2.jpg) | ![4](./img/geomag2.jpg) | 
|  ![1](./img/birch.jpg) | ![2](./img/grass.jpg) | ![3](./img/ragweed.jpg) | ![4](./img/wind.jpg) | 
|  ![1](./img/humm2.jpg) | ![2](./img/lg.jpg) | ![3](./img/kith.jpg) | ![4](./img/holl.jpg) | 
|  ![1](./img/but4.jpg) | ![2](./img/but6.jpg) | ![3](./img/but12.jpg) | ![4](./img/but16.jpg) | 
|  ![1](./img/sl-4g.jpg) | ![2](./img/sl-4v.jpg) | ![3](./img/shutter.jpg)| ![4](./img/shutter2.png) |


https://aliexpress.ru/item/1005006335587633.html

https://github.com/Limych/ha-gismeteo

https://community.home-assistant.io/t/guition-4-480x480-esp32-s3-4848s040-smart-display-with-lvgl/729271

https://github.com/albert-canfield/HA-panel-esphome

https://github.com/GlennGoddard/CanvasGaugeBackgrounds

