# Opencore For macOS Ventura

This is a vanilla Opencore Bootloader made specifically for the laptop with Custom ACPI Patches. This repo will be updated till the death of my laptop or me. __Along wth Ventura, this bootloader is working with Monterey, Big Sur and Catalina as well but requires some tweaks, see notes.__

## Laptop Specifications

__Model__: Dell Vostro 3468 (This is the laptop given by CM Pakistan Shehbaz Sharif in 2017)

__CPU__: Intel i7-7500U

__iGPU__: Intel HD Graphics 620

__RAM__: 8GB DDR4 2133MHz

__Touchpad__: Synaptics I2C

__Speakers__: Realtek ALC256 Audio Controller

__Wifi/Bluetooth__: fenvi VCM BCM94352Z (Changed the previously installed card, Google a better card for this laptop if you want)

For more details, Google is your best friend

## Opencore Version: __0.9.0__

## What's Working?

This laptop will be supported as long I have it. As of now, the following things are working:

| Device | Status | Comments |
| ------ | ------ | -------- |
| CPU | __Working__ | With correct native XCPM and Frequency Management (Lowest Freq: 400 MHz) |
| GPU | __Working__ | With hopefully correct framebuffer patching |
| Keyboard | __Working__ | Swap Modifier Keys in SysPrefs if wanted |
| Trackpad | __Working__ | Working with all gestures, might improve in the future |
| Brightness Controls | __Working__ | Working with keys mapped correctly to F11 and F12 :) |
| Audio | __Working__ | Use ComboJack for headphones and external mic. Function keys mapped correctly |
| Wifi | __Working (Conditional)__ | Use a compatible wifi card. This repo uses ~Intel 3165AC~ fenvi BCM94352Z. Works fine |
| Bluetooth | __Working__ | Even the Continuity Features works cuz native :P |
| Sleep | __Working__ | Laptop goes to the S3 Sleep state just fine |
| SD Card Reader | __Not Working__ | Will never work |
| HDMI | __Working__ | Empty Space cuz it will look like shit if I dont write something here |
| USB Ports | __Working__ | Properly Mapped (Finally) |
| Battery Status | __Working__ | Correct Readouts |
| iServices | __Serial Info Needed__ | Easy Fix, just update Platform Info by following Dortainia [Guide here](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)

## Notes for Big Sur

~Change itlwm with Big Sur version until I have time to create a seperate branch for it. Also, remove the Bluetool Kext and replace with Injector in the Intel Bluetooth Firmware zip.~

In case that you have Intel Wifi/Bluetooth use this stuff given sous-ci:
* itlwm: https://github.com/OpenIntelWireless/itlwm

* IntelBluetoothFirmware: https://github.com/OpenIntelWireless/IntelBluetoothFirmware

__Since the latest version of my EFI, this is no longer included or recommended__

## Misc. Notes

* ~The USB Port mapping might be different for you, so please use USBInjectAll.kext and do proper mapping through Hackintool~
* For iServices use the [Dortania Guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html)
* ~Although I tested it, if you feel 400Mhz min frequency is too low to be unstable, change it using CPUFriend Guide [here](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html)~

Well it turns out this is just not recommended since native management works just fine

## Changelog:

__11 Mar 2023__

* Updated OpenCore (`0.8.8` --> `0.9.0`)

__4 Jan 2023__

* Updated OpenCore (`0.8.5` --> `0.8.8`)

__4 Nov 2022__

* Updated OpenCore (`0.8.2` --> `0.8.5`)

__8 Sep 2022__ What the fuck took me an year to edit this changelog

* Updated OpenCore (`0.7.5` --> `0.8.2`)
* Fixed some assholery
* Fixed some more assholery
* Added some assholery


__11 Sep 2021__

* Bump min frequency back to TDP-Down Frequency after observing some crashes

9 Sep 2021

* Use Custom SSDTs for Brightness Key mapping to F11/F12
* Decluttering
* Use CPUFriend to reduce the min freq to absolute minimum for this kabylake piece of shit


8 Sep 2021:

* Updated Kexts
* OpenCore Bump (`0.7.2` --> `0.7.3`)

7 Sep 2021:

* Fix Some Broken Stuff

7 Sep 2021:

* Initial Build following the Dortania Guide



## Credits:

* Acidanthra
* Dortania Guide
* CPUFriend
* Random TonyMacx86 Guides
* Rehabman
* All the stress turning this repo in a psychological escape from my crippling anxiety
