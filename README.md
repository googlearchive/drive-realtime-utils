# Google Drive Realtime API Utility

## Overview

The Google Drive Realtime API Utility is a lightweight JavaScript library aimed
at simplifying authentication to Google Drive as well as various other features.

Simply pass in an object with the following properties

1. **appId** - the appId of your project found in the developers console.
2. **clientId** - the clientId of your project found in the developers console.

You can instantiate the utility by running the following code.

```javascript
var util = new utils.RealtimeUtility({
	appId: 'YOUR APPID',
	clientId: 'YOUR CLIENTID'
});
```

After instantiating the utility, start the authorization process by calling
`start` and passing in a callback function for after authentication. `start`
also accepts a boolean parameter, true to use a popup or false to try and
authenticate without a popup.

After authentication, the realtime utiltiy has three helper functions. You can
create a new realtime file, load a realtime file, and also get a URL parameter.
The file

Check out the comments in the file to see the parameters and options for
each of these functions.