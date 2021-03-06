# PEN Part 1 - Your First Component

## Aims

By the end of this part, your app's homepage will display a single location and the pens you own in it. See how each pen has a colour, a pen type, and who's borrowing it?

![Part 1](assets/Part1.png)

## A whole new world

During the [overview](Overview.md), you created a new project. The `ng new` command has created a new Angular application called `pen`. There're a lot of files in your new project, but you won't need to worry about most of them.

Find the files `app.component.ts` and `app.component.html`. Can you see how these files relate to each other? How do they relate to what you see in your browser? Try changing the title of the application and see what happens to your browser window.

Once you both understand what's happening in this simple case, let whoever in the pair has the least Angular experience "drive" first.

## Structure of the exercise

Today's PEN is going to be built up in distinct chunks. After you've completed each part, create a commit and push it to GitHub using the following commands:

```
git add -A
git commit -m "Finished Part X"
git push
```

Let your trainer know when you've finished each part, and they'll take a final look at the code you've written and offer some comments on what you've done.

## Generating a component

The Angular CLI has a lot of ways of generating boilerplate/template code for you to make your job easier. Right now, we'll use it to generate a new *component*.

>In Angular, a *component* is a building block for your app. You can think about it like a custom HTML tag: you define the inputs, the layout, and how it will be displayed on the page. In building your page, you'll use your components like building blocks. Some of your components will be composed of other components! Building up your page and components like this helps keep each component simple, and makes your code cleaner.

Let's make a component that displays the details for a location: use the command `ng generate component location-details`.

This will make a new directory with some autogenerated code inside. The files we care about are `location-details.component.ts` and `location-details.component.html`.

>`*.component.ts` files contain a single class with some *metadata* contained in the `@Component` decorator. This is used by Angular to determine how to display your component. `templateUrl` tells Angular which HTML template to use for your component, and the `styleUrls` tell Angular which CSS files to use for styling. The other piece of metadata is the `selector`: whenever Angular sees it as an HTML tag in a template, it will insert your component: in this case, `<app-location-details></app-location-details>`.

Now let's replace the contents of the template in `app.component.html` so that Angular will render your new component on the page. Check that your changes are reflected in your browser.

## Displaying location details

Angular has a clever mechanism for getting information out of TypeScript code and into your templates; any public member variables on your component class (the one in `*.component.ts`) will be available for use in the corresponding template. All you have to do is place the name of the variable between double curly braces: `{{foo}}`. You will have seen this working in the previous part, when looking at the title of the application.

We don't yet have any location details in our code! Create a class that contains all of the data you think you will need about a location (such a class is often called a "model" class).

>You can create a boilerplate class using the Angular CLI - `ng generate class <class-name>`. Don't be afraid to create other useful classes too - maybe one to hold details about a particular pen? Remember to import them whenever you want to use them!

Once you've defined your model class(es), create a location as a member variable on your new component, and write some HTML in the template that will display its details.

You will probably want to use the `ngFor` directive in your template. This lets you use a for-loop in your template, for example to loop over an array, and it repeats the element that it is used on, and all its children, for every iteration of the loop. For example, to create an ordered list with an item for each element of an array:

```html
<ol>
    <li *ngFor="let elem of array">{{elem}}</li>
</ol>
```

## Wrapping up

After you're done, commit your code, push it to GitHub, and *let your trainer know*. Up next, [multiple locations](Part2.md)!
