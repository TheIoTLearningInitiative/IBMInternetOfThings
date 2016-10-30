# IBM Internet of Things Foundation for Python

```sh
root@board:~# pip install ibmiotf
root@board:~# git clone https://github.com/ibm-messaging/iot-python.git
Cloning into 'iot-python'...
remote: Counting objects: 1501, done.
remote: Total 1501 (delta 0), reused 0 (delta 0), pack-reused 1501
Receiving objects: 100% (1501/1501), 574.55 KiB | 212.00 KiB/s, done.
Resolving deltas: 100% (882/882), done.
Checking connectivity... done.
root@board:~# cd iot-python/
root@board:~/iot-python# ls
CHANGES.txt  LICENSE      README.rst   setup.py
CLA.md       MANIFEST.in  samples      src
root@board:~/iot-python# python setup.py install
running install
running bdist_egg
running egg_info
Using /usr/lib/python2.7/site-packages
Finished processing dependencies for ibmiotf==0.1.9
root@board:~/iot-python# cd samples
root@board:~/iot-python/samples# ls
apiExamples          helloWorld           psutil
cli                  httpsSupport         simpleApp
customMessageFormat  managedDevice
gatewayExamples      managedGateway
root@board:~/iot-python/samples# cd helloWorld/
root@board:~/iot-python/samples/helloWorld# ls
README.md      helloworld.py
root@board:~/iot-python/samples/helloWorld# python helloworld.py
2016-03-05 18:46:48,839   ibmiotf.application.Client  INFO    Connected successfully: a:quickstart:6788e5b2-r
2016-03-05 18:46:49,069   ibmiotf.device.Client      INFO    Connected successfully: d:quickstart:helloWorld6
...
^CTraceback (most recent call last):
File "helloworld.py", line 81, in <module>
time.sleep(1)                       
KeyboardInterrupt
root@board:~/iot-python/samples/helloWorld#
root@board:~/iot-python/samples/helloWorld# cd ../psutil
root@board:~/iot-python/samples/psutil# python iotpsutil.py
2016-03-05 18:51:44,770   ibmiotf.device.Client      INFO    Connected successfully: d:quickstart:sample-iotL
(Press Ctrl+C to disconnect)
root@board:~/iot-python/samples/psutil# 
```

