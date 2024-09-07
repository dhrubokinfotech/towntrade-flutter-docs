# Push Notification in iOS:

Push notification in iOS does not work in the iOS Simulator and it requires additional setup process that needs an apple developer account. If you have an apple developer account, you need to create an AppID and enable Push Notification capability there. You’ll also need to create an APN Auth Key in the developer portal and upload that Auth key in your Firebase project. Detail information can be found here: [https://firebase.google.com/docs/cloud-messaging/ios/client](https://firebase.google.com/docs/cloud-messaging/ios/client)

Finally, we have to enable Push Notification capability in the “Signing & Capabilities” tab in XCode.

Finally, it is to mention that, we don’t have to make any change in our codebase. The above tasks in the apple developer portal is needed and Xcode needs to connect to your developer account for certificates, provisioning profiles etc.
