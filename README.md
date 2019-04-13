# esp32-ble-checker
A auto work checker via detecting phone's BLE signal.

## ESP32 side

### Function
+ scan the ble device
+ connect the cloud data server
+ report the ble device mac address to the cloud data server
+ //detected change to the existance of each ble device

### implemention 
+ scan everysecond now and then
+ mantence a fixed length buffer to the ble device address that scaned
+ send the ble device address data to cloud when the buffer nearly full or reaching time point
+ compare the first five chars then compare the whole address in scan fellback function

## Cloud side
