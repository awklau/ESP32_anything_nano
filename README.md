# ESP32_anaything_nano
A very small ESP32 development board for any projects

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
|11| VMAIN | Main Voltage in/out pin. Recommended Input Voltage: 2-16V. If output: voltage from USB port, max 1A|
|12| EN | On/Off pin of the module, pull to ground to switch off (default 100kΩ pullup) |
|13| 3V3 | 3V3 output pin, max 500mA, for external sensors / reference voltage |
|14| GND | Ground pin, must be connected to external components |
|15| GPIO3 | RTC_GPIO3, GPIO3, TOUCH3, ADC1_CH2 |
|16| GPIO46 | GPIO46 |
|17| GPIO14 | RTC_GPIO14, GPIO14, TOUCH14, ADC2_CH3, FSPIWP, FSPIDQS, SUBSPIWP |
|18| GPIO21 | RTC_GPIO21, GPIO21 |
|19| RX | U0RXD, GPIO44, CLK_OUT2 |
|20| TX | U0TXD, GPIO43, CLK_OUT1 |