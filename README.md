# Protogen

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa]. 

In short, you can build your own projects using information provided in this repository, but you have to **provide attribution to this repository** and you **can not sell your work** based on this repository for profit.

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg



## BOM

- ESP32 [ESP32](https://dratek.cz/arduino/1581-esp-32s-esp32-esp8266-development-board-2.4ghz-dual-mode-wifi-bluetooth-antenna-module.html)
- 2x 16x16 Neopixel-compatible displays
- battery holder [SBH-341-1AS držák baterie 4xAA](https://www.gme.cz/v/1506924/sbh-341-1as-drzak-baterie-4xaa)
- 2x 470uF / 5+V capacitors [HITANO CE 470u/25VIT](https://www.gme.cz/v/1485865/hitano-ce-470u-25vit-hit-exr-10x16-rm5-bulk-elektrolyticky-kondenzator)
- 3.3V to 5V logic converter [IIC I2C 5V to 3.3V](https://dratek.cz/arduino/1481-iic-i2c-5v-na-3.3v-obousmerny-prevodnik-logicke-urovne.html)
- 2x 5V fan
- 1N4007 diode (or equivalent)
- The rest of the protogen

## Kavex Part's List 
- ESP32: https://www.aliexpress.us/item/3256806150650156.html
- 2x 16x16 Neopixel-compatible displays: https://www.aliexpress.us/item/3256805063710566.html
- battery holder: https://www.aliexpress.us/item/3256805831102887.html
- 3.3V to 5V logic converter: https://www.aliexpress.us/item/3256805798457379.html
- 1N4007 diode: https://www.aliexpress.us/item/3256805817433207.html
- 470UF 25V 8*12 Aluminum electrolytic capacitor: https://www.aliexpress.us/item/3256805759406524.html
- 5V fans: https://www.aliexpress.us/item/3256803185681643.html
- Dupont Line: https://www.aliexpress.us/item/3256806675662297.html
- M3 304 Stainless Steel Hex Hexagon Socket Screw: https://www.aliexpress.us/item/2255801159169965.html
- 3D Printed Parts: https://www.thingiverse.com/thing:6018991
- PLA: https://www.amazon.com/gp/product/B07ZNHF46J/

![proto](https://user-images.githubusercontent.com/8028882/236701038-a80ce5f3-3012-4528-be68-1b71acf7782d.gif)

## Diagram
![diagram](https://github.com/kiraacorsac/protogen/assets/8028882/d177aa28-e766-4fdc-973f-950d4ff4e7b6)



## Frimware

- Set up `config.h`
  - Set or unset DEBUG flag as needed
  - Make sure brightness is set on a reasonable level depending on power source (high brightness may fry components if current routed through ESP)
  - Make sure WiFi name and password is set correctly

# Tooling

## Control center (protogen-phone-control)
    npm install
    npm run build
    
![photo_2023-05-07_22-11-10](https://user-images.githubusercontent.com/8028882/236700550-8f14f148-c867-41c7-8a31-d43c892e0fd3.jpg)

## Animation generator (animation-generator)
    .\env\Scripts\activate.bat
    pip install -r requirements.txt
    python img-to-str.py ./test-animations/smile
    
Then you need to manually create animation library from the outputs (see `temp.json`), minimize it and put the string in animationBookJson[] in `AnimationBook.h`. 
