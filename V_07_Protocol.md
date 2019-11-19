# Session 7 
## How to install IOTempower in Linux
1. Install IOTempower onto an SD card
2. Set up Pi
3. Connect to the Pi
4. Open the Pi’s IP in a browser
5. Use cloudcmd to interact with the Pi

## Where are the tools/scripts? 
After starting the iot/run command they are in the main IOTempower directory.

## Where is documentation?
In addition to the GitHub documentation, there are some examples of IOTempower in use on ulno.net. 
There are videos on YouTube and a Facebook group for any extra questions. 

## What is the role of the different folders in lib/node_types?
* Esp32 support
* Capacitive touch support
* servo/pwm on esp32 and esp8266
* esp32 d1 mini kit support
* Menu shortcuts
* nodemcu support
* pre_flash directory
* esp8266 support
* esp32 support
* sonoff pow support
* d1 mini support

## which topic needs to be called with what to switch on the coffee machine?
Coffee-machine: switch(1)

## set all lights in living room to blue?
living_room: leds1(#0000FF) / leds2(#0000FF)

## turn the main power off?
main: switch(0)

## what is the general rule for forming topics in IoTempower?


## When does it make sense to change something in system.conf?




##LoRa

### What is the relation bandwidth/range/power? What is the link budget?
Low power wide area network, high bandwidth (—> high capacity)

### What is the community approach?
Deploy LoRa networks, buy a contract, use the infrastructure

### What are benefits with LORA?
Many devices can be connected

### What are problems with LORA?
Slow, simplex mode communication

### Google link budget again: what is it exactly , find examples
accounting of all of the gains and losses from a transmitter
e.g. Transmitter Antenna Gain, Transmitter Loss

### Google "radio link budget calculator”. Do 2 calculations for LoRa and WiFi.
LoRa: Transmit power = 17dBm, Sensitivity = -137 dBm —> -120 dBm Output

### Google: LORA in Austria and Linz. – What activities exist
Lower Austria is certified, activities include meetings, workshops
Linz: 4 gateways, 9 contributors

### Google how expensive a LORA client adapter, LORA gateway (or gateway adapter is)
USB adapter: 64€, gateway: 223€

### Check LORA's software support (and licenses for the respective libraries)
Ex: Actility, IOTLABS, mQCentral
LoRa Arduino library: MIT license

### Discuss with neighbor:
### What is Lora good for, what might it be bad at? – What are its advantages/short comings?
Good: good coverage, low power usage 
Bad: slow, not good for real-time applications

### How does it fit into IoT?
Connect different devices over large areas, used to send data between these devices