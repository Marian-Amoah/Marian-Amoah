
# HOW TO LOCALLY SETUP MANAGEMENT PORTAL

This is primarily for new developers working on the management Portal.


## Installation
We need some libraries that are necessary to run the projects. You will need an ITC administrator to do the installation for you.
1. Install MySQL server and an SQL client [Documentation](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp)
2. Install NVM - node Package Manager [Documentation](https://tecadmin.net/install-nvm-macos-with-homebrew/)
3. Install Composer for PHP Backend [Documentation](https://tecadmin.net/install-composer-on-macos/)

    
## Setting up the database
1. Start your MySQL server
2. Launch MySQL Client and test connection
3. Import base sql file [Link to download file](https://youtu.be/jW5lrS6EUPM)
4. ( An email address and a google id for authenticating user[yet to resolve])
## Setting up the backend(laravel/PHP)
1. Clone "support-api-v2"
To clone run this command:
```bash
  git clone code commit://itc- playground@support-api-v2
```
2. Launch the project and open a new terminal
3. Set the name of DB_DATABASE to the name of your database in your ".env" file.

To checkout run

```bash
  git checkout -b ['name']
```
4. In the terminal, run the following commands:
```bash
  composer install
```
```bash
  composer require laravel/passport
```
```bash
  php artisan migrate
```
```bash
  php artisan passport:install
```
```bash
  composer require lcobucci/jwt=3.3.3
```
```
  php artisan optimize
```
```bash
  php artisan serve --port=6010
```
- Note that Port 6010 is the default port used in ITC for support-api-v2

## Setting up the frontend(Angular)
1. Clone "support-portal-v2"
To clone run this command:
```bash
  git clone code commit://itc- playground@support-portal-v2
```
2. Launch the project and open a new terminal

To checkout run
```bash
  git checkout -b ['name']
```
3. Delete the package-lock.json file.(if it is in the folder)
4. To switch to use node 14:
```bash
  nvm use 14
```
7. Install dependencies.
```bash
  npm install or npm i
```
8. Serve the application 
```bash
  ng serve --port=6001
```
Note that Port 6001 is the default ports used in ITC for support-portal-v2

## Errors and Potential Fixes

#### First Error(Angular Application) : ERROR in ./src/assets/scss/style.scss (./node_modules/@angular-devkit/build-angular/src/angular-cli- files/plugins/raw-css-loader.js!./node_modules/postcss-loader/src?? embedded!./node_modules/sass-loader/lib/loader.js??ref--14-3!./src/ assets/scss/style.scss)Module build failed (from ./node_modules/sass- loader/lib/loader.js):
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer : In the style.scss, comment out “@import "node_modules/ progress-tracker/src/styles/progress-tracker.scss";

#### Second Error(Angular Application) : ERROR in ./src/assets/scss/ style.scss (./node_modules/@angular-devkit/build-angular/src/angular-cli- files/plugins/raw-css-loader.js!./node_modules/postcss-loader/src?? embedded!./node_modules/sass-loader/lib/loader.js??ref--14-3!./src/ assets/scss/style.scss)
#### Module build failed (from ./node_modules/sass-loader/lib/loader.js):$marker-size-third: ceil(math.div($marker-size, 3)); ^Invalid CSS after "...hird: ceil(math": expected expression (e.g. 1px, bold), was ".div($marker-size, "in /Users/mboye-amoah/Desktop/Management_Portal/ management_portal_v2/node_modules/progress-tracker/src/styles/progress- tracker/_progress-tracker-variables.scss (line 19, column 30)
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer :  in the style.scss. comment out “@import "progress-tracker- custom";

#### Third Error(Laravel Application) : local.ERROR: Replicating claims as headers is deprecated and will removed from v4.0. Please manually set the header if you need it replicated. {"exception":"[object] (ErrorException(code: 0): Replicating claims as headers is deprecated and will removed from v4.0. Please manually set the header if you need it replicated. at /Users/mboye-amoah/Desktop/Management_Portal/ management_portal_api-v2/vendor/lcobucci/jwt/src/Builder.php:352)
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer :   Run “composer require lcobucci/jwt=3.3.3 ” inside the terminal.
## Tech Stack

**Client:** Angular,typescript,html,css,bootstrap

**Server:** Laravel, php


## Used By
 [IT Consortium](https://itconsortiumgh.com/)


![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)

