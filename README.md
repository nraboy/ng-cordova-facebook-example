Facebook Oauth Example For Ionic Framework
==============================

This example will demonstrate how to use ngCordova to authenticate with Facebook and retrieve
an access token for use with the Facebook REST API.


Requirements
-------------

* Apache Cordova 3.5+
* [Apache Cordova InAppBrowser Plugin](http://cordova.apache.org/docs/en/3.0.0/cordova_inappbrowser_inappbrowser.md.html)
* [Apache Cordova White-list Plugin](https://github.com/apache/cordova-plugin-whitelist)
* [ngCordova](http://www.ngcordova.com)


Configuration
-------------

Download this example project from GitHub and run the following commands:

    $ ionic platform add android
    $ cordova plugin add org.apache.cordova.inappbrowser
    $ cordova plugin add cordova-plugin-whitelist

The above commands will add the Android build platform and install the required Apache InAppBrowser plugin.

This example application requires you to have your own Facebook application registered with Facebook.com.  Doing so
will give you a unique client id that can be included into your project.  When registering your application with Facebook,
make sure to set the callback uri to **http://localhost/callback**, otherwise ngCordova will not function.

With the client id in hand, open **www/js/app.js** and find the following line:

    $cordovaOauth.facebook("CLIENT_ID_HERE", ["email", "read_stream", "user_website", "user_location", "user_relationships"])

You will want to replace **CLIENT_ID_HERE** with the official key.


Usage
-------------

With this example project configured on your computer, run the following from the Terminal or command prompt:

    $ ionic build android

Install the application binary to your device or simulator.

The application is currently composed of three parts and makes use of two of the official Facebook RESTful APIs.

1. Oauth sign in
2. Basic profile (GET /me)
3. Basic stream (GET /me/feed)

You will be required to sign into the application using your own Facebook username and password.  Once logged in, you can
view very basic information found in your profile or navigate to your stream.  The stream will show posts with a comment and
like count.


Version History
-------------

0.0.1

* Add: oauth sign in
* Add: view profile
* Add: view feed of recent entries


Have a question or found a bug (compliments work too)?
-------------

Tweet me on Twitter - [@nraboy](https://www.twitter.com/nraboy)


Resources
-------------

Ionic Framework - [http://www.ionicframework.com](http://www.ionicframework.com)

AngularJS - [http://www.angularjs.org](http://www.angularjs.org)

Apache Cordova - [http://cordova.apache.org](http://cordova.apache.org)

ngCordova - [http://www.ngcordova.com](http://www.ngcordova.com)

Nic Raboy's Code Blog - [https://blog.nraboy.com](https://blog.nraboy.com)
