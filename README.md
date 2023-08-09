# Firebase Messaging App
This project adds the back-end to a public message board. 
- I am using a public API for Firebase - this is not an example of good security!

## Steps
Setup
- Clone the original repo [here](https://github.com/tb-harris/firebase)
- Go to firebase.google.com and add a project. Don't enable analytics
- Click the </> Web button below Get Started and name the web app the same as the project name.
- Do not enable firebase hosting

Configuring the SDK
- On the page that opened, under "Add Firebase SDK," copy ONLY the `firebaseConfig` object which looks like this:
    ```JavaScript
    const firebaseConfig = {
        apiKey: "dfbjkdsbfjdskjlfdsbkfdsdjkfkj",
        authDomain: "fsdgfsgdfdsgg-sdfdfsg.firebaseapp.com",
        projectId: "sdfgdfgsdfgs-sfdf",
        storageBucket: "sfdggdfssgf-sfggdf.appspot.com",
        messagingSenderId: "1234567890",
        appId: "1:12345678:web:123456789e2345"
    };
    ```
- Go to `init-firebase.js` and replace `const firebaseConfig = { }` with the copied `firebaseConfig{ ... }` code 

Setup the database
- On your project page, go to Build / Realtime Database, then click Create Database
- Click on "start in test mode" and click enable
- On the Realtime Database page, click on rules and change the code to be: 
```JavaScript
{
  "rules": {
    ".read": true,  // 2023-9-8
    ".write": true,  // 2023-9-8
  }
}
```
- Click enable

Getting a reference to our database
- From the firebase project page, click on docs in the top right
- Click on Reference
- Go to JavaScript - compact (namespaced) / firebase.database / Reference [(here)](https://firebase.google.com/docs/reference/js/v8/firebase.database.Reference?hl=en&authuser=0)
- Add the line `const database = firebase.database().ref();` to the top of `main.js`

Writing to the database
- Follow step 2 of `main.js`: getting references to our HTML elements
- Follow the code in step 3 of `main.js`: updating the database.
- Follow the code in steps 4 and 5 of  `main.js`

Reading from the database
- Follow step 6 in `main.js`