# Projects

- [Developing with Node-RED](0https://software.intel.com/en-us/articles/developing-with-node-red)


## Input Mqtt + Output Debug

### @ Node-Red Flow Space

> Input Mqtt
> > Server test.mosquitto.org:1883
> > Topic IBMIoT/NodeRed/IntelEdison

> Output Debug
> > Output Message Property
> > msg.payload

### Source

```js
[{"id":"744af6bf.8bb508","type":"mqtt-broker","z":"98b49c15.674b6","broker":"test.mosquitto.org ","port":"1883","clientid":"","usetls":false,"verifyservercert":true,"compatmode":true,"keepalive":"60","cleansession":true,"willTopic":"","willQos":"0","willRetain":"false","willPayload":"","birthTopic":"","birthQos":"0","birthRetain":"false","birthPayload":""},{"id":"c89cadcc.37635","type":"debug","z":"98b49c15.674b6","name":"","active":true,"console":"false","complete":"false","x":591,"y":130,"wires":[]},{"id":"7f0cbf12.80f34","type":"mqtt in","z":"98b49c15.674b6","name":"","topic":"IBMIoT/NodeRed/IntelEdison","broker":"744af6bf.8bb508","x":356,"y":130,"wires":[["c89cadcc.37635"]]}]
```

### @ Intel Edison Console

```sh
    26 Mar 14:37:38 - [info] Started flows
    26 Mar 14:37:40 - [info] [mqtt-broker:744af6bf.8bb508] Connected to broker: mqtt://test.mosquitto.org :1883
```

### @ Another Device

```sh
    $ mosquitto_pub -h test.mosquitto.org -t IBMIoT/NodeRed/IntelEdison -m "Hello World!"
```
### @ Node-Red Debug Tab

```sh
    3/26/2016, 8:41:18 AMc89cadcc.37635
    IBMIoT/NodeRed/IntelEdison : msg.payload : string [12]
    Hello World!
```

## Input Mqtt + Output Debug + Function Function 

#### @ Node-Red Flow Space

> Input Mqtt
> > Server test.mosquitto.org:1883
> > Topic IBMIoT/NodeRed/IntelEdison

> Output Debug
> > Output Message Property
> > msg.payload

> Function Function
> > Name MyFunction
> > Function Code See Below

```js
if (msg.payload == 'On')
{
    msg.payload = 1
}
if (msg.payload == 'Off')
{
    msg.payload = 0
}
return msg;
```

> Output Gpio
> > Board galileo-io
> > > Nodebot Galileo/Edison
> > Type Digital (0/1)
> > Pin 13

### Source

```js
[{"id":"e7025d5c.18fda","type":"nodebot","z":"98b49c15.674b6","name":"","username":"","password":"","boardType":"galileo-io","serialportName":"","connectionType":"local","mqttServer":"","socketServer":"","pubTopic":"","subTopic":"","tcpHost":"","tcpPort":"","sparkId":"","sparkToken":"","beanId":"","impId":"","meshbluServer":"https://meshblu.octoblu.com","uuid":"","token":"","sendUuid":""},{"id":"744af6bf.8bb508","type":"mqtt-broker","z":"98b49c15.674b6","broker":"test.mosquitto.org ","port":"1883","clientid":"","usetls":false,"verifyservercert":true,"compatmode":true,"keepalive":"60","cleansession":true,"willTopic":"","willQos":"0","willRetain":"false","willPayload":"","birthTopic":"","birthQos":"0","birthRetain":"false","birthPayload":""},{"id":"c89cadcc.37635","type":"debug","z":"98b49c15.674b6","name":"","active":true,"console":"false","complete":"payload","x":591,"y":130,"wires":[]},{"id":"7f0cbf12.80f34","type":"mqtt in","z":"98b49c15.674b6","name":"","topic":"IBMIoT/NodeRed/IntelEdison","broker":"744af6bf.8bb508","x":232,"y":130,"wires":[["c89cadcc.37635","a439a46b.5bc658"]]},{"id":"a439a46b.5bc658","type":"function","z":"98b49c15.674b6","name":"MyFunction","func":"if (msg.payload == 'On')\n{\n    msg.payload = 1\n}\nif (msg.payload == 'Off')\n{\n    msg.payload = 0\n}\nreturn msg;","outputs":1,"noerr":0,"x":444,"y":186,"wires":[["5366e815.ac9918"]]},{"id":"5366e815.ac9918","type":"gpio out","z":"98b49c15.674b6","name":"","state":"OUTPUT","pin":"13","i2cDelay":"0","i2cAddress":"","i2cRegister":"","outputs":0,"board":"e7025d5c.18fda","x":628,"y":186,"wires":[]}]
```

### @ Intel Edison Console

```sh
    1459004673454 Connected Intel Edison  
    26 Mar 15:04:33 - [info] [mqtt-broker:744af6bf.8bb508] Connected to broker: mqtt://test.mosquitto.org :1883
```

### @ Another Device

```sh
    $ mosquitto_pub -h test.mosquitto.org -t IBMIoT/NodeRed/IntelEdison -m "On"
    $ mosquitto_pub -h test.mosquitto.org -t IBMIoT/NodeRed/IntelEdison -m "Off"
```
### @ Node-Red Debug Tab

```sh
    3/26/2016, 9:06:37 AMc89cadcc.37635
    IBMIoT/NodeRed/IntelEdison : msg.payload : string [2]
    On
    3/26/2016, 9:06:41 AMc89cadcc.37635
    IBMIoT/NodeRed/IntelEdison : msg.payload : string [3]
    Off
```

### @ Intel Edison Board

Check the Led tight to GPIO 13 (DS2)

## Intel Edison + Grove Starter Kit

- [Node-RED nodes to support a few Grove Sensors for Intel Edison Arduino Board](http://flows.nodered.org/node/node-red-contrib-socialogix4edison)

```sh
    root@edison:~# npm install node-red-contrib-socialogix4edison
    -\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-n
    ��└��─��─ q@1.4.1
    root@edison:~# 
```