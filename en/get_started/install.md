Install Arduino Environment
================

## Linux

### 1. Download Arduino IDE

[official download page](https://www.arduino.cc/en/Main/Software)

### 2. Install dependence 

Ubuntu for example:

```shell
sudo usermode -a -G dialout $(whoami)
sudo apt install python3 python3-pip
sudo pip3 install pyserial
```

### 3. Add board in Arduino IDE

* Add URLs

Open Arduino IDE, select `File` -> `Preferences`, 

Add `Additional Boards Manager URLs`: 
`http://dl.sipeed.com/MAIX/Maixduino/package_Maixduino_k210_index.json`

![](../../assets/arduino_settings.png)

* Install board tools and libs

Select `Tools` -> `Board` -> `Boards Manager`， search `Maixduino`, click `Install`

![](../../assets/arduino_board.png)

![](../../assets/maixduino_install.png)


### 4. Change settings about board

Change board settings in `Tools`  section on the top of Arduini IDE.

* `Board`: The same as your dev board
* `Burn Toolfirmware`: just for Maix Go Board, default `open-ec`
* `Burn Baudrate`: Decrease it if download fail
* `Port`: Serial port, e.g. `/dev/ttyUSB0`
* `Programmer`: Burn tool, must select `k-flash`

![](../../assets/arduino_board.png)





## Windows



### 1. Download Arduino IDE

[official download page](https://www.arduino.cc/en/Main/Software)

Then double click pack to install

### 2. Install dependence 

* Download [.Net Core Runtime](https://download.visualstudio.microsoft.com/download/pr/3f05ee2d-5372-43d6-9562-be86632a53d4/1361281426efa7ff206289adb0411f55/dotnet-runtime-3.0.0-preview3-27503-5-win-x64.exe) (required by burn tool [k-flash for windows](https://github.com/kendryte/kendryte-flash-windows) )

* Add toolchain path to global environment path:

Find your toolchain path, it should be like this:

```
C:\Users\(username)\AppData\Local\Arduino15\packages\Maixduino\tools\riscv64-unknown-elf-gcc\8.2.0\bin
```

The username is your PC user's name


Open search tool, type in `env`, and choose `Edit the system environment variables` -> selet `Environment Variables` -> selct `Path` in `System variables` section -> Selct`New` -> copy your toolchain path -> click OK  to confirm

![](../../assets/win10_search.png)

![](../../assets/win10_search_env.png)

![](../../assets/win10_edit_env.png)

![](../../assets/win10_add_env_path.png)

### 3. Add board in Arduino IDE

* Add URLs

Open Arduino IDE, select `File` -> `Preferences`, 

Add `Additional Boards Manager URLs`: 
`http://dl.sipeed.com/MAIX/Maixduino/package_Maixduino_k210_index.json`

![](../../assets/arduino_settings.png)

* Install board tools and libs

Select `Tools` -> `Board` -> `Boards Manager`， search `Maixduino`, click `Install`

![](../../assets/arduino_board.png)

![](../../assets/maixduino_install.png)


### 4. Change settings about board

Change board settings in `Tools`  section on the top of Arduini IDE.

* `Board`: The same as your dev board
* `Burn Toolfirmware`: just for Maix Go Board, default `open-ec`
* `Burn Baudrate`: Decrease it if download fail
* `Port`: Serial port, e.g. `/dev/ttyUSB0`
* `Programmer`: Burn tool, must select `k-flash`

![](../../assets/arduino_board.png)


