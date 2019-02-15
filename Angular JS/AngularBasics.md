

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

If your new application would need routing, use the following to setup your workspace.

```console
ng new my-app --routing
```

### Run the application
Angular includes a server, so that you can easily build and serve your app locally.
Go to the workspace folder (my-app).
Launch the server by using the CLI command ng serve, with the --open option.

```console
cd my-app
ng serve --open
```

### Generate a new component

```console
ng generate component
```

### How do I allow my application to be accessed outside localhost?

```console
ng serve --host 0.0.0.0
```

### How do I build my application for production?
```console
ng build --prod
```

### My application durbancomics.com/pre-order gives a 404 when refreshed in the live environment , how can I solve this ?
You can download the .htacess file from here and drop it on the root location on the server.



### Useful Links
https://medium.com/codingthesmartway-com-blog/creating-angular-projects-with-angular-cli-e32b2cb486da
