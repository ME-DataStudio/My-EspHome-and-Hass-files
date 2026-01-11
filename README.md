So i wanted an epaper display showing random pictures and thought it would be an easy job seeing the examples on the web. Well it turned out the be a frustating job for me as i wanted to use my HAOS server as the server to deliver pictures and an eink display with ESP32 and battery powered. Given these requirements HASS with ESPhome seemed a logical choice.

So i bought an waveshare eink 4.37inch 4 clour display which in hindsight wasn't a smart buy because it was not supported in the display component of ESPhome. So i have modified the waveshare epaper component (which you can find overhere (esphome-configs/um-feathers3/my_components/waveshare_epaper).

My ESP32 is a S3 from unexpected maker. I selected it after reading https://github.com/charnley/eink-art-gallery, which was the basis for my project and https://github.com/usetrmnl. I needed an ESP32 with enough PSRAM is what took from those projects.

After setting up my ESP32 with eink and building ESPhome with the config in https://github.com/ME-DataStudio/My-EspHome-and-Hass-files/tree/main/esphome-configs/um-feathers3 (including the modified waveshare-epaper component) i started on the HASS side of it all. And there it got complicated. How to let HASS push a picture to ESPhome device? I build the canvas_coordinator from Charnly's github (after having trouble to get the Dockerfile correct and getting WSL and Docker running on Windows), but when starting the docker image i get an assertion error about storage.

So next step i looked at some eink dashboards, but soon realized that they all gather data from sensors and display that. So a pull in stead of a push from HASS. SO now looking for a way to get the ESP32 pull an image from HASS.

Work in progress... (11-1-2026)
