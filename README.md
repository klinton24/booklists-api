# Getting Started with this project

After cloning/forking this repo, run the `npm install` command

## Local DB setup

We're going to be using PostgreSQL for the project so you will want to get that set up locally on your machine.
To get it set up, click on this [link](https://www.postgresqltutorial.com/install-postgresql/). This will take you to the install site for Windows. If your computer has a different OS, there are links on that page to take you to the appropriate place.

Follow the steps of the wizard. Use port `5432` when asked, and don't worry about installing the Stack Builder stuff.

This wizard will setup a user under the account name `postgres`. When you are asked to give a password, be sure to give it remember what you set it as.

You'll need to install a DB viewer. I recommend pgAdmin just to be consistent with others on the project. You can download it here: https://www.pgadmin.org/download/

Once you have that downloaded and opened, right click the `Databases` dropdown in the left panel and select 'Create' and then 'Database'. Name the database `fcc-reading-db`.

## Environment variables

Create a new file at the root of the project and call it `.env`.

Add the following code:

```
PORT=3030
DB_URL=postgres://postgres:DB_PASSWORD@localhost:5432/fcc-reading-db
```

Replace the `DB_PASSWORD` with the password you added when setting up Postgres earlier.

## Starting the app

Now that you have your database connected, we can run `npm run start` in your command line and the app should start up and we should see the console output something like this:

```
info: Feathers application started on http://localhost:3030
Created users table
Publishing all events to all authenticated users. See `channels.js` and https://docs.feathersjs.com/api/channels.html for more information.
```
