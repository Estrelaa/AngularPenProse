# PEN Part 3 - Services

## Aims

In this part, we won't add any extra functionality to our application, but we will refactor our code slightly. At the moment, the locations are hardcoded into one of your components - this isn't a good idea in the long term!

Eventually you'd want to get the data from a database - and the component itself shouldn't care about the details! We'll pull out the code that defines the locations into its own service class that your component depends on. Then you can change the details of how the locations are read later on without your component having to worry.

## Creating a service

The Angular CLI contains the handy command `ng generate service <service-name>`. Generate a well-named service that you'll use as the source of information for your components. For now, it'll just be locations.

The generated service class contains some metadata that allows Angular to provide an instance of it to any other service or component that requires it. Your locations component will require an instance of your new service. Update the constructor of your locations component to something like this:

```typescript
constructor(private locationsService: locationsService)
```

Angular looks at the type of the constructor parameter, realises that it knows about a service of that type, automatically makes one, and passes it in. This process is called *dependency injection*.

## Using the service

Write a method on the new service that provides a list of locations, and refactor your locations component to get its locations from the new service instead of using its own hardcoded list.

Check that your application still works after making this change!

## Wrapping up

Commit your code, push it, and flag your trainer. Up next, [user inputs](Part4.md)!