# About the project

This is the code I wrote following the Classed tutorial on building a social network using React, Node & Firebase and is based on the SocialApe app ([back end repository](https://github.com/hidjou/classsed-react-firebase-functions), [front end repository](https://github.com/hidjou/classsed-react-firebase-client)) from the [Classed Full Stack React & Firebase tutorial series](https://www.youtube.com/watch?v=RkBfu-W7tt0&list=PLMhAeHCz8S38ryyeMiBPPUnFAiWnoPvWP) by [Ahmed Hadjou](https://github.com/hidjou)

This code is for the back end. The front end code I wrote can be found [here](https://github.com/Kgotso-Koete/socialApe-react-firebase-client).

# How to run the code:

The app is deployed on Google Firebase. Here is the [demo](https://socialape-69760.firebaseapp.com)

## 1: API Base URL

Add https://europe-west1-socialape-69760.cloudfunctions.net/api as the 'proxy' value in package.json

## 2: Install packages

Run `npm install`

## 3: Run project

Run `npm start`

## 4: Open it

Open your web browser and go to http://localhost:3000

# Description and features

For now, the application will have the following user stories and corresponding features:

## users routes

1. The user can sign up to create an account
   <br/>Back end: `app.post("/signup", signup);`
   <br/>Front end: `home` component with a pop up `signup` component using path `/signup`

2. The user can log into their account
   <br/>Back end: `app.post("/login", login);`
   <br/>Front end: `home` component with a pop up `login` component using path `/login`

3. An authenticated user can upload a picture via their profile screen
   <br/>Back end: `app.post("/user/image", FBAuth, uploadImage);`
   <br/>Front end: `home` component with an embedded `Profile` component without any path specified

4. An authenticated user can edit other profile details (other than their picture) in their profile screen
   <br/>Back end: `app.post("/user", FBAuth, addUserDetails);`
   <br/>Front end: `home` component with an embedded `Profile` component without any path specified

5. An authenticated can go to their user feed which will list their profile and posts that they created
   <br/>Back end: `app.get("/user", FBAuth, getAuthenticatedUser);`
   <br/>Front end: n/a

6. The app can fetch unauthenticated user details to be displayed in various components
   <br/>Back end: `app.get("/user/:handle", getUserDetails);`
   <br/>Front-end: `user` component with embedded list of `Screams` and a `StaticProfile` component with path `/users/:handle`

7. The app can fetch the authenticated user's list of notifications for unread likes and comments
   <br/>Back end: `app.post("/notifications", FBAuth, markNotificationsRead);`
   <br/>Front end: `Navbar` component with an embedded `Notifications` component without any path specified

## Scream routes

8. An unauthenticated user can get a list of posts
   <br/>Back end: `app.get("/screams", getAllScreams);`
   <br/>Frond end: `home` component displays feed with path `/`

9. An authenticated user can create a new post
   <br/>Back end: `app.post("/scream", FBAuth, postOneScream);`
   <br/>Front end: `Navbar` component with an embedded `PostScream` component opens up dialog box, no path specified.

10. An unauthenticated user can get the details of a post to be displayed in a dialog box
    <br/>Back end: `app.get("/scream/:screamId", getScream);`
    <br/>Front end: `Scream` component with a pop up `ScreamDialog` component using path `/users/${userHandle}/scream/${screamId}`

11. An authenticated user can delete a post that they created
    <br/>Back end: `app.delete("/scream/:screamId", FBAuth, deleteScream);`
    <br/>Front end: `Scream` component with a pop up `DeleteScream` component without any path specification

12. An authenticated user can like a post
    <br/>Back end: `app.get("/scream/:screamId/like", FBAuth, likeScream);`
    <br/>Front end: `Scream` component with an embedded `LikeButton` component without any path specification

13. An authenticated user can unlike a post
    <br/>Back end: `app.get("/scream/:screamId/unlike", FBAuth, unlikeScream);`
    <br/>Front end: `Scream` component with an embedded `LikeButton` component without any path specification

14. An authenticated user can comment on a post and read other comments displayed
    <br/>Back end: `app.post("/scream/:screamId/comment", FBAuth, commentOnScream);`
    <br/>Front end: `Scream` component with a pop up `ScreamDialog` component using path `/users/${userHandle}/scream/${screamId}`

# Timesheet log

- Version 1 (Classed Tutorial): 59 hours
- Version 2 (personal modifications): ?

#

This web applicaion is built using React, Node & Firebase and is based on the SocialApe app ([back end repository](https://github.com/hidjou/classsed-react-firebase-functions), [front end repository](https://github.com/hidjou/classsed-react-firebase-client)) from the [Classed Full Stack React & Firebase tutorial series](https://www.youtube.com/watch?v=RkBfu-W7tt0&list=PLMhAeHCz8S38ryyeMiBPPUnFAiWnoPvWP) by [Ahmed Hadjou](https://github.com/hidjou)

Special thanks to [Ahmed Hadjou](https://github.com/hidjou) for a great tutorial with a stunning app as a project.<br/><br/>
To be modified further by Kgotso Koete<br/><br/>
Johannesburg, October 2019
