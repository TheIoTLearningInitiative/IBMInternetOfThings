C
==

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
root@board:~/iotf-embeddedc# ./buildlib.sh
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

