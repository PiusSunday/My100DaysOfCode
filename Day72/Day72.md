# Day 72

So about the bug yesterday, when trying to add a new user information to the Firebase Firestore Database, the email wouldn't get sent but the other user informations gets sent to Firestore, for some reasons I didn't know, even though the function and function call was correct.

I took time today to go through the code, analyze the function and the function call and I finally found the bug.

The bug was simply the fact that I had a separate function to add user information to the database and I was calling that function in the method that registers new users.

For the add user information to Firestore function, I had a parameter that was supposed to be the user's email, but I needed to pass the <FirebaseAuth.instance.currentUser!.email>, which is the email of the current user, to the function instead of an explicit property.

So, I added the add user information to the database function directly to the register new user function and passed the <FirebaseAuth.instance.currentUser!.email> to the function and it worked.
