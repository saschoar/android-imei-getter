# android-imei-getter
Simple non-GUI app to help getting the device IMEI over ADB.

## Usage:

```bash
# install application
adb install imeigetter.apk

# an app start is required to register the broadcast receiver, so we start the main activity here
adb shell am start -n com.saschahuth.imeigetter/.MainActivity

# send the broadcast to receive the result
adb shell am broadcast -a com.saschahuth.imeigetter.GET_IMEI
# output will be something like:
# Broadcast completed: result=0, data="000000000000000", where "data" is the IMEI

# uninstall application
adb uninstall com.saschahuth.imeigetter
```