# Effect Hook and Rules of Hooks

- React Hooks
  - Effect Hook
- Effect Hook
- Rules of Hooks

# Effect Hook
React provides a built-in hook called **useEffect** that allows executing logic after the component render.

In general this useEffect hook can be simply called as Effect hook.

Using Effect Hook we can perform actions like,

- Making API Call
- Using Scheduler methods like setInterval( )
- DOM Manipulations, etc.
  
### Syntax: `useEffect(effect)`
The useEffect accepts *effect* as an argument, where the effect is a callback function.

#### Updating Browser title using Effect Hook
Using the ***title*** property provided by the DOM object we can update the Browser title.

Import the useEffect from the react and call it inside the component.
`import {useState, useEffect } from 'react'`

- React keeps track of the effect and executes it after the render.
- All the state variables and props are accessible to the Effect.
- If you try to pass arguments to effect and access them, you'll get undefined values.
```jsx
useEffect((score) => {
  document.title = `Score: ${score}`
})
```
### Accessing State values
If you access the new state value immediately after updating the state in Event handlers, you may not get the updated value because ***state updates are asynchronous***
