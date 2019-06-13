---
Layout: module
# 4. State Management

Notes:
#9 on the board
---

Trail: 4. State Management

- remember the drawing of a component as f(props)?

---

Trail: 4. State Management

- it's a lie. f(props, state).

---

Trail: 4. State Management

- example
  - counter?
  - (probably just a drawing showing that a component manages its state)

---

Trail: 4. State Management

- when you update state of a component, React re-renders it

Notes:

Mention there is no two-way binding for state mgmt - it's a one-directional loop.

---

Trail: 4. State Management

- state can be passed into child components (as props)

---

Trail: 4. State Management

- options!

---

Trail: 4. State Management, Options

- useState
  - for managing component state

---

Trail: 4. State Management, Options, useState

- example

---

Trail: 4. State Management, Options

- useContext
  - for managing state of a sub-tree

---

Trail: 4. State Management, Options, useContext

- drawing

---

Trail: 4. State Management, Options, useContext

- example (might not make the cut)
  - provider (at the top)
  - consumers

---

Trail: 4. State Management, Options

- redux, mobx
  - for managing state at the top of the tree

---

Trail: 4. State Management, Options, Redux/Mobx

- drawing

---

Trail: 4. State Management, Options, Redux/Mobx

- example (might not make the cut)

---

Trail: 4. State Management, Options, Redux/Mobx

- caution: don't use these unless you know you need them

---

Trail: 4. State Management

- elevate state? (not sure if...)
