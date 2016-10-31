# Getting Started

> Using the starter applications. IBM® Bluemix® provides starter applications for the runtimes. Follow these steps to use the starter applications.

1. Navigate to the Runtimes section.
2. Click the runtime you want to use.
3. Log in to IBM® Bluemix®, if you have not already.
4. Provide the app name, modify the host name if required, and click Create.
5. Your app begins staging, and the landing page for your app on the Bluemix Dashboard displays as your app starts.
6. You can follow the instructions on that page to do the following tasks:
   6.1 Download the Cloud Foundry command line interface.
7.Download the starter application.
8.Take steps to redeploy the starter application.
9.Modify the app and deploy again.
> The directory containing the starter application you downloaded contains a README file. Refer to the README for a description of the files in the starter application package. Make changes to the code, deploy the application again, then see the effect in your running app.

- [Youtube IBMetinfo Getting started with IBM Bluemix](https://youtu.be/MtBdbaCQV8A)
- [Youtube IBMetinfo How Bluemix Works](https://www.youtube.com/watch?v=OD1NP-Yk2BI)
- [Youtube Smucsm s Teach Me How to Bluemix](https://youtu.be/10GV_MfasW4)

## Hello World Python Flask App, IBM Bluemix Console

Instructions from [Youtube Jeff Sloyer Deploying a Hello World Python Flask App in IBM Bluemix (Cloud Foundry)](https://www.youtube.com/watch?v=b-SF3bgaQTw)


1. Go to [Github IBM Bluemix Python Flask](https://github.com/IBM-Bluemix/python-hello-world-flask)
2. [Click on "Deploy to Bluemix"](https://bluemix.net/deploy?repository=https://github.com/IBM-Bluemix/bluemix-python-flask-sample)

```
PYTHON-HELLO-WORLD-FLASK
GIT URL: https://github.com/IBM-Bluemix/python-hello-world-flask
GIT BRANCH: master
APP NAME: tili-python-hello-world-flask-0001
REGION: IBM Bluemix US South
ORGANIZATUION: theiotlearninginitiative
SPACE: dev

Deploy!
```

3. Go to
http://tili-python-hello-world-flask-0001.mybluemix.net/

```sh
Hello World! I am running on port 63608
```

## Hello World Python Flask App, Cloud Foundry Command Line Interface

1. Go to https://github.com/cloudfoundry/cli
2. Download and install CF Cli from [CloudFoundry Command Line Interface](https://github.com/cloudfoundry/cli/releases)

```sh
user@workstation:~/Downloads$ sudo dpkg -i cf-cli-installer_6.16.1_i686.deb 
Selecting previously unselected package cf-cli.
(Reading database ... 152345 files and directories currently installed.)
Preparing to unpack cf-cli-installer_6.16.1_i686.deb ...
Unpacking cf-cli (6.16.1) ...
Setting up cf-cli (6.16.1) ...
user@workstation:~/Downloads$ cd
user@workstation:~$ 
```

```sh
user@workstation:~$ mkdir ibmbluemix
user@workstation:~$ cd ibmbluemix/
user@workstation:~/ibmbluemix$ git clone https://github.com/IBM-Bluemix/bluemix-python-flask-sample.git
Cloning into 'bluemix-python-flask-sample'...
remote: Counting objects: 58, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 58 (delta 4), reused 0 (delta 0), pack-reused 45
Unpacking objects: 100% (58/58), done.
Checking connectivity... done.
user@workstation:~/ibmbluemix$ cd bluemix-python-flask-sample
user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ ls
LICENSE       NOTICE    README.md         runtime.txt  welcome.py
manifest.yml  Procfile  requirements.txt  static
user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ 
user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ cat manifest.yml
---
applications:
- name: bluemix-python-flask-sample
  memory: 128M
user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ cf login -a https://api.ng.bluemix.net
API endpoint: api.ng.bluemix.net
Email> theiotlearninginitiative@
Password> 
Authenticating...
OK
Targeted org theiotlearninginitiative@
Select a space (or press enter to skip):
1. dev
2. xe1gyq
Space> xe1gyq
Targeted space xe1gyq
API endpoint:   https://api.ng.bluemix.net (API version: 2.40.0)   
User:           theiotlearninginitiative   
Org:            theiotlearninginitiative   
Space:          dev   
user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ user@workstation:~/ibmbluemix/bluemix-python-flask-sample$ cf push xeflask -m 128M
Using manifest file /home/xe1gyq/ibmbluemix/bluemix-python-flask-sample/manifest.yml
Creating app xeflask in org theiotlearninginitiative / space dev as theiotlearninginitiative...
OK
Creating route xeflask.mybluemix.net...
```

3. Go to
http://xeflask.mybluemix.net/

```sh
Hi there!
Thanks for creating a Python Flask Starter Application.
```