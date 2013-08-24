
# Rapid Android dev/prototyping techniques

### Leveraging IntelliJ/Eclipse UI Editors

#### Theming

- [Android Holo Color Generator](http://android-holo-colors.com/)
- [Android Action Bar Style Generator](http://jgilfelt.github.io/android-actionbarstylegenerator/)

#### GitStepping

You can follow along the various steps on github.

#### ActionBar

Demo 

* http://developer.android.com/design/patterns/actionbar.html
* http://developer.android.com/guide/topics/ui/actionbar.html
* http://developer.android.com/guide/topics/ui/menus.html

#### Hamburger

Demo


### Using Genymotion for super fast feedback loops.

Pros:

- Blazingly fast, faster than real device.
- (Integration tests at x10 speeds? Yes please.)
- Perfect for product demos on projectors
- Acts like a real device 
	- Access to Play Store
	- Syncs with your google account

Caveats:

- You might have to wait for support of new Android versions. 
- Fixed! ~~Current version has softkeyboard/hardkey bugs (overflow a problem)~~ 
- When using NDK/JNI you'll need to make sure to provide x86 libraries


### TL;DR
Quick, where's my .apk?? 

- Just run (ctrl-r) with your device as a target, or:
- From your project folder on the command line (Mac/Linux with properly configur):
	- `ant clean release`
	- `find . -name \*apk -ls` points to the useable .apk. 
	- `adb install your.apk` to install
	- `adb uninstall com.your.project.packagename your.apk` to uninstall


"Easy" wins when/if time permits

- BugSense
- Leveraging Google's Android APIs (Maps, push notifications, etc.)


## Pits of doom? 

- Like scrum? Use post-its, avoid time consuming task managers.
- ActionBarSherlock: we love it, but if you're lucky, by the time you have a shippable product, gingerbread will be dead. The time overhead might not be worth it.
- RoboGuice, RoboElectric are awesome, but in a hackathon, testing is probably not a priority, and while injection can make you faster, it won't if you have to teach everyone on your team how to use it.
