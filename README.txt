Connect to the tomato router
username is root
password is admin
Under Administration - Scripts - Init, paste the following lines
++++++++++++++++++++++++++++
cd /tmp/splashd
rm splash.html
rm style.css
rm jquery.min.js
rm bg.jpg
wget http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/splash.html
wget http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/style.css
wget http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/jquery.min.js
wget http://rawgit.com/upggr/Tomato-Router-Splash-Page-With-Password/master/bg.jpg
sed -i -e 's/demousername/demo/g' splash.html
sed -i -e 's/demopassword/demo/g' splash.html
++++++++++++++++++++++++++++

You can change username and password if you replace the "demo" value above with the required username and password.
For example if you want the username to be :User1 and the password to be :Password1 the last 2 lines in the above script should be :
sed -i -e 's/demousername/User1/g' splash.html
sed -i -e 's/demopassword/Password1/g' splash.html

(Obviously the default script will be demo:demo as username and password)
