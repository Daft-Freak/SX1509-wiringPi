SX1509-wiringPi
===============

SX1509 support for Wiring Pi.
Based on code from [here](https://github.com/sparkfun/SX1509_IO-Expander/tree/master/Arduino/libraries/SX1509).

How to use
----------

Setup:
```
int sx1509Setup(
  const int pinBase,
  const int i2cAddress,
  const int resetPin,
  const int interruptPin,
  const int oscillatorPin
)
```

 - `pinBase`: base pin number (anything > 64)
 - `i2cAddress`: i2c address (default 0x3E)
 - `resetPin`: pin that nRST is connected to (-1 if not connected)
 - `interruptPin`: pin that nINT is connected to (-1 if not connected)
 - `oscillatorPin`: pin that OSCIO is connected to (-1 if not connected)


Pin mode, pullups/downs, digital input/output and pwm can now be used with the standard Wiring Pi functions.

Addational functions
------

To set the led driver settings, use:

`void sx1509LEDDriverSetFreq(int pinBase, int freq, int log)`

 - `pinBase`: the same number passed to  setup
 - `freq`: 1-7
 - `log`: 1 to enable logarithmic mode, 0 for linear

TODO
----

 - LED breathe/blink
 - Keypad driver
 - Interrupts
 - Debounce
 - Clock config
 - LED sync
