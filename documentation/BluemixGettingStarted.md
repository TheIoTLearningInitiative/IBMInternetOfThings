Getting Started
==

- [Youtube IBMetinfo Getting started with IBM Bluemix](https://youtu.be/MtBdbaCQV8A)
- [Youtube IBMetinfo How Bluemix Works](https://www.youtube.com/watch?v=OD1NP-Yk2BI)
- [Youtube Smucsm s Teach Me How to Bluemix](https://youtu.be/10GV_MfasW4)


## Hello World Python Flask App, IBM Bluemix Console

Instructions from [Youtube Jeff Sloyer Deploying a Hello World Python Flask App in IBM Bluemix (Cloud Foundry)](https://www.youtube.com/watch?v=b-SF3bgaQTw)


1. Go to [Github IBM Bluemix Python Flask](https://github.com/IBM-Bluemix/bluemix-python-flask-sample)
2. [Click on "Deploy to Bluemix"](https://bluemix.net/deploy?repository=https://github.com/IBM-Bluemix/bluemix-python-flask-sample)
```
BLUEMIX-PYTHON-FLASK-SAMPLE
GIT URL: https://github.com/IBM-Bluemix/bluemix-python-flask-sample
GIT BRANCH: master
```
3. 

## Hello World Python Flask App, Cloud Foundry Command Line Interface

1. Go to https://github.com/cloudfoundry/cli
2. Download and install CF Cli
```sh
xe1gyq@jessie:~/Downloads$ sudo dpkg -i cf-cli-installer_6.16.1_i686.deb 
Selecting previously unselected package cf-cli.
(Reading database ... 152345 files and directories currently installed.)
Preparing to unpack cf-cli-installer_6.16.1_i686.deb ...
Unpacking cf-cli (6.16.1) ...
Setting up cf-cli (6.16.1) ...
xe1gyq@jessie:~/Downloads$ cd
xe1gyq@jessie:~$ 
```

```sh
xe1gyq@jessie:~$ mkdir ibmbluemix
xe1gyq@jessie:~$ cd ibmbluemix/
xe1gyq@jessie:~/ibmbluemix$ git clone https://github.com/IBM-Bluemix/bluemix-python-flask-sample.git
Cloning into 'bluemix-python-flask-sample'...
remote: Counting objects: 58, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 58 (delta 4), reused 0 (delta 0), pack-reused 45
Unpacking objects: 100% (58/58), done.
Checking connectivity... done.
xe1gyq@jessie:~/ibmbluemix$ cd bluemix-python-flask-sample
xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ cf login -a https://api.ng.bluemix.net
```
