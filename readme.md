# Pushing Push Notfications to Android Application using Firebase

## Getting Started 

Follow the below steps to Configure Firebase 

Step 1: Sign in to your Gmail Account and Create a New Project in Firebase Console : https://console.firebase.google.com/

Step 2: Clicking on Add Project will pop this dialog up and give your project name

Step 3: Now click that green button looks like android logo in the middle for adding firebase to android app

Step 4: Enter Package Name,Application Name and SHA1 Key for step one

Note: Make sure the package name matches the application id in build.gradle of app, in our project the package name is com.sandbox.push, if you give different package name make sure you change the name in build.gradle in app folder of android project

To Get SHA-1 Key, Follow Below Steps:
Go to C:\Users\{{your_laptop_username}}\.android\
open the above path from CMD and type below command
```
keytool -exportcert -alias androiddebugkey -keystore debug.keystore -list -v -storepass android
```
OR

Open Command Prompt and type in below command and hit Enter:
```
keytool -list -v -keystore C:\Users\{{your_laptop_username}}\.android\debug.keystore -alias androiddebugkey -storepass android -keypass android
```

There you can SHA-1 Key, Copy and paste in firebase

Step 5: Now Download the googleservices.json file and place in your Android Project. And copy the downloaded googleservices.json and replace and paste in app folder of android project

Step 6:  Below lines in respective build.gradle files are already added in the project:

### Project Level Gradle Install Prerequisites ( build.gradle):
```
classpath 'com.google.gms:google-services:3.3.0'

```

### App Level Gradle Install Prerequisites ( build.gradle):
```
implementation 'com.google.firebase:firebase-core:15.0.2'
implementation 'com.google.firebase:firebase-messaging:15.0.2'


apply plugin: 'com.google.gms.google-services'

```

Step 7:Hit run and install application on your device.

Step 8: And Now Go back to Firebase Console and Go to Cloud Messaging from Side Menu which will open this screen

Step 9: Now just enter Notification Message and select your app package name to send the push.

Step 10: Holla!! Congrulations, You will get notification to your device 

Hopefully if you have performed each step then you will get the push notification in your device.




