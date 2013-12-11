menu-drawer-compat-example
==========================

Example project for ActionBar Compat and Menu Drawer tested on API level 7 (Android 2.1)

## Screenshot

Visit [this link](https://www.dropbox.com/s/w43z6yk23ldz5rh/device-2013-08-19-031443.png). 

## Changes required from demo app

I started from [the sample menu drawer app](http://developer.android.com/shareables/training/NavigationDrawer.zip) from [the official Navigation Drawer Documentation](http://developer.android.com/training/implementing-navigation/nav-drawer.html). That sample project requires API level 14 though. The following is a quick overview of what I had to change to get this working with everything from API level 11 and up.

* update theme
* add compat libraries
* extend ActionBarActivity
* change imports
* clean up layout drawer

## update theme

In your manifest update the application tag to include the following compat theme.

   <application
        android:label="@string/app_name"
        android:icon="@drawable/ic_launcher"
        android:theme="@style/Theme.AppCompat">
        
## Add compat libraries

### Support lib libraries

* and android-support-v7-appcompat.jar to libs folder
* replace android-support-v4.jar in libs folder

You'll have to set up the required android support libraries to get this sample working. The project file (eclipse) contains a local reference to my system set up. Fix that first. The jars are included on this project in the libs folder.

### Compat Project setup

* add android-support-v7-appcompat as a library project

The compat library project isn't included here. You can find it in your SDK folder. First import that as an Android project (eclipse File menu > import > android > existing android project) from:

   SDK_PATH/extras/android/support/v7/appcompat

Now you can add this android project as a dependency on your project.

## Update imports

Only for existing projects. In your source files replace the imports to match all support packages.

## TODO

Some open points listed here

* use proper own namespace attr and styles for pre lvl 14, see: http://stackoverflow.com/questions/17261230/navigation-drawer-not-working-on-pre-ics-versions
* fix invalidateOptionsMenu() calls => use support version

## More info

* about nav drawer: http://developer.android.com/training/implementing-navigation/nav-drawer.html
* about actionbar compat: http://developer.android.com/guide/topics/ui/actionbar.html
* setting up support lib: http://developer.android.com/tools/support-library/setup.html
