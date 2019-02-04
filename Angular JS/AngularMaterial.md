

## Angular Material

### Setup a new angular applciation.
Install the Angular CLI globally.
To install the CLI using npm, open a terminal/console window and enter the following command:

```console
npm install --save @angular/material @angular/cdk @angular/animations
npm install --save hammerjs
```

###  Configure animations
Once the animations package is installed, import BrowserAnimationsModule into your application to enable animations support.

```javascript
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

@NgModule({
  ...
  imports: [BrowserAnimationsModule],
  ...
})
export class PizzaPartyAppModule { }
```

### Import the component modules
Import the NgModule for each component you want to use:

```javascript
import {MatButtonModule, MatCheckboxModule} from '@angular/material';

@NgModule({
  ...
  imports: [MatButtonModule, MatCheckboxModule],
  ...
})
export class PizzaPartyAppModule { }
```

### Add Material icons
```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

### Useful Links
https://material.angular.io/guide/getting-started
