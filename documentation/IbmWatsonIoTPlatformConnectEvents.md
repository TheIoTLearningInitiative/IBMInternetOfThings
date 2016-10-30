# Events

```sh
root@edison:~# ls
CodeLabs  EmbeddedLinux  ibm-iot-quickstart.zip  lib  usr
root@edison:~# unzip ibm-iot-quickstart.zip 
Archive:  ibm-iot-quickstart.zip
   creating: ibm-iot-quickstart/
  inflating: ibm-iot-quickstart/setup.sh
  inflating: ibm-iot-quickstart/package.json
  inflating: ibm-iot-quickstart/device.sample.cfg
  inflating: ibm-iot-quickstart/IoTFoundation.pem
   creating: ibm-iot-quickstart/packages/
  inflating: ibm-iot-quickstart/packages/nodejs_0.10.25-r0_i586.ipk
  inflating: ibm-iot-quickstart/packages/ntp-utils_4.2.6p5-r6.0_i586.ipk
  inflating: ibm-iot-quickstart/packages/ntp-tickadj_4.2.6p5-r6.0_i586.ipk
  inflating: ibm-iot-quickstart/packages/ntpdate_4.2.6p5-r6.0_i586.ipk
   creating: ibm-iot-quickstart/sketch/
   creating: ibm-iot-quickstart/sketch/print_ipaddr/
  inflating: ibm-iot-quickstart/sketch/print_ipaddr/print_ipaddr.ino
  inflating: ibm-iot-quickstart/IoTFoundation-CA.pem
  inflating: ibm-iot-quickstart/ibm-iot-quickstart.js
root@edison:~# cd ibm-iot-quickstart
root@edison:~/ibm-iot-quickstart# 
```

```sh
root@edison:~/ibm-iot-quickstart# ls
IoTFoundation-CA.pem  device.sample.cfg      package.json  setup.sh
IoTFoundation.pem     ibm-iot-quickstart.js  packages      sketch
root@edison:~/ibm-iot-quickstart# cp device.sample.cfg device.cfg 
root@edison:~/ibm-iot-quickstart# 
```
