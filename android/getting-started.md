# Getting Started with Android

## Overview

### What You'll Learn

In this section, you'll learn

1. How to install Android Studio
2. How to create a project in Android Studio
3. What the different files are in an Android Studio project
4. How to run your project in the Android emulator

### Prerequisites

None!

### Introduction

In this section, we'll show how to install Android Studio, give you the tour of the different files in a project, and show you how to run it!

## Installing Android Studio

*Note:* The following directions are based on [those provided by Google](https://developer.android.com/studio/install).

### Windows

Go to the [download page](https://developer.android.com/studio) and download the Android Studio `.exe` file, then run it and install the SDK packages it recommends!

### MacOS

Grab the DMG from the [download page](https://developer.android.com/studio), launch it, and drag and drop Android Studio into the Applications folder.

### Linux

If you're running a 64-bit machine, make sure to install the following 32-bit libraries (yep, it's weird, but they're needed):

```
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
```

Then, visit the [download page](https://developer.android.com/studio), and download the `.tar.gz` archive. Move it to wherever you'd like, and unpack it using:

```
tar -xvf <the file you downloaded>
```

This command will extract the archive into an `android-studio` folder in your current directory. To run Android Studio, go into the `android-studio/bin/` folder and run:

```
./studio.sh
```

## Creating an Android Studio Project

Now that we've got Android Studio up and running, let's whip up a quick "Hello World!" project

1. Open Android Studio, and **click the *Create New Project* button**:

![create-proj](/home/lambda/repos/MobileDevelopmentWorkshop/android/create-proj.png)

2. You'll see that Android Studio comes with a ton of templates for projects right off the bat. For now, let's **just choose *Empty Activity*** -- this'll start us with a simple app and some "Hello World!" text.
3. Now, you'll be presented with a screen to set up some configuration for your project. The only things we'll worry about here are the *Name* and *Minimum SDK* fields.
   * *Name:* This just determines the name of your app, and the package and project names are altered to reflect this (I chose "Ye" for my app because I was just messing around -- in case you're confused by later photos).
   * *Minimum SDK:* This determines the minimum version of Android that your app can run on. Choose a version like 4.1 and you'll be able to install it on 99% of Androids, but you won't have any features that came it from versions 4.2 to 11! Going with the default is pretty safe here.
4. **Press *Finish*** and wait for the project to finish loading up -- you can see on the bottom of the screen if the IDE is still doing anything (e.g. Gradle takes a while to finish doing stuff). ***This will probably take several minutes when you open your first project!*** Your code won't be available to work with until much of these initial tasks are complete.
5. Now, you'll have a project ready for development! It's just a blank screen with "Hello World!" for now, but we'll get into doing stuff with it later!

## Tour of Your Android Project

Android Studio is built on the JetBrains IDE platform, so if you've ever used PyCharm or IntelliJ, things will look familiar; however, there are a number of significant differences from other IDEs.

![studio](/home/lambda/repos/MobileDevelopmentWorkshop/android/studio.png)

On the right, you can see the editor where we can interact with Java, XML, and other files. On the left, you'll see a file tree where we can navigate the files of our project.

In Android Studio, different files are presented differently in the editor. For example, if you click the tab in the upper left of the editor to open `activity_main.xml`, you'll be presented with the Layout Editor:

![layout](/home/lambda/repos/MobileDevelopmentWorkshop/android/layout.png)

In this case, Android Studio lets you define the layout of your app with a drag-and-drop editor instead of presenting you with the raw XML. We'll learn more about using this later on.

Let's expand the file tree and see what's actually in this project:

![files](/home/lambda/repos/MobileDevelopmentWorkshop/android/files.png)

Let's start from the top:

* `AndroidManifest.xml` - An incredibly important file. This file tells Android things like:
  * How many activities (or screens) your application has
  * What permissions your app needs in order to run
  * How other apps can integrate with yours (e.g. allowing your photo editing app to show up when working in the Photos app)
  * API keys
  * ...and much more.
* `MainActivity.java`  - This file contains the Java code associated with the empty activity the project starts out with. We'll discuss this a bit later.
* Don't worry about the `com.example.firstapp (androidTest)` folders -- we won't be covering them.
* `res/` - This folder contains all of the static resources your app uses -- everything from images to activity layouts to strings (yes, strings) are contained within this directory.
* `drawable` - Don't worry about it.
* `layout/` - This folder contains XML files that specify the layout of your Android activities (editable in the Layout Editor).
* `activity_main.xml` - This XML file determines the layout of the items on screen for the empty activity we've started with.
* `mipmap/` - Don't worry about it -- this just contains icons.
* `colors.xml` - This file defines names for colors to be used in the application's themes.
* `strings.xml` - This file defines names for strings to be used throughout the app.
  * It may seem ridiculous that you have to define a string here before using it on a label or something, but this makes localization much easier.
* `themes/` - This folder contains a couple XML files that define light and dark mode color schemes.

## Testing Your Project in the Android Emulator

Now that we know the lay of the land, let's run our app! It may not look like much, since we haven't added anything, but let's go for it anyway!

Near the top-center of the IDE, you should see this menu:

![run](/home/lambda/repos/MobileDevelopmentWorkshop/android/run.png)

This is where we can build and run our app -- I've already installed an emulator, so you might not see the *Pixel 2 API 28* bit. Let's cover how to get that set up.

### Creating an Android Emulator Device

To test an app from your computer, you need to create a virtual device to test your application on -- it's basically like having a virtual phone!

1. Open the second dropdown from the menu above, and click *AVD Manager*.
2. Once you're in there, you should see a pretty empty menu. At the bottom left of the screen, press the *Create Virtual Device* button to create a new device.
3. Now, you'll be given a list of different phones to emulate (if you go to the left, you can also emulate TVs, smart watches, and even cars!). For the purposes of this workshop, choose the Pixel 2 and press *Next*.
4. This screen will ask you what version of Android you'd like to run, from Android 7 to Android 11. *Keep in mind that you must choose a device that has at least the same version of Android as you chose when you created the project!* Download API 28, choose it, and press *Next*.
5. Now, you'll be able to set the name of the device, and choose whether you want it in portrait or landscape orientation. Leave the defaults and press *Finish*.

Now, if you open the AVD Manager, you'll be able to run your new virtual phone! Before you do that, though, let's test out our app on it.

### Testing the Project

This should be pretty straightforward -- in the dropdown menu that you got to the AVD Manager from, you should be able to select your new virtual device. Now, press the green *Run* button to the right!

Your virtual device should start, and your app will open up like below:

![phone](/home/lambda/repos/MobileDevelopmentWorkshop/android/phone.png)

Congrats! You've just tested your first Android application! Now, let's talk about making it yours.