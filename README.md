# i2c-tools-xu3-xu4

## 0. Get the binaries
`git clone https://github.com/TedNIVAN/i2c-tools-xu3-xu4.git
cd i2c-tools-xu3-xu4`

## 1. Copy them to the ODROID
`adb connect <your_device_IP_address>
adb remount
adb push i2cdetect /system/bin
adb push i2cset /system/bin
adb push i2cget /system/bin
adb push i2cdump /system/bin`

## 2. Give the permissions
`adb shell
cd /system/bin
chmod 0777 i2c*`

## 3. Wire your devices
Hardware i2c at pins **14** (SCL) and **16** (SDA).

## 4. Scan the devices
`i2cdetect -y 5`

## 5. Output with the BMP180 sensor*

odroidxu3:/ # i2cdetect -y 5 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
70: -- -- -- -- -- -- -- 77  
