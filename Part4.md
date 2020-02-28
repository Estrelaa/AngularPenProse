# Busboard Part 4 - User input

## Aims

The user should be able to specify what number buses should show up

## FormsModule

In order to bind user input to your component classes, you will need to import the `FormsModule` in your app's root module. In `app.module.ts`, add the following line:

```typescript
import { FormsModule } from '@angular/forms';
```

Then add `FormsModule` to the list of `imports` in the module.

```typescript
@NgModule({
  ...
  imports: [
    ...
    FormsModule
  ],
  ...
})
```

## Binding input to your component

Make a public member on your component called `busNumber`. You can bind the user input to it like this:

```html
<input type="text" [(ngModel)]="busNumber">
```

This binds the input field to the member called `busNumber`. Any changes the user makes to the `<input>` updates the value of the member automatically.

Update your code so that the user can specify a bus number and your app will filter out bus arrivals to only display buses with that number.

It should look something like this:

WIP

