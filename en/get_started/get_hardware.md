Get development board
========



Get your favorite hardware from Sipeed's official Taobao store： [Taobao](https://shop365481095.taobao.com/)



## Required hardware

### 一A development board

Choose a board [here](../hardware/board.md)

### USB Type C cable

![Type-C](../../assets/type_c.png)

Type-C is chosen because it supports positive and negative insertion and is very friendly to development.

Buy from Taobao official can ask if it is included, most of the current Android machines are also using Type C cable

### Screen

By default, the LCD (24pin interface) of the st7789 driver chip is used with a resolution of 320x240.

Buy from Taobao official can ask if it contains

### Camera

Use ov2640 by default

Buy from Taobao official can ask if it contains



### Micro SD Card (TF Card) (optional)

Not applicable SD card can also manipulate files. Some of the internal Flash has been reserved as a file system, but Flash is very slow!

In order to facilitate the quick operation of the picture file, you can choose to purchase a `Micro SD` card, MaixPy has built-in SPI SD card protocol driver.

When purchasing, try to choose a new Micro SD card with fast speed, such as SD 2 generation protocol, Class10 memory card.

Of course, the quality of SD cards on the market is uneven, and the SPI mode may not be compatible. Try to buy a regular card. Or maybe you should customize the driver code ~~

As shown below, the two cards on the left are not supported by the MaixPy driver. Both the middle and the right are supported, but the class10 card in the middle is the fastest.

![](../../assets/TF.png)


### ST-Link (used to update the firmware of the STM32 on the development board Maix Go) (optional)

If you purchase `Maix Go`, it integrates a `STM32` chip to simulate the 'USB to serial' tool, and simulate `JTAG`. If you want to update its firmware later, it is recommended to buy a `ST-Link` Spare

### JTAG Debugger (optional)

`K210` This chip supports `JTAG` debugging. If you need debugging function, you need to use `JTAG` debugger. Please consult the official `Sipeed` Taobao shop.

If you are a `Maix Go` development board, you don't need to purchase the `JTAG` debugger separately. The `Max Go` development board has an integrated `STM32` chip that can emulate `JTAG` (`STM32` uses `CMSIS-DAP` or `open-ec` firmware), `open-ec` firmware is not currently supported, will be supported later, please refer to the `open-ec` github project home page description

