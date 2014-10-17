Build and Deploy the Example
----------------------------

First follow the general example located in this [README](../README.md)

## Change Push Configuration

In ```www/push-config.json``` change ```"pushServerURL"``` with the url of your AeroGear UnifiedPush Server instance. You also need to change ```"senderID"```, ```"variantID"``` and ```"variantSecret"``` with the values assigned by UnifiedPush Server and GCM or APNS:

```javascript
{
   "pushServerURL": "<pushServerURL e.g http(s)//host:port/context >",
   "android": {
      "senderID": "<senderID e.g Google Project ID only for android>",
      "variantID": "<variantID e.g. 1234456-234320>",
      "variantSecret": "<variantSecret e.g. 1234456-234320>"
   },
   "ios": {
      "variantID": "<variantID e.g. 1234456-234320>",
      "variantSecret": "<variantSecret e.g. 1234456-234320>"
   }
}


```

You can also copy/paste these settings from your UnifiedPush console

You'll also need to install the war file and add the url of your jboss to the www/js/app.js file. Be sure that it must be reachable from your device so start jboss-as with `-b 0.0.0.0` and use and ip or hostname and not `localhost`

```javascript
//app.js    
CONTACTS.app.baseUrl = "< backend URL e.g http(s)//host:port >/jboss-contacts-mobile-picketlink-secured/";

```
