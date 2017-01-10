# Input Inject + Output Debug

# @ Node-Red Flow Space

* Node Input: Inject

  * Payload: **Timestamp**
  * Topic: 
  * Repeat: **Interval** every **1** Second
  * Name: 

* Node Output: Debug

  * Output: msg.payload
  * To: debug tab
  * Name: 

# Source

```js
[{"id":"c89cadcc.37635","type":"debug","z":"98b49c15.674b6","name":"","active":true,"console":"false","complete":"false","x":591,"y":130,"wires":[]},{"id":"eb9bef99.14641","type":"inject","z":"98b49c15.674b6","name":"","topic":"","payload":"","payloadType":"date","repeat":"1","crontab":"","once":false,"x":206,"y":130,"wires":[["c89cadcc.37635"]]}]
```

# @ Intel Edison Console

```sh
26 Mar 14:20:30 - [info] Started flows
```

# @ Node-Red Debug Tab

```sh
3/26/2016, 8:47:43 AM8b89cb10.747638
    Hi : msg.payload : string [0]
```



