# Projects

## Project Device Type

[IBM Bluemix Console](https://console.ng.bluemix.net/)

1. IBM Watson IoT Platform Quickstart connection
[Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)

   ```sh
     root@board:~# wget https://github.com/ibm-messaging/iot-gw-solutions/releases/download/1.03/ibm-iot-quickstart.zip
     root@board:~# cd ibm-iot-quickstart
     root@board:~/ibm-iot-quickstart# ls
     CLA.md     LICENSE    README.md  samples
     root@board:~/ibm-iot-quickstart# cd samples/
     root@board:~/ibm-iot-quickstart/samples# ls
     client.py              ibm-iot-quickstart.py
     root@board:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
     No config file found, connecting to the Quickstart service
     MAC address: 784b87a53a73
     0.0
     message published
     1.00586756077
     message published     
     ...
     [Go to https://quickstart.internetofthings.ibmcloud.com/#/ and write Device ID based on device MAC Address]
```

2. Register your Device In Watson IoT Platform [How to Register Devices in IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/how-to-register-devices-in-ibm-iot-foundation/)

```sh
- Create IBM Watson IoT Platform Organization
  - Name **IntelEdison01**
  - Organization ID **5ii3a2**
- Create Device Type
  - Device Type Name **IntelEdison01-DeviceType**
  - Device Type Description **Intel Edison 01 Device Type**
- Add Device in IBM Watson IoT Platform
  - Device ID (MAC Address) **784082a53a73**
  - Authentication Method **Token**
  - Authentication Token **s&M9e_vP!8Ftykd?GOP**
- Finish

3. Connect the registered Device In Watson IoT Platform
[Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)

```sh
    root@board:~# vi device.cfg
    org=5ii3a2
    type=IntelEdison01-DeviceType
    id=784082a53a73
    auth-method=token
    auth-token=s&M9e_vP!8Ftykd?GOP
    root@edison:~/ibm-iot-quickstart/samples# python ibm-iot-quickstart.py
    Configuration file found - connecting to the registered service                                              
    0.0
    message published
    0.92204526404
    message published
    
    [Go to https://6ih3a3.internetofthings.ibmcloud.com/dashboard/#/devices/browse click on your Device ID and review Recent Events]
```

## Project Gateway Type

[IBM Bluemix Console](https://console.ng.bluemix.net/) then Dashboard

1. Register your Gateway In Watson IoT Platform [How to Register Gateways in IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/how-to-register-gateways-in-ibm-watson-iot-platform/)

- Create IBM Watson IoT Platform Organization
  - Name **IntelEdison01**
  - Organization ID **5ii3a2**
- Create Device Type
  - Device Type Name **IntelEdison01-GatewayType**
  - Device Type Description **Intel Edison 01 Gateway Type**
- Add Device in IBM Watson IoT Platform
  - Device ID (MAC Address) **784082a53a73**
  - Authentication Method **Token**
  - Authentication Token **i+*La@jT5dd9YyMW9s**
- Finish

2. API Key

 - Go to IBM Watson IoT Platform Dashboard
 - Click on "ACCESS" tab
 - Click on "API Keys" tab
 - Click on “Generate API Key”

## Project

- [Connect an Intel® IoT Gateway to IBM Watson IoT Platform](https://developer.ibm.com/recipes/tutorials/connect-an-intel-iot-gateway-to-iot-foundation/)


