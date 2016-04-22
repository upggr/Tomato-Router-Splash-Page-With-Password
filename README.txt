Connect to the tomato router
Open Putty or any other ssh tool
Address is the ip of the router (for example 192.168.99.1) 
Port is 22
username is root
password is admin
type the following commands:
++++++++++++++++++++++++++++
rm /tmp/splashd/splash.html
rm /tmp/splashd/style.css
rm /tmp/splashd/bg.jpg
cd /tmp/splashd/
wget https://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/4e06b8d56437bb38a62f7dfc5396c845f56c73e8/splash.html
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/style.css
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/jquery.min.js
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/bg.jpg
nvram commit
reboot
++++++++++++++++++++++++++++

You can change username and password in the splash.html file like this :
+++++++++++++++++++++++++++
vi /tmp/splashd/splash.html
:68  - Then modify the username an password (default is 12 and 12)
:wq
nvram commit
reboot
+++++++++++++++++++++++++++
