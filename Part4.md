# Busboard Part 4 - User input

## Aims

We want to be able to filter by who's borrowed our pens! The user should be able to type in a name and the location details should only display pens that have been lent to that person.

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

Make a public member on your component called `borrower`. You can bind the user input to it like this:

```html
<input type="text" [(ngModel)]="borrower">
```

This binds the input field to the member called `borrower`. Any changes the user makes to the `<input>` updates the value of the member automatically.

Update your code so that the user can specify a name and your app will filter out pens to only display pens lent to that person.

It should look something like this:

so wip

much incomplete

wow

## Wrapping up

Commit your code, push it, and flag down your trainer. Up next, [routing](Part5.md)!

