


## Angular Pipe Search

### Setup a search within your app

Create a new file called filter.pipe.ts and add in the following code. 
```javascript
import {Pipe, PipeTransform} from '@angular/core';

@Pipe({
  name: 'search'
})
export class SearchPipe implements PipeTransform {
  public transform(value, keys: string, term: string) {

    if (!term) return value;
    return (value || []).filter(item => keys.split(',').some(key => item.hasOwnProperty(key) && new RegExp(term, 'gi').test(item[key])));

  }
}
```

###  Add the following code to App.Module
```javascript
import { SearchPipe }from './filter.pipe';

@NgModule({
  declarations: [
    SearchPipe 
  ]
```

### Use in component html
```html
   <mat-card class="card-item" *ngFor="let product of products | search:'title': searchText">
```
