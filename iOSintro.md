# Intro to Coding for iOS
## Overview
**What you'll learn**
In this section you'll learn

 1. What Xcode is and how to install it
 2. How to make a Hello World iOS app
 3. iOS programming languages
 4. Process for distributing an app on the App Store

**Prerequisites**
Before starting this section, you should have an understanding of

 1. Experience with programming is suggested, but not necessary (you can learn Python [here](https://github.com/HackBinghamton/PythonWorkshop))

**Introduction**
Xcode is Apple's IDE (integrated development environment) for macOS. Not only can you create iPhone apps, but you can also code software to run on Mac computers, iPads, Apple Watches, and Apple TVs. 

**NOTE:** You need a Mac computer to create iOS apps. However, you do not need an iPhone to test them. 

## Xcode
The Xcode IDE is necessary for writing native iOS apps. An IDE is a piece of software that makes coding a lot easier. For example, Xcode will automatically make suggestions for your code as you're writing it. A native app is an app specifically designed for one platform, which is iOS in our case. 

The first step for creating your iOS app is to install Xcode on your computer. Note that Xcode is only available for Mac computers. You can download Xcode either on the App Store or [here](https://developer.apple.com/download/). Installing Xcode is a bit of a hassle. While the actual application is only about 12GB, you'll need a little more than 40GB free on your computer to download it. If you don't have enough space on your computer, it's helpful to temporarily move your larger files (probably your applications) onto an external hard drive if you have one. 

Keep reading to see how to set up a project in Xcode!

## Hello World iOS App
Now that you've downloaded Xcode, we can make a simple Hello World app. When I say simple, I mean *simple*!

When you open Xcode, you'll see a pop up that says "Welcome to Xcode" with some options for getting started. You'll want to select **Create a new project**.

Next, you'll need to choose a template for this project. At the top you'll see the different operating systems you can choose from, select **iOS**. For your template, choose **App**. Once you get the hang of coding for iOS, you can check out our next iOS section to see some other templates in action!

Now you need to fill in some information about your app. **Product Name** is the name of your app. You can name this anything like helloWorldApp, myFirstApp, or hackbuIsCool. **Team** requires that you sign in with your Apple ID. This just lets Apple know who is creating the app in case you decide to put it on the App Store. **Organization Identifier** is also another thing needed to put an app on the App Store. This can be anything you want it to be. For example, my organization identifier is my Binghamton PODs username. For **Interface** choose **Storyboard**. For **Language** you can choose between Swift or Objective-C. 

**Swift vs. Objective-C**
So which language should we choose? Objective-C has been around for a long time and Swift, which was realized in 2014, is slowly taking over the iOS scene. Because Objective-C is older, it lacks modern language features and its syntax is more complicated. Swift, on the other hand, is relatively new and has a simpler syntax that looks similar to Python. 

Here's an example of the same line of code in each language: 
Objective-C: `[mylabel setText:@"Hello World!"];` 
Swift: `mylabel.text = "Hello World!"` 
So as you can see, Swift  is a lot prettier than Objective-C.

We'll be using Swift throughout the iOS portions of this workshop, but if you're interested in Objective-C there are plenty of tutorials to follow online.

**Now back to building our Hello World app!** 
Once you fill out the information for your app and decide where to store it on your computer, Xcode will open your project. Head over to the Main.storyboard file. This is a click and drag interface for building apps. Click the + in the top right corner of Xcode. You'll see a popup of the various UI elements you can add to your app. 

Let's add a **label**. You can click and drag the label onto the phone screen. Now you can double click it to type "Hello World", or whatever you want! 

Let's see what our app looks like now. There are two different ways you can test an app from Xcode. The first option is to run the simulator that comes with Xcode. You can do this by clicking the play button in the top left corner. The second option is to test it on your iPhone. You can plug your iPhone into your computer, select your device, and hit the same play button. Your app will install on your phone and automatically open when it's ready. In most cases, the simulator is easier. However, some app functionality cannot be simulated, such as when you use the camera in your app. So in that case you should test the app on your own device. 

Tada! You've created your first iOS app, congratulations! Check out our next section on iOS to learn more about making an interactive app.

## The App Store
You might be wondering how to put an app on the App Store. This is more complicated (and expensive) than it seems. Once you've created a high quality app that you feel comfortable distributing on the App Store, you need to enroll in the Apple Developer Program to be able to put your app on the App Store. Enrolling in this program costs $99 annually (crazy!). Then you can go to App Store Connect and create a listing for your app with the title, description, and some screenshots. After doing this you can create an archive of your app in Xcode and submit this to App Store Connect as well. Then you can review all the information on your listing and submit your app to the Apple Certification Team for review. 

This is a long process so we obviously don't expect you to release any apps to the App Store after this workshop. If you're interested in having the app on your phone for personal use, you can run the app on your phone, as you would to test it. Then the app will remain on your phone until you delete it. If you ever make changes to your app, you'll need to run the app on your phone from Xcode again to put the changes on your phone. 
