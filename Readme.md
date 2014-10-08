Realm-Releases
==============

[Realm.io](https://realm.io) compiled releases to be used as a git submodule in swift

Go to [static.realm.io/downloads/cocoa/latest](http://static.realm.io/downloads/cocoa/latest) for the latest release download if it's not here.

This leaves out documentation. Head over to [realm.io/docs/cocoa](http://realm.io/docs/cocoa) for that!

## How to use

in your project's directory run:

`git submodule add https://github.com:t413/Realm-Releases.git`

- Now drag Realm.framework from the Realm-Releases/ directory to the File Navigator in your Xcode project.
- Don't copy items! They're already in your project folder.
- Click on your project in the Xcode File Navigator. Select your app’s target and go to the Build Phases tab.
  * Under Link Binary with Libraries press + and add libc++.dylib.
  * Now click + and add Realm.framework
- Click the little (easily missed) + button in the bar under General, Build Phases, etc. and add a **New Copy Files Phase**
  * Double click the title and rename it "Copy Frameworks"
  * Change destination to Frameworks
  * Add Realm.framework
- Add RLMSupport.swift to your target
