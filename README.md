## Automated-Facebook-Audience-Creation
Automated audience creation/addition on facebook using Firebase Cloud Functions. 
A user is added to an audience on the basis of a trigger event. Ex: Add_To_Cart. 
Now, the user can be shown relevant campaigns on Facebook to push him complete the purchase.

## Pre-requisites
* Node.js
* Firebase project
* Firebase-CLI
* A Facebook application and php-ads-sdk
* Apache web server
* PHP5

## Steps to run the code
* Install Apache and PHP5 on a remote machine. https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04
* Setup Firebase-CLI on your machine https://firebase.google.com/docs/cli
* Setup php-ads-sdk and obtain app_id, app_secret, access_token, add_account_id for your respective application from https://developers.facebook.com/apps
* Deploy the cloud function on Google's server by using command:
```
firebase deploy --only functions
```
* Once the function is deployed, we would start getting triggers for add_to_cart event on our server's DNS/IP.
* Add the php file facebook_add_audience.php in the Apache default read directory (/var/www/html).
* Start Apache web server using the command:
```
sudo service apache start
```

* The php script would be triggered from the cloud function code and would create a new audience on facebook per product group if it does not already exist. If the audience already exists, it would add that particular email to the existing audience.
* You can check all the audiences on https://business.facebook.com/asset-library/audience

