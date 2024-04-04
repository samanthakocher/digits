<img src="doc/landing.png">

Digits is an application that allows users to:
* Register an account.
* Create and manage a set of contact.
* Add a set of timestamped notes regarding their interactions with each contact.

## Installation
First, install Meteor.

Second, download a copy of Digits. Note that Digits is a private repo and so you will need to request permission from the author to gain access to the repo.

Third, cd into the app directory, and install the required libraries with:

<img src="/doc/meteor-npm-install.png">

Once the libraries are installed, you can run the application by invoking:

<img src="/doc/meteor-npm-run-start.png">

The first time you run the app, it will create some default users and data. Here is the output:

<img src="run-start-output.png">


<Strong>Note regarding bcrypt warning.</Strong> You will also get the following message when you run this application.

<img src="/doc/bcrypt.png">

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at http://localhost:3000. You can login using the credentials in settings.development.json, or else register a new account.

Lastly, you can run ESLint over the code in the imports/ directory with:

<img src="/doc/run-lint.png">

## User Interface Walkthrough

<h3>Landing Page</h3>
When you first bring up the application, you will see the landing page that provides a brief introduction to the capabilities of Digits:

<img src="/doc/landing.png">

<h3>Register</h3>
If you do not yet have an account on the system, you can register by clicking on “Login”, then “Sign Up”:

<h3>Sign In</h2>
Click on the Login link, then click on the Signin link to bring up the Sign In page which allows you to login:

<h3>User home page</h3>
After successfully logging in, the system takes you to your home page. It is just like the landing page, but the NavBar contains links to list contact and add new contacts:

<h3>List Contacts</h3>
Clicking on the List Contacts link brings up a page that lists all of the contacts associated with the logged in user:

This page also allows the user to add timestamped “notes” detailing interactions they’ve had with the Contact. For example:

<h3>Edit Contacts</h3>
From the List Contacts page, the user can click the “Edit” link associated with any Contact to bring up a page that allows that Contact information to be edited:

<h3>Admin mode</h3>
It is possible to designate one or more users as “Admins” through the settings file. When a user has the Admin role, they get access to a special NavBar link that retrieves a page listing all Contacts associated with all users:
