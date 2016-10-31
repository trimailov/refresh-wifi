# refresh-wifi

Small app to remove stale macOS prefrences. It removes WiFi preferences from `/Library/Preferences/SystemConfiguration/`.

It basically executes this shell script:

```
sudo rm -f
    /Library/Preferences/SystemConfiguration/com.apple.airport.preferences.plist
    /Library/Preferences/SystemConfiguration/com.apple.network.identification.plist
    /Library/Preferences/SystemConfiguration/com.apple.wifi.message-tracer.plist
    /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist
    /Library/Preferences/SystemConfiguration/preferences.plist
```

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
