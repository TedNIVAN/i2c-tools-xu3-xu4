# i2c-tools-xu3-xu4

## 0. Get the binaries
`git clone https://github.com/TedNIVAN/i2c-tools-xu3-xu4.git
cd i2c-tools-xu3-xu4`

## 1. Copy them to the ODROID
`adb connect <your_device_IP_address> <br />
adb remount <br />
adb push i2cdetect /system/bin
adb push i2cset /system/bin
adb push i2cget /system/bin
adb push i2cdump /system/bin`

## 2. Give the permissions
`adb shell
cd /system/bin
chmod 0777 i2c*`

## 3. Wire your devices
Hardware i2c is at pins **14** (SCL) and **16** (SDA).

## 4. Scan the devices
`i2cdetect -y 5`

## 5. Output with the BMP180 sensor*

odroidxu3:/ # i2cdetect -y 5 <br />                                                  
0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f  <br />
00:          -- -- -- -- -- -- -- -- -- -- -- -- --  <br />
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br />
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br />
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br />
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br />
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br /> 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --  <br /> 
70: -- -- -- -- -- -- -- 77 <br />
