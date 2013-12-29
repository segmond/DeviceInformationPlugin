# DeviceInformation plugin for Phonegap #

This plugin allows you to retrieve most information about your Android devices that are available through Android's Telephony Manager class from your PhoneGap application.

## Adding the Plugin to your project ##

Using this plugin requires [Android PhoneGap](https://github.com/apache/incubator-cordova-android).

1. To install the plugin, copy the www/deviceinformation.js file to your project's www folder and include a reference to it in your html file after cordova.js.

    &lt;script type="text/javascript" charset="utf-8" src="phonegap.js"&gt;&lt;/script&gt;<br/>
    &lt;script type="text/javascript" charset="utf-8" src="deviceinformation.js"&gt;&lt;/script&gt;
    
2. Create a directory within your project called "src/com/vliesaputra/cordova/plugins" and copy src/com/vliesaputra/cordova/plugins/DeviceInformation.java into it.

3. In your res/xml/config.xml file add the following line:

    &lt;plugin name="DeviceInformation" value="com.vliesaputra.cordova.plugins.DeviceInformation"/&gt;

## Using the plugin ##

You create a new object that represents the plugin using cordova.require. Then you can call the 'get' method on that object providing a success callback which will be called with a result value that is a JSON object of all the information about your devices.

<pre>
  /**
    * Get the devices information.
    */
  get(success, failure)
</pre>

Sample use:

    var deviceInfo = cordova.require("cordova/plugin/deviceinformation");
    deviceInfo.get(function(result) {
            console.log("result = " + result);
        }, function() {
            console.log("error");
    });
    

## RELEASE NOTES ##

### December 29, 2013 ###

* Initial release


## BUGS AND CONTRIBUTIONS ##


## LICENSE ##

This plugin is available under the MIT License (2008). 
The text of the MIT license is reproduced below. 

---

### The MIT License

Copyright (c) &lt;2013&gt; Veronica Liesaputra

 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:

 The above copyright notice and this permission notice shall be included in
 all copies or substantial portions of the Software.

 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
 THE SOFTWARE.
 
