# Intent Filters

## Allowing Other Apps to Start Your Activity

To allow other apps to start your activity by performing an action that might be useful from this app, you need to add an `<intent-filter>` element in your manifest file for the corresponding `<activity>` element.

the system identifies your intent filters and adds the information to an internal catalog of intents supported by all installed apps. When an app calls `startActivity()` or `startActivityForResult()`, with an implicit intent, the system finds which activity (or activities) can respond to the intent.

### Add an Intent Filter

The system may send a given Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent object.

**[Action]**

Specify this in your intent filter with the `<action>` element. The value you specify in this element must be the full string name for the action, instead of the API constant.

**[Data]**

A description of the data associated with the intent.
Specify this in your intent filter with the `<data>`element. Using one or more attributes in this element, indicate the data type accepted.

**[Category]**

Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started.

```java
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
```

> **Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the `<action>`, `<category>`, and`<data>` elements in each `<intent-filter>`.**

> **If any two pairs of action and data are mutually exclusive in their behaviors, you should create separate intent filters to specify which actions are acceptable when paired with which data types.**

### Handle the Intent in Your Activity

As your activity starts, call `getIntent()` to retrieve the Intent that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as `onCreate()` or `onStart()`.

### Return a Result

If you want to return a result to the activity that invoked yours, simply call `setResult()` to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call `finish()` to close (and destroy) your activity.