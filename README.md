# How to build rom use device tree cm for x (6.0)
repo source rr,cm:
rr: repo init -u https://github.com/ResurrectionRemix/platform_manifest.git -b marshmallow
cm: repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0
repo sync

Device,kernel,vendor,...
1- use device from here https://github.com/NormandyEGY/andro...nokia_normandy put in /device/nokia/normandy
2- use vendor from here https://github.com/NormandyEGY/andro...nokia_normandy put in /vendor/nokia/normandy
3- use extra from here https://github.com/NormandyEGY/vendor_extra put in /vendor/normandy
4- use kernel from here https://github.com/Ahmed-Hady/androi...nokia_normandy put in /kernel/nokia/normandy
5- use media from here https://github.com/msm7x30/android_hardware_qcom_media rename to msm7x27a put in /hardware/qcom/media-caf/msm7x27a
6- use wifi from here https://github.com/NormandyEGY/andro...e_atheros_wlan put in /hardware/atheros/wlan
Others Here:
https://github.com/NormandyLP

Apply Patches
cd device/nokia/normandy/patch
sh apply.sh

Build rom:
. build/envsetup.sh && lunch cm_normandy-userdebug && brunch normandy
