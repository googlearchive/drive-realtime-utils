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

## Contributing

Before creating a pull request, please fill out either the individual or corporate Contributor License Agreement.

If you are an individual writing original source code and you're sure you own the intellectual property, then you'll need to sign an individual CLA.
If you work for a company that wants to allow you to contribute your work to this client library, then you'll need to sign a corporate CLA.
Follow either of the two links above to access the appropriate CLA and instructions for how to sign and return it. Once we receive it, we'll add you to the official list of contributors and be able to accept your patches.