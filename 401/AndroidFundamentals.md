# Android Fundamentals :


- you can write Android apps using Kotlin, Java, and C++ programming languages.
- there are more than one suffix for android app :
  - (.apk) suffix, contains the contents that is required at runtime.
  - (.aab) suffix, contains  some additional metadata that is not required at runtime. 


- sandbox is the way to let android apps have security.
  - The Android operating system is a multi-user Linux system in which each app is a different user.
  - By default, the system assigns each app a unique Linux user ID.
  - Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
  - By default, when any of the app's components need to be executed, and then shuts down the process when it's no longer needed.


## Anroid app components:
There are four different types of app components:

- Activities:
it is the type that allow the user to interact with the app, so he can do things and see some stuff.

Services:
it is the type that allow theuser to use it along with multiple other apps, such as the apps that allow you to listen to music while being in another app.

Broadcast receivers:
to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements
Content providers:
it holds thee data in an SQLite data base.

/////
Intents bind individual components together at runtime. to make an Intent  use the intent object , which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).

/////

AndroidManifest.xml. (to start any component, this file needs to read the manifest).
for example: 
``` java
<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
        <activity android:name="com.example.project.ExampleActivity"
                  android:label="@string/example_label" ... >
        </activity>
        ...
    </application>
</manifest>
```
