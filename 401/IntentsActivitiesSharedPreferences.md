# Read: 27 - Intents, Activities, and SharedPreferences

While running the app, the tasks will be arranged in a stack so when we do more than one one task using one app, all the tasks will be collected in a stack. almost every app has the home page as a staring point and when the current activity starts another, the new activity is pushed on the top of the stack.
but the previous activity stays in the stack, Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack when started by the current activity and popped off when the user leaves it using the Back button or gesture
everyhtime the user hit on the back button he/ she will pop the activity out of the stack.
![alt text](https://developer.android.com/images/fundamentals/diagram_backstack.png)


## Multiple activity instances
if your app allows users to start a particular activity from more than one activity, a new instance of that activity is created and pushed onto the stack.

## Multi-window environments
When apps are running simultaneously in a multi-windowed environment, supported in Android 7.0 (API level 24) and higher, the system manages tasks separately for each window; each window may have multiple tasks. The same holds true for Android apps running on Chromebooks: the system manages tasks, or groups of tasks, on a per-window basis.

**BUT** what if you want to arrange the tasks in your own?
if you decided that you want to change the normal behavior.
with attributes in the <activity> manifest element and with flags in the intent that you pass to startActivity().
these are the principal <activity> attributes that you can use:
- taskAffinity. 
- launchMode.
- allowTaskReparenting.
- clearTaskOnLaunch.
- alwaysRetainTaskState.
- finishOnTaskLaunch.
(and more)
------------------------------
How to save the data? 
  
  - You can create a new shared preference file or access an existing one by calling one of these methods:

- getSharedPreferences() — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app.
- getPreferences() — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.
  When naming your shared preference files, you should use a name that's uniquely identifiable to your app. An easy way to do this is prefix the file name with your application ID. For example: "com.example.myapp.PREFERENCE_FILE_KEY"


  
