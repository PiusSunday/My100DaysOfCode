# Day 69

Today, I did some error handling on the Smart Home App for the user authentication.

I created new fields to collect user informations then saved them to Firebase Firestore Database.

I'm currently trying to separate the sign up screen into two, one for the user to enter their email and password and the other for the user to enter their informations.

I thought it would be better to separate them into two because the user will have to enter their informations after they sign up and it would be better to have a separate screen for that.

To do this, Instead of creating a new screen, I'm trying to use the same screen but with different states, thereby using the Stepper widget.
