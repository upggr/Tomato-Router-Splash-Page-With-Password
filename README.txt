Connect to the tomato router
username is root
password is admin
Under Administration - Scripts - Wan Up, paste the following lines
++++++++++++++++++++++++++++
#!/bin/sh
cd /tmp/splashd
rm splash.html
rm style.css
rm jquery.min.js
rm bg.jpg
wget http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/splash.html
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/style.css
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/jquery.min.js
wget http://cdn.rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/bg.jpg
sed -i -e 's/demousername/demo/g' splash.html
sed -i -e 's/demopassword/demo/g' splash.html
sed -i -e 's/companyname/Your Hotel/g' splash.html
++++++++++++++++++++++++++++

You can change username and password if you replace the "demo" value above with the required username and password.
For example if you want the username to be :User1 and the password to be :Password1 and the title to be "My Hotspot", the last 3 lines in the above script should be :
sed -i -e 's/demousername/User1/g' splash.html
sed -i -e 's/demopassword/Password1/g' splash.html
sed -i -e 's/companyname/My Hotspot/g' splash.html

(Obviously the default script will be demo:demo as username and password)

You can also change the photo that displays as the background by modifying the line that references the jpg file. For example if this is a hotel, just grab their background there in the url.

Unfortunately I could not link directly to my github files as the busybox does not support https, so I resorted using rawgit. Keep this in mind if you decide to use your own image, needs to be served from http.

You can preview the login page here : http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/splash.html

