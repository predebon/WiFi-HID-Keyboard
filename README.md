# Wi-Fi HID Keyboard 
#### Using STM32F1 and ESP8266

First, you will need to gather the components:
* Any STM32 (not tssop20) microcontroller board;
* Any ESP microcontroller board;

Yes, that simple.

In Cube, select the standard mouse HID from STM (RCC and USB configurations), add an USART (SPI if you are using NRF24L01) and your circuitary too if needed.

If you don't want to spend a significant time configuring the HID descriptors, just replace yours usbd_hid.c and .h from Middlewares\ST\STM32_USB_Device_Library\Class\HID folder for mine.

It's coded only the A to Z, a to z, 0 to 9, space and enter characters, if you want more keys, just go to the [HID Usage Tables PDF](http://www.usb.org/developers/hidpage/Hut1_12v2.pdf) under keyboard section and add your own commands.

For WiFi, I've been using a ESP01 in the standard AT firmware, if you are new to this microcontroller, please refer to my ESP8266.txt text.