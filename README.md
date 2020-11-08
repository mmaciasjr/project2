# Credit for seed repo and much of this Readme code: https://github.com/paigen11/mysql-registration-passport

# MySQL Registration with JWT & Passport Authentication

## How to run this app

1. cd to `<root>/client`
2. run `npm install`
3. run `npm start`
4. in a separate shell, cd to `<root>/api`
5. run `npm install`
6. run `npm start`

## About This App

This application is a full-stack MERN app (MySQL, Express, React and
Node.js). It is a user registration application that allows a user to register in the database, log in, view their profile, update it and delete it.

Passport local handles user authentication for the unprotected routes, which are the user registration and login routes.

Once the user has logged in a JWT token is created and sent to the client and storeed in local storage along with user data, Passport JWT takes over at this point and handles all further user authentication for protected routes.

Each request from the client to the server must include the JWT as one of its authorization headers before the route can be accessed. If the JWT is missing, corrupted or expired (it has a 1 hour expiration date from the time it's created on login), the authentication will fail and the route cannot be accessed.

If a user logs out or deletes their user profile, the JWT is removed from local storage and the user is dropped back at the home screen again.

They can update their password once logged in to the app as well from a separate update password screen.
