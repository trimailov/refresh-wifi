# refresh-wifi

![](logo.png)

Small app to remove stale macOS WiFi preferences from `/Library/Preferences/SystemConfiguration/` to "refresh" WiFi.

It basically executes this shell script:

```
sudo rm -f
    /Library/Preferences/SystemConfiguration/com.apple.airport.preferences.plist
    /Library/Preferences/SystemConfiguration/com.apple.network.identification.plist
    /Library/Preferences/SystemConfiguration/com.apple.wifi.message-tracer.plist
    /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist
    /Library/Preferences/SystemConfiguration/preferences.plist
```

## Motivation

After some time, or after macOS updates WiFi stops working in stable way. Either it loses connection every few minutes, requires restarting, router restarting, etc.

Often it's recommended simply to remove WiFi preferences and restart your computer. It works for me and people around me, thus I created this app so not only me, but less tech savvy people could do this themselves without any help.

## Use

### As app

1. Download app from [realese tab](https://github.com/trimailov/refresh-wifi/releases/latest)
2. Unzip it
3. Run it. *

\* While you run it, you'll be prompted that you'll need to turn off your wifi and enter your password, press OK and restart your computer.

### As script

1. Download project as zip
2. Copy `rm_wifi_preferences.workflow` to `/Library/Scripts/`
3. You can run it from your menu bar *

\* To run workflow as script, you may need to open `Script Editor.app` and in General preferences tab select `Show Script menu in menu bar`.
