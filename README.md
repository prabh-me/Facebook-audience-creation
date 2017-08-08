## Automated-Facebook-Audience-Creation
Automated audience creation/addition on facebook using Firebase Cloud Functions. 
A user is added to an audience on the basis of a trigger event. Ex: Add_To_Cart. 
Now, the user can be shown relevant campaigns on Facebook to push him complete the purchase.

## Pre-requisites
* Node.js
* Firebase project
* Firebase-CLI
* Apache web server
* PHP5

## Steps to run the code
* Install Apache and PHP5 on a remote machine. https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04
* Setup Firebase-CLI on your machine https://firebase.google.com/docs/cli
* Deploy the firebase_cloud_function.js file on Google's server by using command
```
firebase deploy --only functions
```
