# Advanced CSS Theming with Custom Properties and JavaScript

## Understanding :root and var()

### A custom property is a property whose name starts with two hyphens (-) like --foo. They define variables that can be referenced using var()

### Defining custom properties within the :root selector means they are available in the global document space to all elements. :root is a CSS pseudo class which matches the root element of the document - the <html> element. It's similar to the html selector but with higher specificity

## CSS Custom Properties vs Preprocessor Variables

### CSS custom properties are natively parsed in modern browsers. Preprocessor variables require compilation into a standard CSS file and all variables are converted to values

### Custom properties can be accessed and modified by JavaScript. Preprocessor variables are compiled once and only their final value is available on the client