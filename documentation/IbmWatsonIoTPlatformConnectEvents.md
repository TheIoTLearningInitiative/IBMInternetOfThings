# Events

## NodeJS

```sh
root@board:~# ls
CodeLabs  EmbeddedLinux  ibm-iot-quickstart.zip  lib  usr
root@board:~# unzip ibm-iot-quickstart.zip 
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
root@board:~# cd ibm-iot-quickstart
root@board:~/ibm-iot-quickstart# 
```

```sh
root@board:~/ibm-iot-quickstart# sh setup.sh
Installing board packages ...
Not downgrading package nodejs on root from v4.4.3-r1.0 to 0.10.25-r0.
Installing ntp-tickadj (4.2.6p5-r6.0) on root.
Installing ntp-utils (4.2.6p5-r6.0) on root.
Installing ntpdate (4.2.6p5-r6.0) on root.
Collected errors:
 * satisfy_dependencies_for: Cannot satisfy the following dependencies for ntp-tickadj:
 *      libc0 (>= 0.9.33+git0+946799cd0ce0c6c803c9cb173a84f4d607bde350) * 
 * opkg_install_cmd: Cannot install package ntp-tickadj.
 * satisfy_dependencies_for: Cannot satisfy the following dependencies for ntp-utils:
 *      libc0 (>= 0.9.33+git0+946799cd0ce0c6c803c9cb173a84f4d607bde350) * 
 * opkg_install_cmd: Cannot install package ntp-utils.
 * satisfy_dependencies_for: Cannot satisfy the following dependencies for ntpdate:
 *      libc0 (>= 0.9.33+git0+946799cd0ce0c6c803c9cb173a84f4d607bde350) * 
 * opkg_install_cmd: Cannot install package ntpdate.
Setting time ...
setup.sh: line 5: ntpdate: command not found
Installing NodeJS packages ...
npm WARN package.json ibm-iot-quickstart@0.0.1 No repository field.
npm WARN package.json ibm-iot-quickstart@0.0.1 No README data
npm WARN package.json ibm-iot-quickstart@0.0.1 No license field.
properties@1.2.1 node_modules/properties
root@board:~/ibm-iot-quickstart# 
```

```sh
root@board:~/ibm-iot-quickstart# ls
IoTFoundation-CA.pem  device.sample.cfg      package.json  setup.sh
IoTFoundation.pem     ibm-iot-quickstart.js  packages      sketch
root@board:~/ibm-iot-quickstart# cp device.sample.cfg device.cfg 
root@board:~/ibm-iot-quickstart# nano device.cfg
```

```sh
org=my_organization
type=my_type
id=112233445566
auth-method=token
auth-token=my_token
```

## Python

```sh
root@board:~# wget https://github.com/ibm-messaging/iot-gw-solutions/releases/download/1.03/ibm-iot-quickstart.zip
root@board:~# cd ibm-iot-quickstart
root@board:~/ibm-iot-quickstart# ls
CLA.md     LICENSE    README.md  samples
root@board:~/ibm-iot-quickstart# cd samples/
root@board:~/ibm-iot-quickstart/samples# ls
client.py              ibm-iot-quickstart.py
```

```sh
root@board:~/ibm-iot-quickstart# nano device.cfg
```

```sh
org=my_organization
type=my_type
id=112233445566
auth-method=token
auth-token=my_token
```

```
root@board:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
No config file found, connecting to the Quickstart service
MAC address: 784b87a53a73
0.0
message published
1.00586756077
message published     
```