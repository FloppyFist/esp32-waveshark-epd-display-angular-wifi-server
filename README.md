# Esp32 Waveshark Epd Display Angular Wifi Server
Picture frame for Waveshark's [Esp32 driver board](https://www.waveshare.com/product/displays/accessories/driver-boards/e-paper-esp32-driver-board.htm) & epd display utilizing Arduino IDE & Angular

## Developer Setup
Sometimes it is not easy for beginners to set up all of this, hence a detailed description.

### Arduino IDE
* Install the [Arduino IDE](https://www.arduino.cc/en/Main/Software)
* Install Esp board libs in the Arduino IDE's board manager
  * Add this at ```File > Preferences > Additional Board Manager URLs```
    ```
    https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
    ```
  * Go to ```Tools > Board: xxx > Board Manager```
  * Scroll down & install 'esp32'.
  * This will take ages. Go get a drink or something. Visit friends in Paris. Write a postcard.
* Clone this repo inside your Arduino folder, usually ```C:\Users\<username>\Documents\Arduino\``` on Windows
* Use Arduino IDE to install all [Arduino dependencies](#arduino-ide-dependencies). Manually that is:
  * Download all libs from the linked repos (.zip)
  * In Arduino IDE: ```Sketch > Include Library > Add .ZIP Library```
  * Now the libs will be found when building

### Angular
* Install newest LTS Version of node.js from [here](https://nodejs.org/en/)
* Install [VSCode](https://code.visualstudio.com/) or your preferred editor
  * Cool VSCode extensions for angular:
    * [Angular Extension Pack](https://marketplace.visualstudio.com/items?itemName=loiane.angular-extension-pack) - that's an all in one bundle
    * [i18n Ally](https://marketplace.visualstudio.com/items?itemName=antfu.i18n-ally) for translation management
* Install Angular CLI: Open the ```src/angular``` folder with VSCode and go into a terminal with ```ctrl + j``` and enter
  ```
  npm install -g @angular/cli
  ```
* Install all dependencies for the angular project
  ```
  npm install
  ```
* If commands are failing because ```'ng.ps1 cannot be loaded because 
running scripts is disabled on this system'```, run 
  ```
  Set-ExecutionPolicy Unrestricted -Scope CurrentUser
  ```

### Local config files

Create a file ```src/arduino/epd_server/local_dev_config.h``` and fill with settings as follows.
```
#define wifiSettings

const char* ssid = "Your Wifi Name";
const char* password = "Your Wifi Password";
```

## Build
### Angular
### Arduino / Esp32

## Dependencies
### Arduino IDE Dependencies
* [GxEPD2](https://github.com/ZinggJM/GxEPD2) Waveshare lib for epd displays
* [Adafruit GFX](https://github.com/adafruit/Adafruit-GFX-Library) - can be found in lib manager to auto-install

### Angular Dependencies
See package.json for details on the angular dependencies.