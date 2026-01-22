So i wanted an epaper display showing random pictures and thought it would be an easy job seeing the examples on the web. Well it turned out the be a frustating job for me as i wanted to use my HAOS server as the server to deliver pictures and an eink display with ESP32 and battery powered. Given these requirements HASS with ESPhome seemed a logical choice.

So i bought an waveshare eink 4.37inch(G) 4 colour display which in hindsight wasn't a smart buy because it was not supported in the display component of ESPhome. So i had to modify the waveshare epaper component (which you can find overhere (esphome-configs/um-feathers3/my_components/waveshare_epaper).

My ESP32 is a S3 from unexpected maker. I selected it after reading https://github.com/charnley/eink-art-gallery, which was the basis for my project and https://github.com/usetrmnl. I needed an ESP32 with enough PSRAM is what took from those projects.

After setting up my ESP32 with eink and building ESPhome with the config in https://github.com/ME-DataStudio/My-EspHome-and-Hass-files/tree/main/esphome-configs/um-feathers3 (including the modified waveshare-epaper component) i started on the HASS side of it all. And there it got complicated. How to let HASS push a picture to ESPhome device? I build the canvas_coordinator from Charnly's github (https://github.com/charnley/eink-art-gallery). At first I did not get it installed into HASS but after some tips from Charnly (see issue on his github) and searching on internet why port 22 was not open on HAOS installation (because of add-on Terminal&SSH) i got it working.

So now the only thing i have to do is add the dsiplay as an ESPhome component. I added the display as a type c, because it isn't using the HAT from waveshare but it is delivered with it's own driver board behind the display. It got the needed commands from the example arduino code (i hope i got it right). Now i'm finetuning and finding a way to get 4 colours.

