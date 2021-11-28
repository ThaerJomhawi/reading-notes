# Cognito

### Configure Auth Category

1- `amplify add auth`

2-

```
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
```

3- `amplify push`

### Install Amplify Libraries

Add the following dependency to your app's build.gradle:

```
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```

### Initialize Amplify Auth

Add the Auth plugin before calling Amplify.configure. Update the code you added in Prerequisites:

```
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```

### Check the current auth session

```
Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);
```