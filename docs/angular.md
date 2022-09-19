# Angular

## Architecture

### Components

The most important part of an Angular application. Angular is for creating user interface, components provide user interface.

Components are responsible for an area of our user interface. Usually focused on a single thing.

For Example:

- You might have a component that allows people to log in.
- You might have a component that shows a list of vehicles on customer's policy.
- You might have one that let's them add a vehicle to their policy, etc. etc.

They have two main jobs:

- Accurately present the application state to the user.
- Provide _affordances_ through which the user can manipulate that state.

:::note State
"State" is the value of all meaningful variables in your application
:::

Every Angular application has a single "moma" component that every other component lives within.
That is the `app.component`

Components are made up of the following things (code wise):

- A typescript class
- A template
- CSS

_TypeScript is a statically type language. This is good. We want our application to crash on compile time, not run time._

### Get more practice with the following:

- \*ngif()
- (click) - click is an event
- #newName - newName is an alias to element so you don't have to do document.getElementById() etc.
- [ngClass] - Used for applying css classes
