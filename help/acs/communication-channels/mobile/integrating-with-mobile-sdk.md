---
title: Getting started with Push Notifications with Android App
seo-title: Getting started with Push Notifications with Android App
description: Part 1 - Creating your Android App and adding to Firebase. 
seo-description: Part 1 - Creating your Android App and adding to Firebase
feature: Push
topics: Channels
kt: KT-1375
doc-type: tutorial
activity: use
team: TM
---
#Integrate Mobile SDK with Android APP
In this part, we will integrate the Android app with Mobile SDK. To integrate mobile SDK with the Android app, please follow the following steps:

* Open the ACSPushTutorial project in Android Studio
* Create a new java class called MainApp which extends android.app.Application
* Your project structure at this point should look like below
![main-app](assets/android-main-app.PNG)
* Open the launch property which has Adobe Campaign Standard extensions configured
* Tab to the Environments tab. Click on install icon associated with the Development  environment
* Copy the dependencies that need to be added to build.gradle by clicking the copy icon
* Return to Android Studio. Make sure you are in the ACSPushTutorial project
* Expand the Gradle Scripts folder. Double click the build.gradle of the module. Paste the dependencies in to the dependencies section of the build.gradle file. Your build.gradle file should now look like below
![module-gradle](assets/module-build-gradle.PNG)
* Since we have changed the gradle file, make sure to sync your project to download the dependencies that have been added.

##Register Token
The next step is to register the