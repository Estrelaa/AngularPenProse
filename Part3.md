# PEN Part 3 - Services & Dependency Injection

## Aims

In this part, we won't add any extra functionality to our application, but we will refactor our code slightly. At the moment, the locations are hardcoded into one of your components - this isn't a good idea in the long term!

Eventually you'd want to get the data from another source (e.g. a database or a web API) - and the component itself shouldn't care about the details! We'll pull out the code that defines the locations into its own service class that your component depends on. Then you can change the details of how the locations are read later on without your component having to worry.

## Creating a service

The Angular CLI contains the handy command `ng generate service <service-name>`. Generate a well-named service that you'll use as the source of information for your components. For now, it'll just be locations.

The generated service class contains some metadata that allows Angular to provide an instance of it to any other service or component that requires it. More on this further down the page! Your locations component will require an instance of your new service: update the constructor of your locations component so your new service is passed into it as an input argument:

```typescript
constructor(locationsService: LocationsService)
```

## Using the service

Write a method on the new service that provides a list of locations, and refactor your locations component to get its locations from the new service instead of using its own hardcoded list.

Check that your application still works after making this change!

>Why does your component now have a LocationsService it can access?
>
>Angular is what deals with creating instances of your component classes, so Angular is what looks at the constructors and figures out what to pass in. It looks at the type of the constructor parameter, realises that it knows about a service of that type, automatically makes one, and passes it in. This process is called *dependency injection*.
>
>When you look at your service's metadata, you'll see it's called `@Injectable`! Now you know why it's called that. The one parameter is has, `providedIn: 'root'` tells Angular that this service should be "injectable" anywhere in your application.

## Wrapping up

Commit your code, push it, and flag your trainer. Up next, [user inputs](Part4.md)!