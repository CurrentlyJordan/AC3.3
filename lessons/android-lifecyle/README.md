## The Android Lifecycle

#### Objective

Students will be able to understand the Android Activity Lifecycle and how to use lifecycle methods.

#### Do Now (Morning)

Finish working on [yesterday's exercises](https://github.com/shurane/unit-1-android-resource-exercises).
If you're done, help someone who isn't finished.

#### Code Review

[Code Review Rubric](https://github.com/accesscode-2-1/user-manual/blob/master/code-review-rubric.md)

#### Review of Android Resource Exercises

#### Do Now (Afternoon)

Download [ActivityLifecycle.zip](http://developer.android.com/training/basics/activity-lifecycle/index.html) and
play with/look at the sample app.

#### Tech Industry Chat

#### Android LifeCycle

An Activity is an Android object that represents one single task a user can do. The Activity Lifecycle methods are called depending on the current state of the Activity. This is not controlled by the application developer. The developer is given some guarantees (for example, that `onCreate` is called before `onStart`) but besides that must write these methods with all sorts of user interactions in mind. These are the lifecycle methods:
* `onCreate` is called when the Activity is first created - performs any necessary setup
* `onStart` and `onResume` are called when the Activity is first made visible.
* `onResume` is called anytime an Activity is made visible
* `onPause` is called anytime an Activity is made only partially visible
* `onStop` is called when an Activity is no longer visible to the user - can be followed by either `onRestart` or `onDestroy`.
* `onRestart` is called when a stopped Activity becomes active again.
* `onDestroy` is called to Destroy an Acivity.

The system may also kill an Activity. When this happens, any state about the activity is passed in a [`Bundle`](http://developer.android.com/reference/android/os/Bundle.html). Information about the View hierarchy is typically saved by `onSaveInstanceState`. You can implement this method in order to save more information about the current Activity state using key-value pairs. You can then restore state either in `onCreate` or in `onRestoreInstanceState`, which is called after `onStart` when restoring the Activity.
