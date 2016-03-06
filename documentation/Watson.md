Watson
==

> Learning from the connected world to transform industry

- [IBM Watson Internet of Things](http://www.ibm.com/internet-of-things/index.html)
- [IBM Watson Developer Community](https://developer.ibm.com/watson/)
- [IBM Watson Developer Cloud](http://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/)

## IBM Watson IoT Platform

[IBM Watson IoT Platform](https://docs.internetofthings.ibmcloud.com/)
[IBM Watson IoT Platform Press](https://developer.ibm.com/iotfoundation/blog/2016/02/12/the-ibm-watson-iot-platform-arrives/)
[IBM Watson IoT Platform Python for Device Developers](https://docs.internetofthings.ibmcloud.com/devices/libraries/python.html)

## Project

[How to Register Devices in IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/how-to-register-devices-in-ibm-iot-foundation/)
[Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)

```sh
     root@edison:~# wget https://github.com/ibm-messaging/iot-gw-solutions/releases/download/1.03/ibm-iot-quickstart.zip
     root@edison:~# cd ibm-iot-quickstart
     root@edison:~/ibm-iot-quickstart# ls
     CLA.md     LICENSE    README.md  samples
     root@edison:~/ibm-iot-quickstart# cd samples/
     root@edison:~/ibm-iot-quickstart/samples# ls
     client.py              ibm-iot-quickstart.py
     root@edison:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
     No config file found, connecting to the Quickstart service
     MAC address: 784b87a53a73
     0.0
     message published
     1.00586756077
     message published     
     ...
     [Go to https://quickstart.internetofthings.ibmcloud.com/#/ and write Device ID based on device MAC Address]
```
