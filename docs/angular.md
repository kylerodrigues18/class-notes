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

### VS Code Extensions

- [Link](https://github.com/hypertheory-reference/dot-files/tree/main/angular/.vscode)
- Some settings seem to clash with my IDE

### Redux explained

#### Components have two jobs

1. Accurately display the current state of the application
2. Provide affordances through which the user can interact with the application

- Job 1: Interaction == Actions
  - Components:
    - Just describe what happened (events)
    - Events are actions that are past tense
    - eg. "songAdded" or "songDeleted" or "titleUpdated"
- Job 2: Displaying State == Selector
  - Selectors are functions that return a view (projections) of the required application state
  - When selected from the store, an observable is returned.
  - The component observers that slice of state, the template subscribes to it with the async pipe.

#### Reducers

Functions that are responesible for a portion of the (global) application state. They receive (over time) the actions dispatched and the current application state. They return the same state (if that action doesn't mean anything) or a new state. We write many reducer functions, but they are composed into one reducer function at runtime. After all the reducer functions get a chance at creating a new state when an action is dispatched, the new state is "pushed" to our observables.

Reducer functions must be:

- Pure Functions - output is mapped to input (state, action)
- No side effects - no API calls, nothing unpredictable

#### Courses/Vids to watch

- [1](https://www.destroyallsoftware.com/talks/wat)
- [2](https://www.destroyallsoftware.com/screencasts/catalog/functional-core-imperative-shell)
- [3](https://www.executeprogram.com/)
