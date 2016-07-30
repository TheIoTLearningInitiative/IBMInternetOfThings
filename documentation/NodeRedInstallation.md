# Installation

- [A set of node-red nodes for connecting to johnny-five IO Plugins](https://github.com/monteslu/node-red-contrib-gpio)
- [Intel Galileo & Intel Edison IO Plugin for Johnny-Five](https://github.com/rwaldron/galileo-io/)
- [Youtube Rupam Beginners Guide to node red with Intel Edison Twitter,Gmail,Data Logging,Gpio,MQTT](https://www.youtube.com/watch?v=2k6HrxSmA30)
- [Scargill Backing up Node-Red](http://tech.scargill.net/backing-up-node-red/)
- [node-red-node-intel-gpio](http://flows.nodered.org/node/node-red-node-intel-gpio)

# i386

```sh
    # apt-get install npm nodejs nodejs-legacy
    # npm install -g node-red
    $ node-red
```

# Intel Edison

Install the following npm packages:

- node-red-node-intel-gpio
- node-red-contrib-gpio
- galileo-io
- node-red

## node-red-node-intel-gpio

> A Node-RED node to talk to an Intel Galileo or Edison using mraa

- [NPM JS node-red-node-intel-gpio](https://www.npmjs.com/package/node-red-node-intel-gpio)

```sh
root@edison:~# npm install node-red-node-intel-gpio
node-red-node-intel-gpio@0.0.4 node_modules/node-red-node-intel-gpio
root@edison:~#
```

Look at Node Intel-GPIO

- Digital In
- Digital Out
- Digital PWM

## node-red-contrib-gpio

```sh
root@edison:~# npm install node-red-contrib-gpio
```

```sh

```

```sh
root@edison:~# ls /usr/lib/node_modules/
iotkit                    jsupm_grovevdiv           jsupm_mpl3115a2
jsupm_grovespeaker        jsupm_mma7660
```

## node-red-contrib-gpio

```sh
    root@edison:~# npm install galileo-io
```

```sh
    -\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|-\|/-\|/-\|/-\|/-
    > galileo-io@0.9.4 postinstall /home/root/node_modules/galileo-io
    > node scripts/postinstall
    ...
      Galileo-IO needs to install a trusted version of libmraa0.
    ...
    ��├��─��─ remapped@0.2.1 (getobject@0.1.0, traverse@0.6.6)
    ��└��─��─ es6-shim@0.35.0
```

## node-red

```sh
     root@edison:~# npm install -g --unsafe-perm node-red
     \|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|//
     > bcrypt@0.8.5 install /usr/lib/node_modules/node-red/node_modules/bcrypt
     > node-gyp rebuild
     ...
     ��├��─��─ ws@0.8.1 (options@0.0.6, ultron@1.0.2, utf-8-validate@1.2.1, bufferutil@1.2.1)
     ��└��─��─ node-red-node-serialport@0.1.2 (serialport@2.0.6)
```

## Get board.ip.adress

```sh
    root@edison:~# ifconfig
    ...
    wlan0     Link encap:Ethernet  HWaddr 78:4b:87:a5:3a:73  
              inet addr:192.168.1.65  Bcast:192.168.1.255  Mask:255.255.255.0
    ...
```

## Launch #1

```sh
    root@edison:~# node-red &
```

## Launch #2

```sh
    root@edison:~# ./node_modules/node-red/bin/node-red-pi 
    
    Welcome to Node-RED
    ===================
    
    26 Mar 14:02:36 - [info] Node-RED version: v0.13.4
    26 Mar 14:02:36 - [info] Node.js  version: v0.10.38
    26 Mar 14:02:36 - [info] Linux 3.10.17-poky-edison+ ia32 LE
    26 Mar 14:02:36 - [info] Loading palette nodes
    ...
    26 Mar 14:02:47 - [info] Started flows
    26 Mar 14:02:47 - [info] Server now running at http://127.0.0.1:1880/
     
    Go to http://<board.ip.adress>:1880/#

    root@edison:~# ls .node-red      
    flows_edison.json  lib                node_modules       settings.js
    root@edison:~#
```

## PC

Go to http://<board.ip.adress>:1880/#