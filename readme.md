# Pushing Push Notfications to Android Application using Firebase

## Getting Started 

Create an Account in firebase 

### Prerequisites 
keytool -exportcert -alias androiddebugkey -keystore debug.keystore -list -v -storepass android

###Create Two Java Files:
```
MyFirebaseInstanceIdService

MyFirebaseMessagingService
```


###Project Level Gradle Install Prerequisites ( build.gradle):
```
classpath 'com.google.gms:google-services:3.3.0'

```

### App Level Gradle Install Prerequisites ( build.gradle):
```
implementation 'com.google.firebase:firebase-core:15.0.2'
implementation 'com.google.firebase:firebase-messaging:15.0.2'

```
