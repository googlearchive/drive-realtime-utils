# Google Drive Realtime API Utility

## Overview

The Google Drive Realtime API Utility is a lightweight JavaScript library aimed
at simplifying authentication to Google Drive as well as various other features.

Simply pass in an object with the following properties

1. **appId** - the appId of your project found in the developers console.

You can instantiate the utility by running the following code.

```javascript
var util = new utils.RealtimeUtils({
	appId: 'YOUR APPID',
});
```

After instantiating the utility, start the authorization process by calling
`authorize` and passing in a callback function for after authentication.
`authorize` also accepts a boolean parameter, true to use a popup or false to
try and authenticate without a popup.

After authentication, the realtime utiltiy has several helper functions.
Outlined below are the various functions and parameters that can be called.

## Documentation

### RealtimeUtils.authorize(onAuthComplete, usePopup)
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>onAuthComplete</td>
    <td>Function</td>
    <td>
      This function is a callback for the authorization process. Once completed,
      this function will be invoked. This function will have an authentication
      result object as an argument describing if the authentication was
      successful.
    </td>
  </tr>
  <tr>
    <td>usePopup</td>
    <td>boolean</td>
    <td>
      If true, the user will be prompted to authenticate via a popup. The
      general authentication flow should only require this if it is the first
      time the user has authenticated. Subsequent authentications will not
      require a popup.
    </td>
  </tr>
</table>

### RealtimeUtils.createRealtimeFile(title, callback)
This function will create a new Realtime file and store it in Google Drive.
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>title</td>
    <td>String</td>
    <td>
      The name of the newly created document. Note that all new files are
      created using the <code>'application/vnd.google-apps.drive-sdk'</code>
      mime type. To override this mimetype, pass in mimeType and a string value
      as an option when instantiating RealtimeUtils.
    </td>
  </tr>
  <tr>
    <td>callback</td>
    <td>Function</td>
    <td>
      This function will be invoked after the realtime file has been created in
      Drive. Note that you will still need to load a document after you have
      created one.
    </td>
  </tr>
</table>

### RealtimeUtils.load(documentId, onFileLoaded, initializeModel)
Load a new or existing document that is persisted in Google Drive.
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>documentId</td>
    <td>String</td>
    <td>
      The id of the document as stored in Drive.
    </td>
  </tr>
  <tr>
    <td>onFileLoaded</td>
    <td>Function</td>
    <td>
      The function that will be invoked after the file has been loaded. See the
      official <a href="https://devsite.googleplex.com/google-apps/realtime/reference/gapi.drive.realtime#.load">Realtime documentation</a>
      for more information regarding arguments.
    </td>
  </tr>
  <tr>
    <td>initializeModel</td>
    <td>Function</td>
    <td>
      If this is the first time this document has been opened, the Realtime
      model will be initialized. See the official <a href="https://devsite.googleplex.com/google-apps/realtime/reference/gapi.drive.realtime#.load">Realtime Documentation</a>
      for more information regarding arguments.
    </td>
  </tr>
</table>

### RealtimeUtils.getParam(urlParam)
A convenience function for accessing a parameter in the URL.
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>urlParam</td>
    <td>String</td>
    <td>
      The name of the parameter that is being retrieved from the URL.
    </td>
  </tr>
</table>


## Contributing

Before creating a pull request, please fill out either the individual or
corporate Contributor License Agreement.

* If you are an individual writing original source code and you're sure you
own the intellectual property, then you'll need to sign an
[individual CLA](http://code.google.com/legal/individual-cla-v1.0.html).
* If you work for a company that wants to allow you to contribute your work
to this client library, then you'll need to sign a
[corporate CLA](http://code.google.com/legal/corporate-cla-v1.0.html).

Follow either of the two links above to access the appropriate CLA and
instructions for how to sign and return it. Once we receive it, we'll add you
to the official list of contributors and be able to accept your patches.