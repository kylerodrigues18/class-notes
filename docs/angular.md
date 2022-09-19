# Angular

## Architecture

### Components

The most important part of an Angular application. Angular is for creating user interface, components provide user interface.

Components are responsible for an area of our user interface. Usually focused on a single thing (single responsibility)

They have two main jobs:

- Accurately present the application state to the user.
- Provide _affordances_ through which the user can manipulate that state.

:::note State
"State" is the value of all meaningful variables in your application
:::

Every Angular application has a single "parent" component that every other component lives within.
That is the `app.component`

Components are made up of the following things (code wise):

- A typescript class
- A template
- CSS
