# How to Improve the Performance of React Applications

## What to optimize

### 2 different processes into account: 1. how and what code are we sending to the user. 2. how well this code works when it is executed in the user's browser

## Where to start

### Use Lighthouse to tell us what we are doing wrong

## Reducing code

### The best way to minimize the time in which those files reach the user is to minimize the amount of code you are sending at a single moment

## Uglifying code

## Bundling

### In React, use dynamic imports. We can use the ```import()``` function which returns a promise. This allows us to load certain components only when we actually need them

## Prefetching and preloading

### With prefetching we can signal to the browser taht it should load certain scripts while it's idle

### Preloading is used for resources of higher priority. By specifying that a component needs to be preloaded we tell the browser that the user will absolutely need that file but we needn't block the layout while loading it

## React loadable

### ```react-loadable``` is possibly the most widely adopted library when it comes to code splitting

## Separating CSS

### You can use the ```mini-css-extract-plugin``` to extract CSS out of the bundle when you are building for production and have them separated

### The pros of this approach is that will further lessen the amount of the code in your files and their overall size. Also you will be able to send them concurrently

### The cons of this approach is that it makes the setup more complicated so you need to consider if this is a trade off you are willing to make

## Code execution

## Premature optimization

### Avoid optimizing anything before you see an actual problem. Working around non-existing issues can often do more harm than good


## Measuring performance

### React browser extension => Highlight updates

## Rendering components

### The biggest performance hit your app can take is the unnecessary rerendering of the UI. What we want to achieve is to minimize the amount of times that the components call their ```render``` method so we need to have some things in mind and implement fail-saves where necessary

## Responsiveness

### We can get information about the device the user is using from ```window.navigator.userAgent```

## Images

### We should consider lazy loading if we have a lot of images off screen when the user loads the app
