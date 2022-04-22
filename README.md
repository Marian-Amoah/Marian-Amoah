
# HOW TO LOCALLY SETUP MANAGEMENT PORTAL

This is mainly for developers working on the management Portal for the first time


## Installation
We need some libraries that are necessary to run the projects. You will need an administrator to do the installation for you.
1. install a local server. We will use mysql database.(e.g.MAMP) [Documentation](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/mamp)
2. NVM - node Package Manager(for keeping various versions of node and switching between the versions) [Documentation](https://tecadmin.net/install-nvm-macos-with-homebrew/)
3.  A composer for the backend; it is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it
will manage (install/update) them for you. [Documentation](https://tecadmin.net/install-composer-on-macos/)

    
## Setting up the database
1. Start your server
2. Launch any PHP software tool that will handle the administration of MySQL over the Web. eg."phpMyAdmin"
3. Import the sql file as a new database created. [Tutorials](https://youtu.be/jW5lrS6EUPM)
4. Locate the users table and input your email Address that will enable you login into the system.
5. Set up a google id
## Setting up the backend(laravel/PHP)
1. login into aws account and clone the laravel project on your local machine. [Documentation](https://docs.google.com/document/d/17U9q-BLAtvUQQBTL67gGPvO3hcQ7lrFbmR3tQhqD5Q8/edit#heading=h.6fxiynwr0aa5)
2. launch the project and open a new terminal
3. Checkout to a new branch using your for identifying individual repositories

To checkout run

```bash
  git checkout -b ['Your name']
```
4. In the terminal, run
```bash
  composer install
```
5. We need to install two important package, passport and lcobucci
6. To get started, install Passport, a library that provides a full OAuth2 server implementation for Laravel applications via the Composer package manager. Run this command in your terminal:
```bash
  composer require laravel/passport
```
- Passport's service provider registers its own database migration directory, so you should migrate your database after installing the package. The Passport migrations will create the tables your application needs to store OAuth2 clients and access tokens:
```bash
  php artisan migrate
```
- Next, you should execute the passport:install Artisan command. This command will create the encryption keys needed to generate secure access tokens. In addition, the command will create "personal access" and "password grant" clients which will be used to generate access tokens:
```bash
  php artisan passport:install
```
7. Next, we install lcobucci, a PHP library that allows us to validate JSON Web Tokens. It is mainly used for authentication purposes.
- By running the following command you'll add lcobucci/jwt as a dependency to your project:
```bash
  composer require lcobucci/jwt=3.3.3
```
8. Open the ".env" file in your folder.(Yet to find a way to add it to the project). For now the file can be copied into the folder. Inside the file, set the name of DB_DATABASE to the name of your database.
9. Finally run the following commands in your terminal to start laravel devlopement process.
- To clear Configuration cache:
```bash
  php artisan config:clear
```
- To clear Route cache:
```bash
  php artisan route:clear
```
- To clear Application cache:
```bash
  php artisan cache:clear
```
- This command creates a compiled file of commonly used classes in order to reduce the amount of files that must be included on each request. After running the command, all commonly used classes are compiled and then saved to this file directory:
```bash
  php artisan optimize
```
- To serve the whole application, Note that Port 6010 is the default ports used in ITC for
management_portal_api-v2:
```bash
  “php artisan serve --port=6010
```
## Setting up the frontend(Angular)
1. login into aws account and clone the laravel project on your local machine. [Documentation](https://docs.google.com/document/d/17U9q-BLAtvUQQBTL67gGPvO3hcQ7lrFbmR3tQhqD5Q8/edit#heading=h.6fxiynwr0aa5)
2. launch the project and open a new terminal
3. Checkout to a new branch using your for identifying individual repositories

To checkout run

```bash
  git checkout -b ['Your name']
```
4. Open the package.json file and check that all packages are available
5. Delete the package-lock.json file.(if it is in the folder)
6. To specify node version run:
```bash
  nvm use 14
```
7. Install dependencies.
```bash
  npm install or npm i
```
8. We can serve our application by running the command below, Note that Port 6001 is the default ports used in ITC for  management_portal_v2
```bash
  ng serve --port=6001
```

## Errors and Potential Fixes

#### First Error
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer : In the style.scss, comment out “@import "node_modules/ progress-tracker/src/styles/progress-tracker.scss";

#### Second Error
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer :  in the style.scss. comment out “@import "progress-tracker- custom";

#### Third Error
![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

Answer :   Run “composer require lcobucci/jwt=3.3.3 ” inside the terminal.
## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Authors

- [@IT Consortium_Engineering Team](https://itconsortiumgh.com/)


## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.


## Feedback

If you have any feedback, please reach out to us at https://itconsortiumgh.com/


## Tech Stack

**Client:** Angular,typescript,html,css,bootstrap

**Server:** Laravel, php


## Used By

This project is used by the following companies:

 [IT Consortium](https://itconsortiumgh.com/)


![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)

