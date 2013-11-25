Basic sap.m app using new Component model (> 1.16).

Code formatting convention: 4 spaces for html and javascript.

Notes:
(1) As-is this app makes a GET request to a non-existent Component-preload.js file in the apps root directory. If you add sap-ui-preload="auto" to the URL this GET request goes away! Strangely - adding it as data-sap-ui-preload="auto" to the bootstrap script does not make it go away.

(2) Properties files. Even though we use messageBundle.properties to store texts, sapui5 still makes GET requests for more "specific" language files: messageBundle.en_US.properties and messageBundle.en.properties. Strangely it also looks for a messagebundle.en_US.properties file with a lowever case "b" even though we do not specify this name (in the sapui5 resources directory)!