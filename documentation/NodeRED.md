# NodeRED

> Node-RED is a tool for wiring together hardware devices, APIs and online services in new and interesting ways. Node-Red

- [Node-RED Homepage](http://nodered.org/)
- [Node-RED Getting Started](http://nodered.org/docs/getting-started/)
- [Node-RED Information](https://www-304.ibm.com/connections/blogs/et/resource/node_red/Node-Red.pdf)
- [Node-RED Github](https://github.com/node-red/node-red)
- [Node-RED IBM Github](https://github.com/ibm-messaging/iot-nodered)

- [Node-RED Documentation Installation](http://nodered.org/docs/getting-started/installation.html)
- [Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)
- [Intel® IoT Gateway Developer Hub](https://software.intel.com/en-us/tags/82166)
- [Getting Started with Node-RED and IBM Bluemix](https://github.com/intel-iot-devkit/Intel-IoT-Gateway/blob/master/Getting%20Started%20With%20Node-Red%20and%20Bluemix/README.MD)

Features

- Rapid Development
- Simple use with JSON
- Simple REST
- Simple MQTT
- Simple to use other Services

```sh
    # npm install -g node-red
    # apt-get install nodejs-legacy
    $ node-red
```

```sh
    root@edison:~# npm install -g --unsafe-perm node-red
     \|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|//
     > bcrypt@0.8.5 install /usr/lib/node_modules/node-red/node_modules/bcrypt
     > node-gyp rebuild
     ...
     ��├��─��─ ws@0.8.1 (options@0.0.6, ultron@1.0.2, utf-8-validate@1.2.1, bufferutil@1.2.1)
     ��└��─��─ node-red-node-serialport@0.1.2 (serialport@2.0.6)
     root@edison:~# node-red &
     
     Go to http://<board.ip.adress>:1880/#
     
```

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

