---
Footer: false

<!-- .slide: data-background="/images/show-me-3-styling.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-4-state-mgmt.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

---

Trail: 4. State Management

<!-- .slide: data-background="/images/component-f-props.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

- remember the drawing of a component as f(props)?
- it was a lie!

---

Trail: 4. State Management

<!-- .slide: data-background="/images/component-f-props-state.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

Components are _actually_ functions of both their props and their state

...

props are passed into a component

state is contained within a component

and the component manages it.

Examples:

- the checked state of a checkbox.
- the current value of a counter

...

- when you update props OR state of a component, React re-renders it

---

Trail: 4. State Management

<!-- .slide: data-background="/images/state-turns-into-props.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

Once you have a component managing its state,

it can pass it down to its children as props

This is a really common thing to do in React-

elevate the state to the highest level that any other component would need it, and manage it there.

...

When it comes to ways to manage state, you've got options!

---

Trail: 4. State Management, Options

## `useState`

```javascript
function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      Count: {count}
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
    </div>
  );
}
```

Notes:

- every time that button gets clicked, state gets updated, & component re-rendered
- If you need to manage more than one property, you just add more `useState`

Great for

- managing individual component state
- closely related components

...

and then a whole bunch of other great options:

---

Trail: 4. State Management, Options

## `useReducer`

## `useContext`

<!-- .element: class="fragment" -->

## `Redux`

<!-- .element: class="fragment" -->

## `MobX`

<!-- .element: class="fragment" -->

## `mobx-state-tree`

<!-- .element: class="fragment" -->

Notes:

Many options for dealing with application-level state

- useReducer: more complicated state that depends on the previous state
- useContext: for managing state across a large sub-tree
- redux - application state that provides middleware in your state mgmt
- mobx - application-level state mgmt w/ observables
- mobx-state-tree - more opinionated version of MobX

- caution: don't use these unless you know you need them
