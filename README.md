# Firebase Admin module

A small Firebase project demonstrating an **Admin Module** which allows end-users with a specific Admin role creating other users and assigning them other specific user roles. **This solution can be applied to Web, Android and iOS apps built with Firebase.**

The project is composed of:

- A Cloud Function that fetches the subcollections of a Document;
- A simple HTML page that demonstrates how it works from a web client.

It demonstrates the approach presented in the following Medium article: https://medium.com/firebase-tips-tricks/how-to-list-all-subcollections-of-a-cloud-firestore-document-17f2bb80a166

### How to use it?

#### Deploy it to one of your Firebase project

- Clone the project `$ git clone https://github.com/rtarnec/firestore-get-document-subcollections.git`
- Install the packages locally by doing `$ npm install` in the `functions` directory
- From the project root directory, list your existing Firebase projects (`$ firebase projects:list`)
- Choose, from the list, the Firebase project you want to use for deployment (If you don't have any Firebase project -or you want to use a new project-, create one in the Firebase console https://console.firebase.google.com/, and re-do `$ firebase projects:list`)
- IMPORTANT Adapt in the `public/index.html` file, the Firebase config object with your own project config. See https://firebase.google.com/docs/web/setup#config-object.
- Deploy the project by doing `$ firebase deploy`

#### Use a browser to open the unique HTML page of the project (i.e. index.html)

Create an Admin user as explained in the Medium article.

Then open the root url of the project (https://<your-project-id>.firebaseapp.com) with your preferred browser and start playing with it:

- Login as an Admin user and create different users with different roles;
- Logout and try to create new users;
- Login as an Author or Editor and try to create new users.
