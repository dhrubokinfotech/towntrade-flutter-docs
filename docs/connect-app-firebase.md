# Connect the Customer App with the Firebase Project

Previously we have created a firebase project in the Firebase console. Now, we need to connect our Customer app with this project. In order to do that, we need to do the following steps.

## Connect Android App to Firebase Project

1. Click on the Gear Icon to the right of ‘Project Overview’ in the left menu. It will open a menu, click on the project settings. The project settings page will open up.
2. In the General tab, navigate to the bottom. Click on the Android icon. It opens up a form like the image.

![](public/img/image3.png)

3. In the Android package name, enter the package name that you have chosen while renaming the package. You can also find it in android &rarr; app &rarr; build.gradle file. Copy the applicationId and paste it to the firebase form on step 2.
4. Also, set the App Nickname, use the same name that you have chosen in the project renaming part.
5. At this point, it will provide us a google-services.json file. Let’s download that file and put it in the android &rarr; app directory within the project. See the following image as reference.
6. Since our codebase already has a empty `google-services.json` file in place, so you can just copy the contents of your 'google-services.json' file and paste it in the existing file.

![](public/img/image2.png)

## Connect iOS App to Firebase Project

You can skip this part for now if you want. You can come back here later when you configure and build the iOS version of the app as described [here](build-ios-app.md).

Now, let’s go to our browser to the Firebase Console and open our firebase app. Now we need to go to the project settings like the Android app process in the previous section.

Now click on “Add App” button and fill up the information as requested.

![](public/img/image7.png)

1. In the above image, we need to put the apple bundle ID. We’ll find that in XCode in the General tab, the field we are looking for is “Bundle Identifier” like the image. Copy that and paste into the form at step 4. In the app nickname, add the app name you have set. And download the config file called GoogleService-info.plist and add that file to the iOS project.
2. To do that, right click on Runner in XCode and select ‘Add files to Runner’ and select the GoogleService-info.plist downloaded previously. Make sure, this file and info.plist file remains in the same directory like the image below.
3. Since our codebase already has a empty `GoogleService-info.plist` file in place, so you can just copy the contents of your 'GoogleService-info.plist' file and paste it in the existing file.

![](public/img/image8.png)

## Update firebase_options.dart

Now, we are assuming that we have completed connecting the project to the Firebase Console application as described in the above steps.

At this point, we have another small task to do before we can build the app. Open the file `firebase_options.dart` from the `lib` folder and we'll see the 2 code blocks for iOS and Android platform like the image below.

![firebase_options.dart](public/img/firebase_options.png)

### Fill up the FirebaseOptions for Android

Read the instructions in the code carefully. Then, Let's open our own `google-services.json` file & firebase_options.dart from the lib folder side by side for convenience. Extract the Red marked information from that JSON file and fill up the `apiKey, appId,messagingSenderId, projectId', storageBucket` in the android block in the `firebase_options.dart` file as shown in the image below.

![firebase options android](public/img/fir_option_android.png)

### Fill up the FirebaseOptions for iOS

Read the instructions in the code carefully. Then, Let's open our own `GoogleService-info.plist` file & firebase_options.dart from the lib folder side by side for convenience. Extract the Red marked information from that Plist file and fill up the `apiKey', appId', messagingSenderId, projectId, storageBucket, androidClientId, iosBundleId` in the ios block in the `firebase_options.dart` file as shown in the image below.

![firebase options ios](public/img/fir_option_ios.png)
