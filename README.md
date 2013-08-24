
# Up and Running Hamburger Action

The goal of this project is to provide people new to the platform a "quick-start" project skeleton that shows off current Android development practices (as of summer 2013). 

## General concepts:

#### GitStepping

We're trying to use git as a teaching method. Basically we encourage beginners to examine the different steps that bring you from nothing to a complete project. We've tried hard to keep each step of the process explained in commit messages.

## Development concepts we introduce in the code:

#### ActionBar

Here are a few links to understand the ActionBar.

* [Design Pattern](http://developer.android.com/design/patterns/actionbar.html)
* [Dev Guide Entry](http://developer.android.com/guide/topics/ui/actionbar.html)
* [Dev Guide on Menus](http://developer.android.com/guide/topics/ui/menus.html), as they're linked to ActionBars when using the overflow button.

#### Hamburger

Hamburger is the name for the "three horizontal line" button icon we see used to summon up a navigation drawer. I picked up on that name from [this](https://twitter.com/markkawano/status/256848377260679168) twitter post and [this](http://jxnblk.tumblr.com/post/36218805036/hamburgers-basements-why-not-to-use-left-nav-flyouts) blog post. Interesting read if you can spare a few minutes.

These two posts are rather critical of the idea, but Google has officialized the concept with the [Navigation Drawer Design Pattern](http://developer.android.com/design/patterns/navigation-drawer.html). Here is a link to the [Navigation Drawer Developer Doc](http://developer.android.com/training/implementing-navigation/nav-drawer.html).


## Tools and libraries we use:

#### [SourceTree](http://www.sourcetreeapp.com/) client for Git (Mac/Windows)

I like it because it's free, it makes some Git concepts easier to understand for newbies (vs the command line), and it promotes the use of [Vincent Driessen's branching model](http://nvie.com/posts/a-successful-git-branching-model/).

As an added bonus it makes it easy to hook up to popular Git code repositories, both public (GitHub) or private (Bitbucket)

#### [Genymotion](http://www.genymotion.com/) Android Emulator

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

#### Theming tools

- [Android Holo Color Generator](http://android-holo-colors.com/)
- [Android Action Bar Style Generator](http://jgilfelt.github.io/android-actionbarstylegenerator/)


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

