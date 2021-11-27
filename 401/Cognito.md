# Read: 36 - Cognito

Amplify Provides the android developer with an easy way to make Authentication to the users. 

To start the Authentication to your android app, follow these steps: 

- execute this command in your terminal:

(amplify add auth)

- it will give you some additional stuff like user name and other things.. write it.

- push your changes to the cloud, execute this command:

(amplify push)

-Install Amplify Libraries by adding the library:
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.30.0'
}

-Initialize Amplify Auth
Add the Auth plugin before calling Amplify.configure. Update the code you added in Prerequisites:

``` java
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```
We can now check the current auth session.



