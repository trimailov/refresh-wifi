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

Download app from [realese tab](https://github.com/trimailov/refresh-wifi/releases/latest), unzip it and run it.

While you run it, you'll be prompted that you'll need to turn off your wifi and enter your password. Press OK and restart your computer.
