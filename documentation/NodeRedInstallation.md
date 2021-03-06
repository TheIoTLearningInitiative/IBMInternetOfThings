# Installation

- [A set of node-red nodes for connecting to johnny-five IO Plugins](https://github.com/monteslu/node-red-contrib-gpio)
- [Intel Galileo & Intel Edison IO Plugin for Johnny-Five](https://github.com/rwaldron/galileo-io/)
- [Youtube Rupam Beginners Guide to node red with Intel Edison Twitter,Gmail,Data Logging,Gpio,MQTT](https://www.youtube.com/watch?v=2k6HrxSmA30)
- [Scargill Backing up Node-Red](http://tech.scargill.net/backing-up-node-red/)
- [node-red-node-intel-gpio](http://flows.nodered.org/node/node-red-node-intel-gpio)

# Intel Edison

Install the following npm packages:

- mraa
- galileo-io
- node-red
- node-red-node-intel-gpio
- node-red-contrib-gpio

## Mraa IO Library

> IO library that helps you use I2c, SPI, gpio, uart, pwm, analog inputs (aio) and more on a number of platforms such as the Intel galileo, the Intel edison and others

```sh
root@edison:~# opkg update
root@edison:~# opkg install mraa
```

```sh
Upgrading mraa from 1.0.0-r0 to 1.5.1 on root.
Downloading http://iotdk.intel.com/repos/3.5/intelgalactic/opkg/i586//mraa_1.5.1_i586.ipk.
Removing package mraa-dev from root...
Removing package mraa-doc from root...
Removing obsolete file /usr/lib/libmraa.so.1.0.0.
Configuring mraa.
```

## NodeRED Directory

```sh
root@edison:~# mkdir nodered
root@edison:~# cd nodered/
root@edison:~/nodered# 
```

## Node-RED Mraa Library

```sh
root@edison:~/nodered# npm install mraa
```

```sh
-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/
> mraa@1.5.1 install /home/root/nodered/node_modules/mraa
> node-gyp rebuild
...
  SOLINK_MODULE(target) Release/obj.target/mraa.node
  COPY Release/mraa.node
make: Leaving directory '/home/root/nodered/node_modules/mraa/build'
mraa@1.5.1 node_modules/mraa
```

## Node-RED galileo-io / edison-io

> Intel Edison & Intel Galileo IO Plugin for Johnny-Five JavaScript Robotics

```sh
root@edison:~/nodered# npm install galileo-io
```

```sh
-\|/-\|/-\|/-\|/-\|/-\|/--\|/-\|/-\|/-\|/-\-\|/-galileo-io@0.10.0 node_modules/galileo-io
��├��─��─ es6-shim@0.35.3
��└��─��─ remapped@0.2.1 (getobject@0.1.0, traverse@0.6.6)
```

## Node-RED node-red :)

> A visual tool for wiring the Internet of Things

```sh
root@edison:~/nodered# npm install node-red
```

```sh
node-red@0.14.6 /usr/lib/node_modules/node-red
-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/
...
...
├── is-utf8@0.2.1
├── on-headers@1.0.1
├── basic-auth@1.0.4
├── media-typer@0.3.0
├── semver@5.3.0
├── node-red-node-rbe@0.1.5
├── clone@1.0.2
├── mustache@2.2.1
├── cookie-parser@1.4.3 (cookie-signature@1.0.6, cookie@0.3.1)
├── passport-http-bearer@1.0.1 (passport-strategy@1.0.0)
├── passport-oauth2-client-password@0.1.2 (passport-strategy@1.0.0)
├── nopt@3.0.6 (abbrev@1.0.9)
├── passport@0.3.2 (pause@0.0.1, passport-strategy@1.0.0)
├── fs.notify@0.0.4 (async@0.1.22, retry@0.6.1)
├── bcryptjs@2.3.0
├── cors@2.7.1 (vary@1.1.0)
├── follow-redirects@0.2.0 (stream-consume@0.1.0, debug@2.2.0)
├── raw-body@2.1.7 (unpipe@1.0.0, bytes@2.4.0, iconv-lite@0.4.13)
├── sentiment@1.0.6 (lodash.assign@4.0.1)
├── body-parser@1.15.2 (content-type@1.0.2, bytes@2.4.0, depd@1.1.0, qs@6.2.0, on-finished@2.3.0, http-errors@1.5.0, debug@2.2.0, iconv-lite@0.4.13, type-is@1.6.13)
├── oauth2orize@1.4.0 (uid2@0.0.3, utils-merge@1.0.0, debug@2.2.0)
├── express@4.14.0 (escape-html@1.0.3, array-flatten@1.1.1, cookie-signature@1.0.6, utils-merge@1.0.0, encodeurl@1.0.1, content-type@1.0.2, merge-descriptors@1.0.1, methods@1.1.2, parseurl@1.3.1, serve-static@1.11.1, content-disposition@0.5.1, range-parser@1.2.0, etag@1.7.0, fresh@0.3.0, vary@1.1.0, cookie@0.3.1, path-to-regexp@0.1.7, depd@1.1.0, qs@6.2.0, on-finished@2.3.0, finalhandler@0.5.0, proxy-addr@1.1.2, debug@2.2.0, type-is@1.6.13, send@0.14.1, accepts@1.3.3)
├── when@3.7.7
├── bcrypt@0.8.7 (bindings@1.2.1, nan@2.3.5)
├── fs-extra@0.30.0 (path-is-absolute@1.0.0, klaw@1.3.0, graceful-fs@4.1.5, jsonfile@2.3.1, rimraf@2.5.4)
├── uglify-js@2.7.0 (async@0.2.10, uglify-to-browserify@1.0.2, source-map@0.5.6, yargs@3.10.0)
├── node-red-node-email@0.1.10 (mailparser@0.6.1, imap@0.8.17, poplib@0.1.7, nodemailer@1.11.0)
├── mqtt@1.13.0 (inherits@2.0.1, reinterval@1.1.0, xtend@4.0.1, help-me@0.1.0, minimist@1.2.0, commist@1.0.0, mqtt-connection@2.1.1, readable-stream@1.0.34, end-of-stream@1.1.0, pump@1.0.1, mqtt-packet@3.4.7, concat-stream@1.5.1, split2@2.1.0, websocket-stream@3.2.1)
├── node-red-node-feedparser@0.1.5 (feedparser@1.1.3, request@2.65.0)
├── node-red-node-twitter@0.1.6 (twitter-ng@0.6.2, oauth@0.9.14, request@2.67.0)
├── i18next@1.10.6 (cookies@0.6.1, json5@0.2.0, i18next-client@1.10.3)
├── ws@0.8.1 (options@0.0.6, ultron@1.0.2, bufferutil@1.2.1, utf-8-validate@1.2.1)
├── cron@1.1.0 (moment-timezone@0.3.1)
├── cheerio@0.19.0 (entities@1.1.1, dom-serializer@0.1.0, css-select@1.0.0, htmlparser2@3.8.3, lodash@3.10.1)
├── xml2js@0.4.17 (sax@1.2.1, xmlbuilder@4.2.1)
└── node-red-node-serialport@0.2.1 (serialport@2.1.2)
```

```sh
root@edison:~/nodered# ls
node_modules
root@edison:~/nodered# ls node_modules/
galileo-io  mraa  node-red
root@edison:~/nodered# ls node_modules/node-red/
CHANGELOG.md        LICENSE    editor        package.json  red.js
CODE_OF_CONDUCT.md  README.md  node_modules  public        settings.js
CONTRIBUTING.md     bin        nodes         red
root@edison:~/nodered# ls node_modules/node-red/bin
node-red-pi
```

## Node-RED Execution

```sh
root@edison:~/nodered# node_modules/node-red/bin/node-red-pi 
```

```sh
4 Mar 04:10:34 - [info] 

Welcome to Node-RED
===================

4 Mar 04:10:34 - [info] Node-RED version: v0.16.2
4 Mar 04:10:34 - [info] Node.js  version: v4.4.3
4 Mar 04:10:34 - [info] Linux 3.10.98-poky-edison+ ia32 LE
4 Mar 04:10:37 - [info] Loading palette nodes
4 Mar 04:10:47 - [warn] ------------------------------------------------------
4 Mar 04:10:47 - [warn] [rpi-gpio] Info : Ignoring Raspberry Pi specific node
4 Mar 04:10:47 - [warn] ------------------------------------------------------
4 Mar 04:10:47 - [info] Settings file  : /home/root/.node-red/settings.js
4 Mar 04:10:47 - [info] User directory : /home/root/.node-red
4 Mar 04:10:47 - [info] Flows file     : /home/root/.node-red/flows_edison.json
4 Mar 04:10:48 - [info] Creating new flow file
4 Mar 04:10:48 - [info] Server now running at http://127.0.0.1:1880/
4 Mar 04:10:48 - [info] Starting flows
4 Mar 04:10:48 - [info] Started flows
```

Go to http://board.ip.adress:1880/#

Loook at the installed __UI Nodes__

- Input
- Output
- Function
- social
- Storage
- Analysis
- Advanced

## Node-Red Required Modules

### node-red-contrib-gpio

> A set of node-red nodes for using johnny-five and IO plugins

Supported Hardware

- Arduino/Firmata	firmata
- Raspberry Pi	raspi-io
- BeagleBone Black	beaglebone-io
- C.H.I.P.	chip-io
- Galileo/Edison	galileo-io
- Blend Micro	blend-micro-io
- LightBlue Bean	bean-io
- Electirc Imp	imp-io
- Particle(Spark) Core	particle-io

```sh
root@edison:~/nodered# npm install node-red-contrib-gpio
```

```sh
> meshblu@2.3.2 preinstall /home/root/nodered/node_modules/node-red-contrib-gpio/node_modules/meshblu
> node -e "try{require('./skip-install.js')}catch(e){}"
...
��├��─��─ udp-serial@0.2.0
��├��─��─ mqtt-serial@0.6.0
��├��─��─ skynet-serial@1.3.0 (debug@2.6.1)
��├��─��─ firmata@0.15.0 (browser-serialport@2.1.0, es6-shim@0.35.3)
��├��─��─ johnny-five@0.10.6 (lodash.debounce@4.0.8, lodash.clonedeep@4.5.0, ease-component@1.0.0, browser-serialport@2.1.0, color-convert@1.2.2, nanotimer@0.3.10, temporal@0.5.0, chalk@1.1.3, es6-shim@0.35.3)
��├��─��─ mqtt@2.4.0 (inherits@2.0.3, reinterval@1.1.0, xtend@4.0.1, minimist@1.2.0, concat-stream@1.6.0, commist@1.0.0, split2@2.1.1, end-of-stream@1.1.0, pump@1.0.2, mqtt-packet@5.2.1, readable-stream@2.2.3, )
��├��─��─ lodash@4.17.4
��├��─��─ serialport@4.0.7 (bindings@1.2.1, commander@2.9.0, debug@2.6.1, lie@3.1.1, nan@2.5.1, object.assign@4.0.4)
��└��─��─ meshblu@2.3.2 (backo@1.1.0, debug@2.6.1, coffee-script@1.12.4, json-stable-stringify@1.0.1, url@0.10.3, socket.io-client@1.7.3, srv-failover@1.3.0, node-rsa@0.2.30)
```

- Device: IO Plugin
  - Arduino/Firmata: firmata
  - Raspberry Pi: raspi-io
  - BeagleBone Black: beaglebone-io
  - C.H.I.P.: chip-io
  - Galileo/Edison: galileo-io
  - Blend Micro: blend-micro-io
  - LightBlue Bean:	bean-io
  - Electirc Imp: imp-io
  - Particle(Spark) Core: particle-io

```sh
root@edison:~/nodered# ls node_modules/
galileo-io  mraa  node-red  node-red-contrib-gpio
root@edison:~/nodered# 
```

### node-red-node-intel-gpio

> A Node-RED node to talk to an Intel Galileo or Edison using mraa

- [NPM JS node-red-node-intel-gpio](https://www.npmjs.com/package/node-red-node-intel-gpio)
- [node-red-node-intel-gpio](http://flows.nodered.org/node/node-red-node-intel-gpio)

```sh
root@edison:~/nodered# npm install node-red-node-intel-gpio
```

```sh
-\|/-\|/-\|/-\|/-\|/-\node-red-node-intel-gpio@0.0.5 node_modules/node-red-node-intel-gpio
```

```sh
root@edison:~/nodered# ls node_modules/
galileo-io  mraa  node-red  node-red-contrib-gpio  node-red-node-intel-gpio
root@edison:~/nodered# 
```

### node-red-contrib-grove-edison

> Node-RED nodes for Grove sensors used with the Intel Edison board

```sh
root@edison:~/nodered# npm install node-red-contrib-grove-edison
-\|/-\|/-\|/-\|/-\|/-node-red-contrib-grove-edison@0.1.1 node_modules/node-red-contrib-grove-edison
root@edison:~/nodered# 
```

```sh
root@edison:~/nodered# ls node_modules/
galileo-io  node-red-contrib-gpio
mraa        node-red-contrib-grove-edison
node-red    node-red-node-intel-gpio
root@edison:~/nodered# 
```


### node-red-contrib-upm

> Node-RED nodes to talk to sensors supported by the UPM library

```sh
root@edison:~/nodered# npm install node-red-contrib-upm
```

```sh
-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|node-red-contrib-upm@0.3.2 node_modules/node-red-contrib-upm
```

```sh
root@edison:~/nodered# ls node_modules/
galileo-io  node-red-contrib-gpio          node-red-node-intel-gpio
mraa        node-red-contrib-grove-edison
node-red    node-red-contrib-upm
root@edison:~/nodered# 
```

### node-red-node-watson

> A collection of Node-RED nodes for IBM Watson services

```sh
root@edison:~/nodered# npm install node-red-node-watson
```

```sh
\|/-\|/-\|/-\|/-\|/-\|/-\|/-npm WARN engine node-red-node-watson@0.5.0: wanted: {"node":">=4.5.0"} (current: {"node":"4.4.3","npm":"2.15.1"})
-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\d
 /-\|/-\|/-\|/-\|/-\|/--\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/--\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|
> websocket@1.0.24 install /home/root/nodered/node_modules/node-red-node-watson/node_modules/watson-developer-cloud/node_modules/websocket
> (node-gyp rebuild 2> builderror.log) || (exit 0)
...
��├��─��─ async@1.5.2
��├��─��─ alchemy-api@1.3.3
��├��─��─ qs@6.3.1
��├��─��─ temp@0.8.3 (os-tmpdir@1.0.2, rimraf@2.2.8)
��├��─��─ is-docx@0.0.3 (ooxml-type@0.0.1)
��├��─��─ request@2.53.0 (tunnel-agent@0.4.3, aws-sign2@0.5.0, forever-agent@0.5.2, caseless@0.9.0, oauth-sign@0.6.0, stringstream@0.0.5, isstream@0.1.2, json-stringify-safe@5.0.1, node-uuid@1.4.7, qs@2.3.3, to)
��├��─��─ image-type@2.1.0 (file-type@3.9.0, meow@3.7.0)
��├��─��─ file-type@2.12.0 (read-chunk@1.0.1, meow@3.7.0)
��├��─��─ cfenv@1.0.4 (ports@1.1.0, underscore@1.8.3, js-yaml@3.7.0)
��├��─��─ watson-developer-cloud@2.25.0 (cookie@0.3.1, vcap_services@0.2.0, isstream@0.1.2, extend@3.0.0, string@3.3.3, csv-stringify@1.0.4, object.omit@2.0.1, object.pick@1.2.0, buffer-from@0.1.1, request@2.79)
��└��─��─ kuromoji@0.0.5 (doublearray@0.0.2, zlibjs@0.2.0)
```

```sh
root@edison:~/nodered# ls node_modules/galileo-io  node-red-contrib-gpio          node-red-node-intel-gpio
mraa        node-red-contrib-grove-edison  node-red-node-watson
node-red    node-red-contrib-upm
root@edison:~/nodered# 
```

### node-red-contrib-play-audio

> A node-red node for playing audio in the browser

```sh
root@edison:~/nodered# npm install node-red-contrib-play-audio
```

```sh
-\|/-\|/-\|/-\|/node-red-contrib-play-audio@2.2.2 node_modules/node-red-contrib-play-audio
```

```sh
root@edison:~/nodered# ls node_modules/
galileo-io             node-red-contrib-grove-edison  node-red-node-watson
mraa                   node-red-contrib-play-audio
node-red               node-red-contrib-upm
node-red-contrib-gpio  node-red-node-intel-gpio
root@edison:~/nodered# 
```

# node-red-bluemix-nodes 

> A collection of extra Node-RED nodes for IBM Bluemix.

```sh
root@edison:~/nodered# npm install node-red-bluemix-nodes
```

```sh
-\|/-\|/-\|/-\|-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\-\|/-\-\|/-\|/-\|/-\|/-\|/-\-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/--\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/d
-\|/-\|/-\|/-\|/-\|/-\|-\|/-\|/-\|-\|/-\|/-\|-\|/-\|/-\|/-\-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|/-\|-\|-\|/-node-red-bluemix-nodes@1.1.9 node_modules/node-red-bluemix-nodes
��├��─��─ xml2js@0.4.17 (sax@1.2.2, xmlbuilder@4.2.1)
��├��─��─ when@3.7.8
��├��─��─ cfenv@1.0.4 (ports@1.1.0, underscore@1.8.3, js-yaml@3.7.0)
��├��─��─ request@2.79.0 (aws-sign2@0.6.0, tunnel-agent@0.4.3, forever-agent@0.6.1, oauth-sign@0.8.2, is-typedarray@1.0.0, caseless@0.11.0, stringstream@0.0.5, aws4@1.6.0, isstream@0.1.2, json-stringify-safe@5.)
��├��─��─ mongodb@2.2.24 (es6-promise@3.2.1, readable-stream@2.1.5, mongodb-core@2.1.8)
��├��─��─ twilio@1.11.1 (underscore@1.8.3, scmp@0.0.3, jwt-simple@0.1.0, q@0.9.7, request@2.27.0)
��├��─��─ mqlight@2.0.2016111400 (uuid@2.0.3, nopt@3.0.6, debug@2.6.1, npmlog@2.0.4, amqp10-link-cache@1.2.2, amqp10@3.4.2, moment@2.14.1)
��└��─��─ lodash@4.17.4
```

```sh
root@edison:~/nodered# ls node_modules/
galileo-io              node-red-contrib-gpio          node-red-node-intel-gpio
mraa                    node-red-contrib-grove-edison  node-red-node-watson
node-red                node-red-contrib-play-audio
node-red-bluemix-nodes  node-red-contrib-upm
root@edison:~/nodered# 
```

## Node-RED Node Modules List

```sh
root@edison:~/nodered# ls /usr/lib/node_modules/
iotkit                    jsupm_grovewater  jsupm_mq303a
iotkit-agent              jsupm_grovewfs    jsupm_my9221
iotkit-comm               jsupm_guvas12d    jsupm_nlgpio16
jsupm_a110x               jsupm_h3lis331dl  jsupm_nrf24l01
jsupm_ad8232              jsupm_h803x       jsupm_nrf8001
jsupm_adafruitms1438      jsupm_hcsr04      jsupm_nunchuck
jsupm_adafruitss          jsupm_hdxxvxta    jsupm_otp538u
jsupm_adc121c021          jsupm_hlg150h     jsupm_ozw
jsupm_adis16448           jsupm_hm11        jsupm_pca9685
jsupm_ads1x15             jsupm_hmc5883l    jsupm_pn532
jsupm_adxl335             jsupm_hmtrp       jsupm_ppd42ns
jsupm_adxl345             jsupm_hp20x       jsupm_pulsensor
jsupm_adxrs610            jsupm_ht9170      jsupm_rfr359f
jsupm_am2315              jsupm_htu21d      jsupm_rgbringcoder
jsupm_apa102              jsupm_hwxpxx      jsupm_rhusb
jsupm_apds9002            jsupm_hx711       jsupm_rotaryencoder
jsupm_apds9930            jsupm_i2clcd      jsupm_rpr220
jsupm_at42qt1070          jsupm_ili9341     jsupm_servo
jsupm_biss0001            jsupm_ina132      jsupm_si1132
jsupm_bma220              jsupm_interfaces  jsupm_si114x
jsupm_bmi160              jsupm_isd1820     jsupm_si7005
jsupm_bmp280              jsupm_itg3200     jsupm_sm130
jsupm_bmpx8x              jsupm_joystick12  jsupm_smartdrive
jsupm_bno055              jsupm_kxcjk1013   jsupm_ssd1351
jsupm_buzzer              jsupm_l298        jsupm_st7735
jsupm_cjq4435             jsupm_l3gd20      jsupm_stepmotor
jsupm_cwlsxxa             jsupm_ldt0028     jsupm_sx1276
jsupm_dfrph               jsupm_lm35        jsupm_sx6119
jsupm_ds1307              jsupm_lol         jsupm_t3311
jsupm_ds1808lc            jsupm_loudness    jsupm_t6713
jsupm_ds18b20             jsupm_lp8860      jsupm_ta12200
jsupm_ds2413              jsupm_lpd8806     jsupm_tcs3414cs
jsupm_ecs1030             jsupm_lsm303      jsupm_teams
jsupm_enc03r              jsupm_lsm9ds0     jsupm_tex00
jsupm_flex                jsupm_m24lr64e    jsupm_th02
jsupm_gas                 jsupm_max31723    jsupm_tm1637
jsupm_gp2y0a              jsupm_max31855    jsupm_tsl2561
jsupm_grove               jsupm_max44000    jsupm_ttp223
jsupm_grovecollision      jsupm_max44009    jsupm_ublox6
jsupm_groveehr            jsupm_max5487     jsupm_uln200xa
jsupm_groveeldriver       jsupm_maxds3231m  jsupm_urm37
jsupm_groveelectromagnet  jsupm_maxsonarez  jsupm_vcap
jsupm_groveemg            jsupm_mcp9808     jsupm_waterlevel
jsupm_grovegprs           jsupm_mg811       jsupm_wheelencoder
jsupm_grovegsr            jsupm_mhz16       jsupm_wt5001
jsupm_grovelinefinder     jsupm_mic         jsupm_xbee
jsupm_grovemd             jsupm_micsv89     jsupm_yg1006
jsupm_grovemoisture       jsupm_mlx90614    jsupm_zfm20
jsupm_groveo2             jsupm_mma7455     mraa
jsupm_grovescam           jsupm_mma7660     npm
jsupm_grovespeaker        jsupm_mpl3115a2   wyliodrin
jsupm_groveultrasonic     jsupm_mpr121
jsupm_grovevdiv           jsupm_mpu9150
root@edison:~/nodered# 
```

## Node-RED Execution

```sh
root@edison:~/nodered# node_modules/node-red/bin/node-red-pi
```

```sh
4 Mar 04:34:38 - [info] 

Welcome to Node-RED
===================

4 Mar 04:34:38 - [info] Node-RED version: v0.16.2
4 Mar 04:34:38 - [info] Node.js  version: v4.4.3
4 Mar 04:34:38 - [info] Linux 3.10.98-poky-edison+ ia32 LE
4 Mar 04:34:42 - [info] Loading palette nodes
4 Mar 04:35:08 - [warn] ------------------------------------------------------
4 Mar 04:35:08 - [warn] [rpi-gpio] Info : Ignoring Raspberry Pi specific node
4 Mar 04:35:08 - [warn] [tcp] Error: tcp in already registered
4 Mar 04:35:08 - [warn] [udp] Error: udp out already registered
4 Mar 04:35:08 - [warn] [upm-curieimu] Error: Cannot find module 'jsupm_curieimu'
4 Mar 04:35:08 - [warn] [upm-grove-button] Error: UPM-Grove-Button already registered
4 Mar 04:35:08 - [warn] [upm-grove-led] Error: upm-grove-led already registered
4 Mar 04:35:08 - [warn] [upm-grove-light] Error: upm-grove-light already registered
4 Mar 04:35:08 - [warn] [upm-grove-relay] Error: UPM-Grove-Relay already registered
4 Mar 04:35:08 - [warn] [upm-grove-rgb-lcd] Error: upm-grove-rgb-lcd already registered
4 Mar 04:35:08 - [warn] [upm-grove-rotary] Error: upm-grove-rotary already registered
4 Mar 04:35:08 - [warn] [upm-grove-sound] Error: upm-grove-sound already registered
4 Mar 04:35:08 - [warn] [upm-grove-temperature] Error: upm-grove-temperature already registered
4 Mar 04:35:08 - [warn] [upm-grove-servo] Error: upm-grove-servo already registered
4 Mar 04:35:08 - [warn] [upm-curieimu] Error: Cannot find module 'jsupm_curieimu'
4 Mar 04:35:08 - [warn] ------------------------------------------------------
4 Mar 04:35:08 - [info] Settings file  : /home/root/.node-red/settings.js
4 Mar 04:35:08 - [info] User directory : /home/root/.node-red
4 Mar 04:35:08 - [info] Flows file     : /home/root/.node-red/flows_edison.json
4 Mar 04:35:08 - [info] Creating new flow file
4 Mar 04:35:08 - [info] Starting flows
4 Mar 04:35:08 - [info] Started flows
4 Mar 04:35:08 - [info] Server now running at http://127.0.0.1:1880/
```

Go to http://board.ip.adress:1880/#

Loook at the installed __UI Nodes__

- Input
- Output
- Function
- social
- Storage
- Analysis
- Advanced
- Weather
- Smart_Process
- grove
- UPM_Sensors
- Intel_gpio
- IBM_Watson
- Watson_Deprecated