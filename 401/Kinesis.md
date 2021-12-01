# Read: 39 - Kinesis


The Analytics category enables you to collect analytics data for your App. The Analytics category comes with built-in support for Amazon Pinpoint and Amazon Kinesis

to Start with it, add this command in your terminal:

amplify add analytics
``` java
then select one of these :
? Select an Analytics provider (Use arrow keys)
    `Amazon Pinpoint`
? Provide your pinpoint resource name:
    `yourPinpointResourceName`
? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started)
    `Yes`
```
then push.
add this dependency to your build.gradle (Module: app). :
``` java 
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.30.0'
```
add these plugins 
``` java
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSPinpointAnalyticsPlugin(this));
```

to view the work run this command: 
amplify console analytics

    
