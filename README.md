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

## Support lib setup

You'll have to set up the required android support libraries to get this sample working. The project file (eclipse) contains a local reference to my system set up. Fix that first. The jars are included here. The library project isn't.

* add android-support-v7-appcompat as a library project
* and android-support-v7-appcompat.jar to libs folder
* replace android-support-v4.jar in libs folder
* clean build

## TODO

Some open points listed here

* use proper own namespace attr and styles for pre lvl 14, see: http://stackoverflow.com/questions/17261230/navigation-drawer-not-working-on-pre-ics-versions
* fix invalidateOptionsMenu() calls

## More info

* about nav drawer: http://developer.android.com/training/implementing-navigation/nav-drawer.html
* about actionbar compat: http://developer.android.com/guide/topics/ui/actionbar.html
* setting up support lib: http://developer.android.com/tools/support-library/setup.html
