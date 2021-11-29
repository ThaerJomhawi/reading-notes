# Notifications

To create your Android platform application in Amazon SNS, you must have credentials from Firebase Cloud Messaging (FCM).

### Create a Firebase project on the Firebase website:

1. In the Firebase console, choose your project.

2. In the left navigation pane, choose the gear icon, and then choose Project settings.

3. Choose Cloud Messaging.

4. Under Project credentials, find the Server key. This your FCM project's API key. Copy it to your clipboard.

### Create a platform application in Amazon SNS

1.  Open the Amazon SNS console.

2.  In the left navigation pane, choose Mobile. Then, choose Push notifications.

3.  On the Mobile push notifications page, next to Platform applications, choose Create platform application.

4.  On the Create platform application page, under Details, do the following:
    For Application name, enter the name of your application.
    For Push notification platform, choose Firebase Cloud Messaging (FCM).
    Under Firebase Cloud Messaging Credentials, for API key, enter the server key that you copied earlier.

5.  (Optional) Set up event notifications and delivery status logging.

6.  Choose Create platform application.
