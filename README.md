# survive

so basically this is my custom hardware project called **survive** and I somehow managed to make a full circuit schematic for it without letting the magic smoke out (yet) B)

## what is this?
it's a compact IoT carrier board I'm building for tracking outdoor weather and environmental data. it uses a **Seeeduino XIAO ESP32-C3** hooked up to a bunch of I2C sensors so it can measure air quality, temperature, humidity, and light levels all on one small board.

check out the schematic image below to see how everything is wired up:

![Schematic](SCH_Schematic1_1-P1_2026-11-13%20(1).png)

## stuff used:
- **Seeeduino XIAO ESP32-C3** (`U2`) - the main brain of the board (connected via I2C on pins D4 and D5)
- **ENS161** (`U4`) - air quality sensor for checking gas / VOC levels
- **BH1750FVI-TR** (`U3`) - digital light sensor for measuring brightness
- **AHT20** (`U1`) - sensor for temperature and humidity
- **some tiny parts** - two 5.1kΩ pull-up resistors (`R1`, `R2`) for the I2C lines and a 100nF capacitor (`C1`) so the 3.3V power stays clean
- **EasyEDA** - for drawing wires, placing parts, and praying everything connects right

## what it can do:
- tracks temp, humidity, air quality, and light all at the same time
- super small and low-profile, so it's easy to put outside in a case
- all sensors share the same 3.3V I2C bus without messing each other up

## status
schematic is finished (now I just gotta route the PCB and solder it without burning anything)
