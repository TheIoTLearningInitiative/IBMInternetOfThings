# NodeRED

> Node-RED is a tool for wiring together hardware devices, APIs and online services in new and interesting ways. Node-Red

- [Node-RED Homepage](http://nodered.org/)
- [Node-RED Getting Started](http://nodered.org/docs/getting-started/)
- [Node-RED Information](https://www-304.ibm.com/connections/blogs/et/resource/node_red/Node-Red.pdf)
- [Node-RED Github](https://github.com/node-red/node-red)
- [Node-RED IBM Github](https://github.com/ibm-messaging/iot-nodered)
- [Node-RED Flows](http://flows.nodered.org/)

- [Node-RED Documentation Installation](http://nodered.org/docs/getting-started/installation.html)
- [Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)
- [Intel® IoT Gateway Developer Hub](https://software.intel.com/en-us/tags/82166)
- [Getting Started with Node-RED and IBM Bluemix](https://github.com/intel-iot-devkit/Intel-IoT-Gateway/blob/master/Getting%20Started%20With%20Node-Red%20and%20Bluemix/README.MD)
- [Intel® IoT Gateway Developer Github](https://github.com/intel-iot-devkit/Intel-IoT-Gateway)
- [Raspberry Pi Hosting Node-Red](https://learn.adafruit.com/raspberry-pi-hosting-node-red/)
- [MakerCollider Node-Red](https://github.com/MakerCollider/node-red-nodes)

Features

- Rapid Development
- Simple use with JSON
- Simple REST
- Simple MQTT
- Simple to use other Services


UI Nodes

- Input
- Output
- Function
- social
- Storage
- Analysis
- Advanced

# Node-RED Application on BlueMix

> You should have connected a registered Device in Watson IoT Platform

[Creating a NodeRED Application on Bluemix](https://developer.ibm.com/recipes/tutorials/creating-a-nodered-application-on-bluemix/)

App Name **IntelEdison-NodeRed**
App Host **IntelEdison-NodeRed**
Domain **mybluemix.net**

## Node-Red Labs

- [Stefania Kaczmarczyk Labs](http://labs.stefdoestech.com/)
- [Stefania Kaczmarczyk Labs IoT](http://labs.stefdoestech.com/iot/)

## Node-RED Github

[Node-RED IBM Github](https://github.com/ibm-messaging/iot-nodered)

```sh
    root@edison:~# npm install node-red-contrib-ibm-watson-iot
    -\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\-\|/-\|/-\|z
    ...
    ...
    ��└��─��─ ibmiotf@0.2.11 (format@0.2.2, btoa@1.1.2, events@1.1.0, loglevel@1.4.0, bluebird@2.10.2, axios@)
    root@edison:~/.node-red# npm install node-red-contrib-iotclouddev
    -\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-z
    ...
    ...
    node-red-contrib-iotclouddev@1.0.3 node_modules/node-red-contrib-iotclouddev
    ��└��─��─ getmac@1.0.7 (extract-opts@2.2.0)
    root@edison:~/.node-red# cd
    root@edison:~# git clone https://github.com/ibm-messaging/iot-nodered.git
    Cloning into 'iot-nodered'...
    remote: Counting objects: 372, done.
    remote: Total 372 (delta 0), reused 0 (delta 0), pack-reused 372
    Receiving objects: 100% (372/372), 124.16 KiB | 168.00 KiB/s, done.
    Resolving deltas: 100% (204/204), done.
    Checking connectivity... done.
    root@edison:~# 
```

