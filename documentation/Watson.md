Watson
==

> Learning from the connected world to transform industry

- [IBM Watson Internet of Things](http://www.ibm.com/internet-of-things/index.html)
- [IBM Watson Developer Community](https://developer.ibm.com/watson/)
- [IBM Watson Developer Cloud](http://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/)

## IBM Watson IoT Platform

- [IBM Watson IoT Platform Programming Guides](https://docs.internetofthings.ibmcloud.com/)
- [IBM Watson IoT Platform Press](https://developer.ibm.com/iotfoundation/blog/2016/02/12/the-ibm-watson-iot-platform-arrives/)
- [IBM Watson IoT Platform Python for Device Developers](https://docs.internetofthings.ibmcloud.com/devices/libraries/python.html)
- [IBM Watson IoT Recipes](https://developer.ibm.com/recipes/)
- [IBM Watson IoT Platform Quickstart](https://quickstart.internetofthings.ibmcloud.com/#/)
- [Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)


### Project Device Type

[IBM Bluemix Console](https://console.ng.bluemix.net/)

1. IBM Watson IoT Platform Quickstart connection
[Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)

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
     [Go to https://quickstart.internetofthings.ibmcloud.com/#/ and write Device ID based on device MAC Address]
```

2. Register your Device In Watson IoT Platform [How to Register Devices in IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/how-to-register-devices-in-ibm-iot-foundation/)

- Create IBM Watson IoT Platform Organization
  - Name **IntelEdison01**
  - Organization ID **5ii3a2**
- Create Device Type
  - Device Type Name **IntelEdison01-DeviceType**
  - Device Type Description **Intel Edison 01 Device Type**
- Add Device in IBM Watson IoT Platform
  - Device ID (MAC Address) **784082a53a73**
  - Authentication Method **Token**
  - Authentication Token **s&M9e_vP!8Ftykd?GOP**
- Finish

3. Connect the registered Device In Watson IoT Platform
[Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)

```sh
    root@board:~# vi device.cfg
    org=5ii3a2
    type=IntelEdison01-DeviceType
    id=784082a53a73
    auth-method=token
    auth-token=s&M9e_vP!8Ftykd?GOP
    root@edison:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
    Configuration file found - connecting to the registered service                                              
    0.0
    message published
    0.92204526404
    message published
    
    [Go to https://6ih3a3.internetofthings.ibmcloud.com/dashboard/#/devices/browse click on your Device ID and review Recent Events]
    
```

### Project Gateway Type

[IBM Bluemix Console](https://console.ng.bluemix.net/) then Dashboard

1. Register your Gateway In Watson IoT Platform [How to Register Gateways in IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/how-to-register-gateways-in-ibm-watson-iot-platform/)

- Create IBM Watson IoT Platform Organization
  - Name **IntelEdison01**
  - Organization ID **5ii3a2**
- Create Device Type
  - Device Type Name **IntelEdison01-GatewayType**
  - Device Type Description **Intel Edison 01 Gateway Type**
- Add Device in IBM Watson IoT Platform
  - Device ID (MAC Address) **784082a53a73**
  - Authentication Method **Token**
  - Authentication Token **i+*La@jT5dd9YyMW9s**
- Finish

2. API Key

 - Go to IBM Watson IoT Platform Dashboard
 - Click on "ACCESS" tab
 - Click on "API Keys" tab
 - Click on “Generate API Key”

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

### Project

- [Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)
