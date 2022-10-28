# HP ProBook 440 G7 - OpenCore files

Tested on macOS Monterey 12.6.1. *Should work on Ventura if setting the correct version of Airporttltlwm and probably some other config.plist values.*v 

Files from this repo should go to ``/EFI/OC``. Please follow [this guide](https://dortania.github.io/OpenCore-Install-Guide) for more infos about how to install macOS on your laptop and understand more things about hackintoshing. **Don't forget to set your own custom SMBIOS values before attempting to boot this configuration!** You should generate a setlist for MacBookPro16,3.

SSDT files are my own (for the most part) and not prebuilt. You should **not** attempt to use them on different hardware (even if slightly different).

## What's working

 - Screen
 - Keyboard
 - Trackpad (with macOS native gestures support)
 - Audio output 
   * Both speakers and jack work
   * Input through jack hasn't been tested (yet)
 - Wi-Fi & Bluetooth support
   * Audio and microphone through Bluetooth work as I managed to connect my AirPods
   * Correct Wi-Fi detection support with proper WPA2/3 management
   * iServices (Handoff, AirPlay, AirDrop) are a bit hasardous but works most of the time
 - USB ports with correct mappings
   * Webcam (Camera HD) is connected through internal USB and thus works out-of-the-box
 - Mostly everthing else but I forgot to put these on the list

## What's not working

 - Internal mic (should be fixed by setting a custom codec on AppleALC, I'm working on it)
 - HDMI port (should work with the right config, audio output through HDMI may never work tho)
 
> Improvements are also needed to the graphics buffers, and the power consumption/battery for our CPU. SD card reader hasn't been tested yet but should work (and probably fixable if not working out-of-the-box)