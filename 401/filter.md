# Read: 41 - Intent Filters
when anyone watches a youtube video, and decide to share it with others, when he/she clicks the button to share, multible apps apears to chare the video on, such as facebook and instgram and others. Notice that all of the apps can share that kind of data(videos). in order to do so in your app you should make a filter intent so what is it?
 
 
 ![filter intent](https://i.stack.imgur.com/QbXZS.png)
**filter intent**:  being prepared to respond to action requests by specifying the appropriate intent filter in your activity between the apps.
 how to add it? 
  - add an <intent-filter> element in your manifest file for the corresponding <activity> element.
  - to properly define which intents your activity can handle, each intent filter you add should be as specific as possible in terms of the type of action and data the activity accepts.
   - Action
A string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.
Specify this in your intent filter with the <action> element. The value you specify in this element must be the full string name for the action, instead of the API constant (see the examples below).

  - Data
A description of the data associated with the intent.
Specify this in your intent filter with the <data> element. Using one or more attributes in this element, you can specify just the MIME type, just a URI prefix, just a URI scheme, or a combination of these and others that indicate the data type accepted.
 
  - Category
Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started. There are several different categories supported by the system, but most are rarely used. However, all implicit intents are defined with CATEGORY_DEFAULT by default.
Specify this in your intent filter with the <category> element.

In your intent filter, you can declare which criteria your activity accepts by declaring each of them with corresponding XML elements nested in the <intent-filter> element.

  
  - get the data:
  
  
``` java
  @Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);

    setContentView(R.layout.main);

    // Get the intent that started this activity
    Intent intent = getIntent();
    Uri data = intent.getData();

    // Figure out what to do based on the intent type
    if (intent.getType().indexOf("image/") != -1) {
        // Handle intents with image data ...
    } else if (intent.getType().equals("text/plain")) {
        // Handle intents with text ...
    }
}
```
  
  Return a Result:
  
  ``` java
  
  // Create intent to deliver some kind of result data
Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
setResult(Activity.RESULT_OK, result);
finish();
  ```
  
