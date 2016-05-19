node-fcm
========
An interface for "Firebase Cloud Messaging for Android" on Node.js

## Installation

Via [npm](https://www.npmjs.com/package/fcm):

    $ npm install fcm


## Usage

    var FCM = require('fcm').FCM;

    var apiKey = '';
    var fcm = new FCM(apiKey);

    var message = {
        registration_id: 'Device registration id', // required
        collapse_key: 'Collapse key', 
        'data.key1': 'value1',
        'data.key2': 'value2'
    };
    
    fcm.send(message, function(err, messageId){
        if (err) {
            console.log("Something has gone wrong!");
        } else {
            console.log("Sent with message ID: ", messageId);
        }
    });

See [FCM documentation](https://firebase.google.com/docs/cloud-messaging) for details.

