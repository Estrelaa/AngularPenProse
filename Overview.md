# Busboard

## Aims

Today we'll be returning to BusBoard, which I'm sure was your favourite part of the bootcamp. This time, we're writing it in Angular!

The aim today is to get you to understand as much Angular as you can without overloading you: you'll each have differing amounts of experience with JavaScript, TypeScript, and Angular.

## Before you start

To get going, you'll need to have completed the following setup. Let your trainer know when you're done, or ask for help if you can't complete any of the steps.

  - Download [Visual Studio Code](https://code.visualstudio.com/): it's very good with TypeScript and AngularJS.
  - Make sure that you have Git, Node.js and npm installed on your machine - you'll need at least version 10.13.0 of Node.
      - Use [nvm-windows](https://github.com/coreybutler/nvm-windows) or [nvm](https://github.com/nvm-sh/nvm) for updating your Node version.
  - Open up a command prompt and navigate to somewhere where you're happy to create a new directory for this project.
  - Run the command `npm install -g @angular/cli` to install the Angular CLI
  - Run `ng new busboard` to create a new Angular project, and navigate to the root directory that was created.
  - Create a new empty repository within your GitHub account. When asked if you want to initialize the project with a README, say no.
  - Follow the onscreen instructions to push your new Angular project to GitHub.
  - Email a link to your repository to your trainer.
  - Open up a second command prompt, navigate to your `busboard` directory, and run `ng serve --open` to launch your application in a browser.
  - You'll be pairing today! Once you're both happily set up, pick whoever in the pair has the least Angular experience and let them "drive" first.

## What's just happened?

The `ng new` command has created a new Angular application called `busboard`. There're a lot of files in your new project, but you won't need to worry about most of them.

Find the files `app.component.ts` and `app.component.html`. Can you see how these files relate to each other? How do they relate to what you see in your browser? Try changing the title of the application and see what happens to your browser window.

Once you understand what's happening in this simple case, read the rest of this page and then move on to Part 1.

## Structure of the exercise

Today's Busboard is going to be built up in distinct chunks. After you've completed each part, create a commit and push it to GitHub using the following commands:

```
git add -A
git commit -m "Finished Part X"
git push
```

Let your trainer know when you've finished each part, and they'll take a final look at the code you've written and offer some comments on what you've done.