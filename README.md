# ESP32_anything_nano
A very small development board for any projects, based on ESP32S3.  
Single board weight = 5g.  

![Image](/doc/pin_no.jpg)  

| Module Pin No. | ESP32 Net Name | Function | 
|---------|--------------|-----------|
|1| GPIO1 | RTC_GPIO1, GPIO1, TOUCH1, ADC1_CH0 |
|2| GPIO2 | RTC_GPIO2, GPIO2, TOUCH2, ADC1_CH1 |
|3| GPIO42 | MTMS, GPIO42 |
|4| GPIO41 | MTDI, GPIO41, CLK_OUT1 |
|5| GPIO40 | MTDO, GPIO40, CLK_OUT2 |
|6| GPIO39 | MTCK, GPIO39, CLK_OUT3, SUBSPICS1 |
|7| GPIO38 | GPIO38, FSPIWP, SUBSPIWP |
|8| GPIO45 | GPIO45 |
|9| GPIO48 | SPICLK_N_DIFF,GPIO48, SUBSPICLK_N_DIFF |
|10| GPIO47 | SPICLK_P_DIFF,GPIO47, SUBSPICLK_P_DIFF |
|11| VMAIN | Main Voltage in/out pin. Recommended Input Voltage: 2-16V (max. 2A). If output: voltage from USB port, max 1A|
|12| EN | On/Off pin of the module, pull to ground to switch off (default 100kΩ pullup) |
|13| 3V3 | 3V3 output pin, max 500mA, for external sensors / reference voltage |
|14| GND | Ground pin, must be connected to external components |
|15| GPIO3 | RTC_GPIO3, GPIO3, TOUCH3, ADC1_CH2 |
|16| GPIO46 | GPIO46 |
|17| GPIO14 | RTC_GPIO14, GPIO14, TOUCH14, ADC2_CH3, FSPIWP, FSPIDQS, SUBSPIWP |
|18| GPIO21 | RTC_GPIO21, GPIO21 |
|19| RX | U0RXD, GPIO44, CLK_OUT2 |
|20| TX | U0TXD, GPIO43, CLK_OUT1 |

Warning!!! Do not input voltage above 3.6V input signal pins (basically all pins except VMAIN).  

Most digital function in ESP32 can be mapped to any GPIO pins (some functions may be limited to some group of GPIOs).  
Programming guides can be found in  
<https://docs.espressif.com/projects/esp-idf/en/v4.4/esp32s3/api-reference/peripherals/index.html>.  
Only GPIO1-20 have ADC ability, in this board, only pin1, 2, 15, 17 are connected to ADC (GPIO 1, 2, 3, 14)  
This config is sub-optimal but to align with the pinout of ESP32S3-eye (original board from expressif) so that most opensource projects can be directly migrated.  

Using GPIO43 and GPIO44 for UART is preferred but not necessary. All GPIOs can be mapped to UART.   

Programming environment setup:  
There exist many methods to program the ESP32 core. Here is a simplest one using Arduino IDE:  
<https://espressif-docs.readthedocs-hosted.com/projects/arduino-esp32/en/latest/installing.html>  

Into flash mode:  
Connect the board to computer via the usb-c connector.  
Press and hold the Download (DL) button.  
Then press and release the reset (RST) button.  
Finally release the Download button.  


