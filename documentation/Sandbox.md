# SandBox

## Project

https://www.ibm.com/developerworks/community/blogs/cee6c09c-a315-4b04-ad14-57d6a60fa8bb/entry/setting_up_the_iot_kit?lang=en
https://www.ibm.com/developerworks/community/blogs/cee6c09c-a315-4b04-ad14-57d6a60fa8bb/entry/Configuring_Node_Red_to_Post_to_the_Internet_of_Things_Foundation?lang=en
https://www.ibm.com/developerworks/community/blogs/cee6c09c-a315-4b04-ad14-57d6a60fa8bb/entry/Connecting_Internet_of_Things_Foundation_to_your_Bluemix_App?lang=en

Features

- Rapid Development
- Simple use with JSON
- Simple REST
- Simple MQTT
- Simple to use other Services



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