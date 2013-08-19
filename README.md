menu-drawer-compat-example
==========================

Example project for ActionBar Compat and Menu Drawer tested on API level 7 (Android 2.1)

# changes required from demo app

update theme
add compat libraries
extend ActionBarActivity
change imports

# support lib setup

add android-support-v7-appcompat as a library project
and android-support-v7-appcompat.jar to libs folder
replace android-support-v4.jar in libs folder

clean build

# TODO

use proper own namespace attr and styles for pre lvl 14, see: http://stackoverflow.com/questions/17261230/navigation-drawer-not-working-on-pre-ics-versions

fix invalidateOptionsMenu() calls

# more info

about nav drawer: http://developer.android.com/training/implementing-navigation/nav-drawer.html
about actionbar compat: http://developer.android.com/guide/topics/ui/actionbar.html
setting up support lib: http://developer.android.com/tools/support-library/setup.html
