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
3. Go to
http://xe1gyq-flask.mybluemix.net/

## Hello World Python Flask App, Cloud Foundry Command Line Interface

ToDo

1. Go to https://github.com/cloudfoundry/cli
2. Download and install CF Cli from [](https://github.com/cloudfoundry/cli/releases)

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
API endpoint: api.ng.bluemix.net
Email> user@gmail.com
Password> 
Authenticating...
OK
Targeted org xe1gyq@gmail.com
Select a space (or press enter to skip):
1. dev
2. xe1gyq
Space> xe1gyq
Targeted space xe1gyq
API endpoint:   https://api.ng.bluemix.net (API version: 2.40.0)   
User:           xe1gyq@gmail.com   
Org:            xe1gyq@gmail.com   
Space:          xe1gyq   
xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ cf push xeflask -m 128M
Using manifest file /home/xe1gyq/ibmbluemix/bluemix-python-flask-sample/manifest.yml

Creating app xeflask in org xe1gyq@gmail.com / space xe1gyq as xe1gyq@gmail.com...
OK

Creating route xeflask.mybluemix.net...



xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ cf push <YOUR_APP_NAME> -m 128M
xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ cf push <YOUR_APP_NAME> -m 128M -b https://github.com/cloudfoundry/python-buildpack
xe1gyq@jessie:~/ibmbluemix/bluemix-python-flask-sample$ cf push <YOUR_APP_NAME> -m 128M -n <YOUR_HOST_NAME>

```
