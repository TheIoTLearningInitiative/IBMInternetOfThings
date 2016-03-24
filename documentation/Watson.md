Watson
==

> Learning from the connected world to transform industry

- [IBM Watson Developer Community](https://developer.ibm.com/watson/)
- [IBM Watson Developer Cloud](http://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/)

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
