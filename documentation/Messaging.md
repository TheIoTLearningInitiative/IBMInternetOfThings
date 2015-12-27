Messaging
==

> Integration and management of cloud-based and on-premises applications and data 

- __MQ Light__ Messaging API for application developers, based on the open AMQP standard. Clients available in node.js, Ruby, Python and Java
- __Message Hub__ Messaging solution in IBM’s Bluemix cloud platform, based on Apache Kafka. Deploy as part of a cloud solution to build messaging into your apps.
- __IBM MQ__ Run your enterprise messaging backbone with IBM MQ: our most powerful tools to maximise the speed and reliability of your business’ messaging.


- [IBM Messaging](http://www-03.ibm.com/software/products/en/category/messaging)
- [IBM Messaging Developer](https://developer.ibm.com/messaging/)
- [IBM Messaging Developer Blogs](https://developer.ibm.com/messaging/blogs/)
- [IBM Community around IBM Messaging Products Github](Ihttps://github.com/ibm-messaging)

## MQ Light

> IBM MQ Light A simple yet powerful AMQP based messaging API. Write apps that run locally, in the cloud, or alongside IBM MQ.

- [MQ Light Homepage](https://developer.ibm.com/messaging/mq-light/)
- [MQ Light Getting Started](https://developer.ibm.com/messaging/mq-light/docs/)
- [MQ Light Github](https://github.com/ibm-messaging?utf8=%E2%9C%93&query=mqlight)
- [MQ Light Presentation](http://www.slideshare.net/nicholsr/ame4181-introducing-mq-light)

### MQ Light Applications

- [Getting started with Python apps using the MQ Light Service for Bluemix](https://developer.ibm.com/messaging/2015/02/19/getting-started-python-apps-using-mq-light-service-bluemix/)
- [MQ Light Python sample for Bluemix](git clone https://github.com/ibm-messaging/mqlight-python-bluemix)
- [Deploy a sample application in MQLight as a service in Bluemix](https://www.youtube.com/watch?v=iwSh8wGjB20)

```sh
    # pip install mqlight --pre
    # dpkg -l libuuid1
    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name                     Version           Architecture      Description
    +++-========================-=================-=================-=====================================================
    ii  libuuid1:amd64           2.20.1-5.1ubuntu2 amd64             Universally Unique ID library
```
```sh
    # nano mqlightrx.py
```
```python
    #!/usr/bin/python
    import mqlight
    
    def on_started(err):
      client.subscribe('news/technology', on_message=on_message)
    
    def on_message(message_type, data, delivery):
      print(data)
    
    client = mqlight.Client('amqp://localhost',on_started=on_started)
```
```sh
    # nano mqlighttx.py
```
```python
    import mqlight
    
    def on_started(err):
      client.send('news/technology', 'Hello World!')
    
    client = mqlight.Client('amqp://localhost',on_started=on_started)
```

### MQ Light Bluemix



## Message Hub

> A scalable, distributed, high throughput message bus in the cloud, available as a fully managed Bluemix service.

- [IBM Developer Works Message Hub Homepage](https://developer.ibm.com/messaging/message-hub/)