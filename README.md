# Where is Chabis - The ChaBox


## Initial plans
The following is a documentation of the process and functionality of the ChaBox, a Pi4 with functionality useful to myself, initially starting as a GPS and weather station sending information to the web using wifi over 4G.

I would like this Pi to act as a gateway between a myriad of projects; I want it to be used for as much as possible, call it curiosity.
Originally I wished to make a low power device that every 2-4 hours would ping GPS information to a web server using 4G, but going for something at a higher level with a higher power draw allows significantly more flexibility and adaptability: 

*Why can't it do everything?*

I need storage. I need FTP and Portability at the same time. I need a web server. I need GPS functionality. I need weather information. I need a portable desktop. I need _this_ funny little project.

---
## Initial Parts
**The parts provided for this project initially include:**
- 1 x Pi4 B 4Gb
- 1 x CE06586 Argon ONE V2 Pi 4 case (awesome Pi case)
- 1 x SEN-10988 Temperature sensor
- 1 x WRL-17146-WiFi module - ESP8266 4MB
- 1 x SEN0375-BME680 Environmental Sensor module 
- 1 x ADA3133 Adafruit ultimate gps featherwing
---
### Current Issues
- The ADA3133 will work directly with the Pi4, on pins 08 and 10 (plus power and other shit). A bigger issue is ESP8266; What can I use this for. The Pi4 has onboard wireless, BUT the ESP8266 is significantly lower power; If I can find a way to low-power the Pi, so the OS runs at a minimum (less than sleep) but power GPIO fully this should be perfect (sometimes dumb is fun, but also I plan on using this project in places where I can not frequently charge a battery, so low power is better really).
    - as an aside, I have no clue wether or not the Pi can power the ESP8266; It takes 3V and does not have variable voltage logic. [I don't know though, maybe PWM?](https://community.element14.com/products/raspberry-pi/w/documents/4317/raspberry-pi-4-model-b-default-gpio-pinout-with-poe-header)
- The Argon case provides access to the GPIOs, but the storage of the rest of the shit can't really just dangle off the Argon case. I'll super glue them together (that is a joke, I'll get to what I do with this later)
- Pi4 good, little computer in my pocket. I can now work from anywhere, and recent circumstances make it hard for me to carry even a laptop with me.
- SEN-10988 is easy as piss, I love these sensors. There's still an issue though; Although the Pi setup is (potentially) a prototype tool for a lower level MCU, this temperature sensor will sit in a bag whilst I travel, lest I situate the ChaBox externally and risk environmental factors. I think the Pi should have enough GPIO pins to not have to worry about that aspect.
---
## TODO
0. Investigate parts some more.
1. Get M.2 key B, and SD card. 
2. Flash em, stick em together.
3. Grab a breadboard and stick some shit together. See what barks, see what doesn't.
4. Basically a little bit of everything.

### This is in development, much is to be changed and updated