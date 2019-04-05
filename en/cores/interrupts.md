Interrupts
=====

In Maixduino, you can use up to 32 digital pins (can be arbitrarily selected among 48 FPIOs) as external interrupts.

-----

## attachInterrupt()

### Description

Set Digital Pins With Interrupts.

### Syntax

`attachInterrupt(pin, ISR, mode)`

### Parameters

`pin`: the pin number

`ISR`: the ISR to call when the interrupt occurs; this function must take no parameters and return nothing. This function is sometimes referred to as an interrupt service routine.

`mode`: defines when the interrupt should be triggered. Four constants are predefined as valid values:

* `LOW` to trigger the interrupt whenever the pin is low,

* `CHANGE` to trigger the interrupt whenever the pin changes value

* `RISING` to trigger when the pin goes from low to high,

* `FALLING` for when the pin goes from high to low.

* `HIGH` to trigger the interrupt whenever the pin is high.

### Returns

Nothing

-----

## detachInterrupt()

### Description

Turns off the given interrupt.

### Syntax

`detachInterrupt(pin)` 

### Parameters

`pin`: the pin number of the interrupt to disable

### Returns
Nothing
