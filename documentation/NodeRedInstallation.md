Installation
==

## i386

```sh
    # npm install -g node-red
    # apt-get install nodejs-legacy
    $ node-red
```

## Intel Edison

```sh
    root@edison:~# npm install -g --unsafe-perm node-red
     \|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|//
     > bcrypt@0.8.5 install /usr/lib/node_modules/node-red/node_modules/bcrypt
     > node-gyp rebuild
     ...
     ��├��─��─ ws@0.8.1 (options@0.0.6, ultron@1.0.2, utf-8-validate@1.2.1, bufferutil@1.2.1)
     ��└��─��─ node-red-node-serialport@0.1.2 (serialport@2.0.6)
     root@edison:~# npm install node-red-contrib-gpio
     ��├��─��─ serialport@2.0.6 (bindings@1.2.1, sf@0.1.7, async@0.9.0, nan@2.0.9, debug@2.2.0, optimist@0.6.1)
     ��└��─��─ meshblu@1.32.0 (backo@1.1.0, debug@2.2.0, json-stable-stringify@1.0.1, url@0.10.3, node-rsa@0.2.30, socket.io-c)
    root@edison:~# 

     root@edison:~# node-red &
     
     Go to http://<board.ip.adress>:1880/#
     
```