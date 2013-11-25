Basic sap.m app using new Component model (> 1.16)
==================================================

Code formatting convention: 4 spaces for html and javascript.

Notes:
1. As-is this app makes a GET request to a non-existent Component-preload.js file in the apps root directory. If you add sap-ui-preload="auto" to the URL this GET request goes away! Strangely - adding it as data-sap-ui-preload="auto" to the bootstrap script does not make it go away.
2. Properties files. Even though we use messageBundle.properties to store texts, sapui5 still makes GET requests for more *specific* language files: messageBundle.en\_US.properties and messageBundle.en.properties. Strangely it also looks for a messagebundle.en\_US.properties file with a lowever case "b" even though we do not specify this name (in the sapui5 resources directory)! This issue can be eliminated by deploying the app as a java web archive (WAR) where the Resource Proxy servlet is used. See online help.

[SAP Online Help 7.40 for SAPUI5](http://help.sap.com/saphelp_nw74/helpdata/de/3c/d54c49e74548d2a61cab7e880b0051/content.htm?frameset=/de/91/f1e3626f4d1014b6dd926db0e91070/frameset.htm)
