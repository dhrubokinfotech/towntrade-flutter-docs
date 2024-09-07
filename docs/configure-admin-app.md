# Configure The Admin App

Let’s open the towntrade-admin project from our bundle with Android Studio. Since we have already done the necessary setup for Flutter and Android, it should detect the flutter project and start indexing the files and other things.

To make the Towntrade customer app functional, we need to build and configure the Towntrade-Admin app first. This admin app lets the product owner configure a lot of things like Product Categories, Sub-categories, Service Locations, and lots of other things. If these are not configured, then the customer app users will not be able to use the app smoothly and may not see any data.

So, we'll prepare the Towntrade Admin app in the following sections:

- ## [Rename the App & Package Name](rename-app-and-package-name.md)

- ## [Connect the Admin App with the Firebase Project](connect-admin-app-firebase.md)

- ## [Enable Firebase Cloud Messaging or Push Notification](firebase-cloud-messaging.md)

- ## [Connect The Customer App to Back4App](connect-back4ap.md)

- ## [Build the Admin App](build-admin-app.md)

- ## [Additional Notes](additional-notes.md)

### Important Note for the Admin App

It is recommended to set up the `SUPER_ADMIN` profile before starting the USER app.

Your Back4App parse backend table initially does not have an admin. So we have written the admin app this way so that it finds if there is any `SUPER_ADMIN` in the parse table already. Please note that it searches for `SUPER_ADMIN`. Not ADMIN or any other role.

If there is no `SUPER_ADMIN` in the table, The admin app will navigate you to the screen where you will be able to set up a `SUPER_ADMIN`. If `SUPER_ADMIN` is registered, you will never be navigated to this screen ever again. Now you can log in to the admin app using the `SUPER_ADMIN` credentials. `SUPER_ADMIN` can create new ADMINs.
