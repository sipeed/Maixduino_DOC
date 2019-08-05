Serial
=====

In Maixduino, there are two types of serial devices, `UARTHSClass` and `UARTClass`.
The `Serial` corresponds to the `UARTHSClass`, and the remaining `Serial1`, `Serial2`, and `Serial3` are `UARTClass`. `Serial` uses the default pin as **4** (RX), **5** (TX).
So you can use it in the serial monitor on your computer.The default pins for the other three global serial ports are **6**(RX), and **7**(TX) (they are connected to the WiFi module),To use them correctly, set different pins for them in `begin()`.

## Functions

The operation of the serial port is exactly the same as that of Arduino. You can find more information on the [Arduino website](https://www.arduino.cc/reference/en/language/functions/communication/serial/).

`if(Serial)`

`available()`

`availableForWrite()`

`begin()`

`end()`

`find()`

`findUntil()`

`flush()`

`parseFloat()`

`parseInt()`

`peek()`

`print()`

`println()`

`read()`

`readBytes()`

`readBytesUntil()`

`readString()`

`readStringUntil()`

`setTimeout()`

`write()`

`serialEvent()`

## Serial port settings

Serial.begin(BaudRate, RX , TX )

