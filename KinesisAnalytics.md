# Read: 43 - Kinesis & Analytics

 with Amplify Analytics you can record analytics event.
 
 how to set up my app :
 - run amplify add analytics
-select between these :
``` java 
? Select an Analytics provider (Use arrow keys)
    `Amazon Pinpoint`
? Provide your pinpoint resource name:
    `yourPinpointResourceName`
? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started)
    `Yes`
    ```
    
- then push.
- add this line to the dependencies :
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.30.0'
now amplifyconfiguration.json should be updated.

To initialize the Amplify Auth and Analytics you need to add some plugins on your onCreate :
 Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSPinpointAnalyticsPlugin(this));

now check your console : amplify console analytics
