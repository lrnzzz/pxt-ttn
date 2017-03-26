# CustomBlock

A quick look at a custom block that can give ideas for a package of blocks needed

Reference:

* <https://github.com/ribbotson/MERL-Microbit/tree/Development/RN2483/source>
  * A reference based on Arduino implementation could also be used.
* Interfaces
  * <https://github.com/ribbotson/MERL-Microbit/blob/Development/RN2483/source/sodaq_RN2483.h>
* Implementation
  * <https://github.com/ribbotson/MERL-Microbit/blob/Development/RN2483/source/sodaq_RN2483.cpp>
* Other information, as string literals etc
  * "Feel the source Luke"

## Initialisation

From the interfaces, one can identify some of the parameters needed for TTN which could be created by reusing the definition of serial.redirect with addition of extra paramters. A parameter for the type of LoRaWAN module used is recommended: at the present time, RN2483 is used for disection.


* Basic Serial for target
  * define tx/rx pins
  * baud 57600
* Init of RN2483 with
  * Over The Air Activation (OTA) - preferred <https://www.thethingsnetwork.org/docs/devices/registration.html> 
    * `bool initOTA(const uint8_t devEUI[8], const uint8_t appEUI[8], const uint8_t appKey[16], bool adr = true);`
  * Activation By Personization (ABP) 
    * `bool initABP(const uint8_t devAddr[4], const uint8_t appSKey[16], const uint8_t nwkSKey[16], bool adr = true);`


