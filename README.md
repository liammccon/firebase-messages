# Firebase Messaging App
This project adds the back-end to a public message board. 
- I am using a public API for Firebase - this is not an example of good security!

## Steps
....

Getting a reference to our database
- From the firebase project page, click on docs in the top right
- Click on Reference
- Go to JavaScript - compact (namespaced) / firebase.database / Reference [(here)](https://firebase.google.com/docs/reference/js/v8/firebase.database.Reference?hl=en&authuser=0)
- Add the line `const database = firebase.database().ref();` to the top of `main.js`

Writing to the database
- Follow step 2 of `main.js`: getting references to our HTML elements
- Follow the code in step 3 of `main.js`: updating the database.