Connect to the tomato router
Open Putty or any other ssh tool
Address is the ip of the router (for example 192.168.99.1) 
Port is 22
username is root
password is admin
type the following commands:
++++++++++++++++++++++++++++
rm /tmp/splashd/splash.html    (enter)
cd /tmp/splashd/    (enter)
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/splash.html   (enter)
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/bg.jpg   (enter)
nvram commit   (enter)
reboot     (enter)
++++++++++++++++++++++++++++

You can change username and password in the splash.html file like this :
+++++++++++++++++++++++++++
vi /tmp/splashd/splash.html    (enter)
:3491    (enter)  - Then modify the username an password (default is 12 and 12)
:wq    (enter)
nvram commit   (enter)
reboot     (enter)
+++++++++++++++++++++++++++
Scroll to line 3491
