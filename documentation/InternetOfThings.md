Internet of Things
==

## Internet of Things Foundation

> Internet of Things Foundation is a fully managed, cloud-hosted service that makes it simple to derive value from Internet of Things (IoT) devices

> Internet of Things Foundation allows you to easily compose IoT solutions

> The IBM Internet of Things service lets your apps communicate with and consume data collected by your connected devices, sensors, and gateways. Our recipes make it super easy to get devices connected to our Internet of Things cloud. Your apps can then use our real-time and REST APIs to communicate with your devices and consume the data you've set them up to collect.

- [Internet of Things Foundation Landing Page](https://internetofthings.ibmcloud.com/#/)
- [Internet of Things Foundation Zone Bluemix](http://www.ibm.com/cloud-computing/bluemix/solutions/iot/)
- [Internet of Things Foundation Getting Started](https://www.ng.bluemix.net/docs/#services/IoT/index.html)
- [Internet of Things Foundation Bluemix Dashboard](https://console.ng.bluemix.net/catalog/services/internet-of-things-foundation/)
- [Internet of Things Foundation Quickstart](https://quickstart.internetofthings.ibmcloud.com/#/)
- [Creating apps with the Internet of Things starter application](https://console.ng.bluemix.net/docs/starters/IoT/iot500.html#iot500)

### Quick Start

Recipes and code for

- ARM mBed
- BeagleBone with SensorTag
- SimpleLink WiFi CC3200 LaunchPad
- Intel Galileo
- Raspberry Pi
- Arduino Uno with WiFi shield
- Device Simulator

### Examples

- https://github.com/MasayaFujita/Edison_to_IoTFoundation_Node
- https://github.com/ibm-messaging/iot-python
- https://developer.ibm.com/recipes/tutorials/connect-an-intel-galileo-to-the-internet-of-things-foundation/
- https://developer.ibm.com/recipes/tutorials/ibm-bluemix-with-python-and-iot-service/
- http://rexstjohn.com/publish-to-ibm-bluemix-via-mosquitto-from-intel-edison/
- http://www.iotdevfest.com/files/Stewart-IoTDevfest2016.pdf

## IoT Real-Time Insights

> The IBM IoT Real-Time Insights services allows you to understand IoT data in context and monitor the conditions of your devices and operations. IoT Real-Time Insights works with Internet of Things Foundation to enrich and monitor data from you devices, visualize what’s happening now, and respond to emerging conditions through automated actions.

- [IoT Real-Time Insights Homepage](https://console.ng.bluemix.net/catalog/services/iot-real-time-insights/)
- [IoT Real-Time Insights Getting Started](http://www.ng.bluemix.net/docs/services/iotrtinsights/index.html)

## flowthings.io

> flowthings.io empowers any developer or organization to leverage the growing instrumentation of the physical world (aka, the Internet of Things) in order to build solutions that surprise with their intelligence, contextual awareness, and effectiveness in operations and user experiences.

- [flowthings.io homepage](https://console.ng.bluemix.net/catalog/services/flowthingsio/)

## Internet of Things Workbench

> IBM Internet of Things Workbench is a service for designing, constructing and simulating Internet of Things systems consisting of devices, cloud services and clients. At this point it is provided as an experimental service which focuses on visual design using diagrams and rapid simulation of multiple devices over IBM Internet of Things Foundation as well as generic message brokers such as IBM Message Sight. Internet of Things Workbench generates Node.js and Node-RED application for the cloud services (applications) on top of IBM Bluemix, as well as simulated devices and clients using Javascript.

- [Internet of Things Workbench Homepage](https://console.ng.bluemix.net/catalog/services/internet-of-things-workbench/)

## Embedded C Client Library - Introduction

> Embedded C client for interacting with the IBM Watson Internet of Things Platform.

```sh
    root@board:~# git clone https://github.com/ibm-messaging/iotf-embeddedc.git
    Cloning into 'iotf-embeddedc'...
    remote: Counting objects: 124, done.
    remote: Total 124 (delta 0), reused 0 (delta 0), pack-reused 124
    Receiving objects: 100% (124/124), 71.47 KiB | 0 bytes/s, done.
    Resolving deltas: 100% (59/59), done.
    Checking connectivity... done.
    root@board:~# cd iotf-embeddedc/
    root@board:~/iotf-embeddedc# ls
    LICENSE          gatewayclient.c  iotfclient.h
    README.md        gatewayclient.h  lib
    buildlib.sh      iotfclient.c     samples
    root@edison:~/iotf-embeddedc# ./buildlib.sh
    Compiling source files ...
    Linking libiotf.so libwiotdevice.so
    Removing temporary files...
    Build complete
    root@edison:~/iotf-embeddedc# cd samples/
    root@edison:~/iotf-embeddedc/samples# ls
    Makefile         build.sh         gateway.cfg      sampleDevice.c
    README.md        device.cfg       helloWorld.c     sampleGateway.c
    root@board:~/iotf-embeddedc/samples# make          
    cc sampleDevice.c -I ./../ -I ./../lib ./../iotfclient.c ./../lib/MQTTClient.c ./../lib/MQTTLinux.c ./../libe
    strip sampleDevice            
    cc helloWorld.c -I ./../ -I ./../lib ./../iotfclient.c ./../lib/MQTTClient.c ./../lib/MQTTLinux.c ./../lib/Md
    strip helloWorld
    cc sampleGateway.c -I ./../ -I ./../lib ./../gatewayclient.c ./../lib/MQTTClient.c ./../lib/MQTTLinux.c ./..y
    strip sampleGateway
    root@board:~/iotf-embeddedc/samples# ./helloWorld 
    Usage: helloWorld deviceId
    where,                                                                           deviceId is a 12 digit hex                                                       root@board:~/iotf-embeddedc/samples# ./helloWorld 123456789123                   Connection Successful. Press Ctrl+C to quit                                       View the visualization at https://quickstart.internetofthings.ibmcloud.com/#/device/123456789123                 Publishing the event stat with rc  0                                             Publishing the event stat with rc  0
      ...
      [Open your web browser and go the address specified above]
      ...
      Publishing the event stat with rc  0
      Publishing the event stat with rc  0
    ^ CSigINT received.
    Quitting!!                                                                       root@board:~/iotf-embeddedc/samples# 
```

## IBM Internet of Things Foundation for Python

```sh
    root@board:~# pip install ibmiotf
    root@board:~# git clone https://github.com/ibm-messaging/iot-python.git
    Cloning into 'iot-python'...
    remote: Counting objects: 1501, done.
    remote: Total 1501 (delta 0), reused 0 (delta 0), pack-reused 1501
    Receiving objects: 100% (1501/1501), 574.55 KiB | 212.00 KiB/s, done.
    Resolving deltas: 100% (882/882), done.
    Checking connectivity... done.
    root@board:~# cd iot-python/
    root@board:~/iot-python# ls
    CHANGES.txt  LICENSE      README.rst   setup.py
    CLA.md       MANIFEST.in  samples      src
    root@board:~/iot-python# python setup.py install
    running install
    running bdist_egg
    running egg_info
    Using /usr/lib/python2.7/site-packages
    Finished processing dependencies for ibmiotf==0.1.9
    root@board:~/iot-python# cd samples
    root@board:~/iot-python/samples# ls
    apiExamples          helloWorld           psutil
    cli                  httpsSupport         simpleApp
    customMessageFormat  managedDevice
    gatewayExamples      managedGateway
    root@board:~/iot-python/samples# cd helloWorld/
    root@board:~/iot-python/samples/helloWorld# ls
    README.md      helloworld.py
    root@board:~/iot-python/samples/helloWorld# python helloworld.py
    2016-03-05 18:46:48,839   ibmiotf.application.Client  INFO    Connected successfully: a:quickstart:6788e5b2-r
    2016-03-05 18:46:49,069   ibmiotf.device.Client      INFO    Connected successfully: d:quickstart:helloWorld6
    ...
    ^CTraceback (most recent call last):
    File "helloworld.py", line 81, in <module>
    time.sleep(1)                       
    KeyboardInterrupt
    root@board:~/iot-python/samples/helloWorld#
    root@board:~/iot-python/samples/helloWorld# cd ../psutil
    root@edison:~/iot-python/samples/psutil# python iotpsutil.py
    2016-03-05 18:51:44,770   ibmiotf.device.Client      INFO    Connected successfully: d:quickstart:sample-iotL
    (Press Ctrl+C to disconnect)
    root@edison:~/iot-python/samples/psutil# 
```
