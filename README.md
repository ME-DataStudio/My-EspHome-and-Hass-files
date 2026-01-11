So i wanted an epaper display showing random pictures and thought it would be an easy job seeing the examples on the web. Well it turned out the be a frustating job for me as i wanted to use my HAOS server as the server to deliver pictures and an eink display with ESP32 and battery powered. Given these requirements HASS with ESPhome seemed a logical choice.

So i bought an waveshare eink 4.37inch 4 clour display which in hindsight wasn't a smart buy because it was not supported in the display component of ESPhome. So i have modified the waveshare epaper component (which you can find overhere (esphome-configs/um-feathers3/my_components/waveshare_epaper).

My ESP32 is a S3 from unexpected maker. I selected it after reading https://github.com/charnley/eink-art-gallery. Which was the basis for my project.
