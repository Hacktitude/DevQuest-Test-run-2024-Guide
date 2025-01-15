# Welcome to `DevQuest 2024`

>> DISCLAIMER: Please note that this project is created only for DevQuest 2024 organized by SLIIT.

1. [Setting up your environment](#setting-up-your-environment)
2. [Solving the challenges](#solving-the-challenges)
3. [Getting support](#getting-support)
4. [References](#references)

## Setting up your environment

This section helps you to understand the prerequisites required and how to work with the codebase. Please read through carefully and follow the instructions to understand the codebase of this project.

### Prerequisites (Mandatory)

Installations of stable versions of `Git`, `Node.js` and `npm` are required on your computer. You must also be proficient in working with the aforementioned technologies.

[Install Git](https://git-scm.com/downloads)

[Install NodeJS 18.18.0](https://nodejs.org/en/blog/release/v18.18.0)

_Recommended: To ensure seamless management of multiple Node.js versions on your machine, it is highly recommended to use a **Node Version Manager (NVM)**._

> <p>
>      For Windows -: <a href="https://github.com/coreybutler/nvm-windows/releases/download/1.1.11/nvm-setup.exe" target="_blank">Download the .exe file</a>
> <br> 
>      Mac and Linux -: <a href="https://github.com/nvm-sh/nvm/blob/master/README.md#installing-and-updating" target="_blank">Refer this</a>

<br>

We recommend that you use [Visual Studio Code](https://code.visualstudio.com/download) and install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension for a better developer experience.

### Clone the project to your local computer

The Git repository URL and credentials will be available at the start of the contest through a link.

Use Git to clone the project to the local development environment using the credentials that will be shared with the team leader.

* `git clone <repository-url>`

> _Note for **Windows users**: Use `cmd` as the terminal to run commands._

### Installing dependencies

Once you clone the project from your team's Git repository, run the following command to install dependencies.

* `npm install`

### Validate if the environment is correctly setup

You can run the Sanity test file in the `tests` directory with the below command.

For Windows users,

* `npm test _sanity.test.js`

> _Note: If you get an error while running this command, make sure you have set all the prerequisites correctly on your machine._

<!-- If you have the environment correctly set up, all the tests should pass in the sanity test. If the sanity test fails with an internal, that is an indication of your environment setup issue, you must first attend to rectifying your development environment. -->

### Setting up the development database

The following commands will create a SQLite database called `main.sqlite3` in your root folder for development purposes. The `migrate` command deletes the existing database and creates a new one with the DB schema, whereas the `seed` command populates the DB with some initial data. These steps are required for running the application.

* to recreate the database
  * `npm run migrate`
* to populate initial data
  * `npm run seed`

If you do change `db/seeds/**` files, the database schema changes with `migrations` and it may break your test cases and the application.
Therefore, ensure not to change or modify files within the `db` and `tests` directories.

### Building and running the application

To start the server (without nodemon) use the following command:

* `npm start`

Click on the `index.html` file and click on the option **"Open with Live Server"** as shown in the screenshot below.

<p align="center">
  <img src="./images/live-server.png" width="350px">
</p>

### Add .gitignore

You will have to note that the project code has no `.gitignore` file. Please add a `.gitignore` file with the following content.

```
node_modules
config/node_modules
.env
.idea
package-lock.json
main.sqlite3
.vscode
junit.xml
```

> It is advised that one member of your team create the file, commit, and push the .gitignore file to the remote repository with the following commands.

### Commit and Push code to origin

* `git add .`
* `git commit -m "adding .gitignore file"`
* `git push`

Then other team members can pull the changes from the remote repository to receive the `.gitignore` file to their local machines.

* `git pull`

This is how you may use git to collaborate as a team to solve challenges.

## Overview

The Movie Rental System is a web application that allows users to browse, rent, and get recommendations for movies. The system includes features for user authentication, movie management, and rental processing. It also provides an admin interface for managing movies and viewing rental statistics. The system uses k-means clustering to group users based on their rental patterns and provides personalized movie recommendations.

### Features

- **User Authentication**: Users can sign up, log in, and manage their profiles.
- **Movie Browsing**: Users can browse a catalog of movies, view details, and search for specific titles.
- **Movie Rental**: Users can rent movies for a specified number of days and view their rental history.
- **Recommendations**: The system provides personalized movie recommendations based on user preferences and rental history.
- **Admin Interface**: Admins can add, update, and delete movies, as well as view rental statistics and manage user accounts.
- **Clustering**: The system uses k-means clustering to group users based on their rental patterns and provides insights into user behavior.
- 

You can use the following credentials to log in as an admin, and an already existing user in seed data. Navigate the application using the main menu.

ADMIN
* Username: `mattD@gmail.com`
* Password: `Test@123`

* USER
* Username: `tomB@gmail.com`
* Password: `Test@123`

### Executing the Tests

Use the below commands to run the tests. When you FIRST run, all the tests except `_sanity.test` will fail. This is expected.

* To run a single test file of a challenge:

  `npm test challenge0.test.js`

As you complete the challenges, the respective tests will be passed one by one. When you complete all the tasks of a challenge, all tests of the respective challenge should pass. Every DevQuest challenge has a test case that you can run to validate the successful completion of the challenge.

> _Note: Tests are not using the main.sqlite3 database. Every test creates an isolated in-memory database._

### Legitimacy of your solution

Any attempt to compromise the integrity of the contest will `unconditionally disqualify` your team. Therefore please ensure you avoid attempting:

* Tampering files in the `tests` folder or `config` folder
* Hard coding values or logic to pass the test without solving the challenge legitimately

### Improving your developer Experience (Optional)

This step is not mandatory to work on the DevQuest challenges, but it may improve your development experience.

* Install a plugin for **SQLite Viewer** on your IDE so that you are able to explore the SQLite database.

<p align="center">
  <img src="./images/Code_bQgIDTxJNp.png" width="500px">
</p>

* Install any other plugin as necessary for you to improve your developer experience.

## Solving the challenges

If your sanity test passes and you are able to run the application, now you can proceed to the challenges. All the DevQuest challenges are documented in their own file. Please visit the links below, read them carefully, and get started solving them.

Although the challenges are independent from one another, it will be easier for you to solve them somewhat sequentially to understand the challenges better.

Note: We also have provided you with some challenges related to the features of the application that will not be evaluated for the competition.

Have fun!

You can now try out the [Challenge 0](./challenge00.md) for the test run. 


### Key Directories and Files

- `client/`: Contains HTML files and assets for the client-side application.
- `config/`: Contains configuration files and scripts.
  - `buildspec.yml`: Build specification for the project.
  - `replace_tests.js`: Script to replace test files.
- `db/`: Contains database files.
- `readme-files/`: Contains challenge descriptions and instructions.
- `src/`: Contains the source code for the project.
- `tests/`: Contains test files.

## Getting support

There will be minimal to no support available on the context day. We are not in a position to clarify challenge descriptions on an individual basis. However, in case of a setting up the project need, you may contact the technical support team via a chat on WhatsApp (No support for technical doubts) to the phone number `+94 71 382 6109`.

In case of **non-technical support** you may reach out to the DevQuest Support Contact No. `xxxxxxxxxx` via calls only.

## References

* <a href="https://DevQuest.lk/devquest/" target="_blank">DevQuest DevQuest Website</a>
