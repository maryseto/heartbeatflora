# heartbeatflora
wearable vibrating electronic 

Electronic code

//  drv.setWaveform(0, 84);  // ramp up medium 1, see datasheet part 11.2
//  drv.setWaveform(1, 1);  // strong click 100%, see datasheet part 11.2

#include <Wire.h>
#include "Adafruit_DRV2605.h"

Adafruit_DRV2605 drv;

void setup() {
  Serial.begin(1200);
  drv.begin();
    

  drv.setWaveform(0, 27);   // Short Double Click Strong 1 - 100%
  
  
  drv.setWaveform(1, 0);  // end of waveforms

}

void loop() {
    
    delay(1200);
    drv.go();
}
