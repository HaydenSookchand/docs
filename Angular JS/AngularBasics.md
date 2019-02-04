

## Angular Basics

### Setup a new angular applciation.
Install the Angular CLI globally.
To install the CLI using npm, open a terminal/console window and enter the following command:

```console
npm install -g @angular/cli
```

### Setup a new workspace
You develop apps in the context of an Angular workspace. A workspace contains the files for one or more projects. A project is the set of files that comprise an app, a library, or end-to-end (e2e) tests.To create a new workspace and initial app project:
Run the CLI command ng new and provide the name my-app, as shown here:

```console
ng new my-app
```

### Run the application
Angular includes a server, so that you can easily build and serve your app locally.
Go to the workspace folder (my-app).
Launch the server by using the CLI command ng serve, with the --open option.

```console
cd my-app
ng serve --open
```
