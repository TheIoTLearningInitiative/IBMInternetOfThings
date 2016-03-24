Quick Start
==

> Quickstart is an open sandbox allowing developers to quickly and easily get devices connected to the Watson IoT platform with registration required. 

> Quickstart! No sign-up required to see how easy it is to connect your device to Watson IoT Platform and view live sensor data.

> Quickstart Simulated Device! In addition to these, we have developed a simple browser-based simulated device, designed for mobile devices, that can be used to connect any device with a web browser to the service.

## Virtual Device

> Use the simulated device to experience the IBM Watson IoT Platform

[IBM Watson IoT Platform Virtual Device](https://developer.ibm.com/recipes/tutorials/use-the-simulated-device-to-experience-the-iot-foundation/)

### Project

Use IBM simulated device from Web Browser to experience the IBM Watson IoT Platform

From Web Browser:

1. http://quickstart.internetofthings.ibmcloud.com/iotsensor
2. http://quickstart.internetofthings.ibmcloud.com/

## Physical Device

Use IBM IoT Quickstart code to send data from a physical device to the IBM Watson IoT Platform

From development board command line:

```sh
     root@board:~# wget https://github.com/ibm-messaging/iot-gw-solutions/releases/download/1.03/ibm-iot-quickstart.zip
     root@board:~# cd ibm-iot-quickstart
     root@board:~/ibm-iot-quickstart# ls
     CLA.md     LICENSE    README.md  samples
     root@board:~/ibm-iot-quickstart# cd samples/
     root@board:~/ibm-iot-quickstart/samples# ls
     client.py              ibm-iot-quickstart.py
     root@board:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
     No config file found, connecting to the Quickstart service
     MAC address: 784b87a53a73
     0.0
     message published
     1.00586756077
     message published     
     ...
     [Go to https://quickstart.internetofthings.ibmcloud.com/#/ and write the Device ID based on device MAC Address]
```