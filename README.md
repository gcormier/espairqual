<img src=images/espairqual_v4.png width=400px />

# espairqual
espairqual is an ESP32 based [esphome](https://esphome.io/) interface for [PMSx003](https://esphome.io/components/sensor/pmsx003.html) and Panasonic NA-GCJA5 particulate matter (PM) sensors.



It offers a plug and play solution to integrate air quality monitoring with home assistant. It provides 5V to the sensor and 3.3V to the internal electronics.

It can be powered by USC-C, or, by a wider range of input voltages on the screw terminals. It was designed for 24VAC, but will likely work with a slightly broader range
of both AC and DC input voltages. The absolute maximum voltage for the switching regulator is 40VDC, which means up to around 28VAC. The minimum DC is approximately 9VDC.

The PCB will fit inside a Hammond 1593KBK case.

## Programming
The USB-C port can be used to program. The first time, the reset button must be held. After this, all subsequent programming does not require access to the button.

There is also a header for the typical serial flashing with GPIO0(9) and EN exposed. It follows my [eflashy32](https://github.com/gcormier/eflashy32) pinout.

## Panasonic SN-GCJA5
I revised the design and added support to esphome for the Panasonic sensor. While the PMS is a good sensor, I did receive one dead-on-arrival from Aliexpress. The panasonic sensor is cheaper, smaller, available from tier-1 distributors (eg. [Digikey](https://www.digikey.ca/en/products/detail/panasonic-electronic-components/SN-GCJA5/10443899)) and has a 5+ year life expectancy. It has internal compensation for the fan, photo diode and laser diode.

The connector is JST-GH (1.25mm) series.