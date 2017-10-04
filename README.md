# React Time Tracking App
- Built following FullStack-React-Book

## Built With
-ReactJS, Babel, Node, Express.

### Running the app

1. Ensure you have `npm` installed.

Follow the instructions for your platform [here](https://github.com/npm/npm).

2. Install all dependencies:

````
npm install
````

3. Boot the HTTP server

````
npm run server
````

The server is now running at [localhost:3000](localhost:3000)

## Notes
---
- Handy framework for developing a React app from scratch:
  1. Break the app into components
  2. Build a static version of the app
  3. Determine what should be `stateful`
  4. Determine in which component each piece of `state` should live
  5. Hard-code initial `states`
  6. Add inverse data flow
  7. Add server communication
- Ternary Operator:
```
condition?expression1:expression2
If the condition is true, the operator returns the value of expression1. Otherwise, it returns the value of expression2. In our example, the variable submitText is set to the returned expression.
```
- in our static app. In our static app, data will be wherever we are defining or using `props`. We will then determine which of that data should be `stateful`.
- `TimersDashboard`
  - declares two components. Sets one prop: `isOpen` boolean, which is passed down to `ToggleTimerForm`
  - `Stateful`. The data is defined here. It changes over time. And it cannot be computed from other `state`
or `props`.
- `EditableTimerList`
  - declares two components, each have props corresponding to givem timer's properties
  - Timer properties
  - `Stateful`. The data is defined in this component, changes over time, and cannot be computed from other `state` or `props`.
- `EditableTimer`
  - uses the prop editFormOpen for a given timer
  - `Stateful`. The data is defined in this component, changes over time, and cannot be computed from
other `state` or `props`.
- `Timer`
  - uses all the props for a timer: Timer properties
  - not `stateful`. Properties are passed down from parent.
- `TimerForm`
  - has two interactive input fields for title and project. initialized with timer's current values.

### Stateful questions:
  1 - Is it passed in from a parent via `props`? If so, it probably isn’t `state`.
  2 - Does it change over time? If not, it probably isn’t `state`.
  3 - Can you compute it based on any other `state` or `props` in your component? If so, it’s not `state`.

## Stateful Data:
  • The list of timers and properties of each timer 
  • Whether or not the edit form of a timer is open 
  • Whether or not the create form is open

- 