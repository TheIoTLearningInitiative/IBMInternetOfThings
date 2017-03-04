# Intel GPIO Digital

# @ Node-Red Flow Space

- Intel GPIO Digital Input
  - D8
  - Interrupt Both

- Intel GPIO Digital Input
  - D2
  - Set Initial Level of Pin to 0 Low

# Source

```js
[{"id":"744af6bf.8bb508","type":"mqtt-broker","z":"98b49c15.674b6","broker":"test.mosquitto.org ","port":"1883","clientid":"","usetls":false,"verifyservercert":true,"compatmode":true,"keepalive":"60","cleansession":true,"willTopic":"","willQos":"0","willRetain":"false","willPayload":"","birthTopic":"","birthQos":"0","birthRetain":"false","birthPayload":""},{"id":"c89cadcc.37635","type":"debug","z":"98b49c15.674b6","name":"","active":true,"console":"false","complete":"false","x":591,"y":130,"wires":[]},{"id":"7f0cbf12.80f34","type":"mqtt in","z":"98b49c15.674b6","name":"","topic":"IBMIoT/NodeRed/IntelEdison","broker":"744af6bf.8bb508","x":356,"y":130,"wires":[["c89cadcc.37635"]]}]
```

