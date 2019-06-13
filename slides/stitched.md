---
title: 10 Things You'll Love About React - Steven J Hicks
theme: css/theme.css
revealOptions:
  transition: 'none'
  controls: false
  progress: false
  center: true
css: css/custom.css
preprocessor: _build/inject.js
width: '100%'
height: '100%'
---
Footer: false

<!-- .slide: data-background="/images/some-title.jpg" class="title" -->

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" style="width:0;height:0;position:absolute;overflow:hidden;">
  <defs>
<symbol viewBox="0 0 567.31298828125 409.60003662109375" aria-labelledby="apsi-zocial-cloudapp-title" id="si-zocial-cloudapp"><title id="apsi-zocial-cloudapp-title">icon cloudapp</title><path d="M.001 280.576c0-35.504 12.544-65.872 37.632-91.136 25.087-25.264 55.215-37.888 90.368-37.888l.511.512c0-1.024-.08-2.224-.255-3.584-.176-1.36-.256-2.384-.256-3.072 0-40.272 14.08-74.576 42.24-102.912C198.401 14.16 232.449 0 272.385 0c35.152 0 66.048 11.264 92.672 33.792s43.008 50.864 49.152 84.992h8.704c39.92 0 73.984 14.16 102.144 42.496s42.256 62.64 42.256 102.912c0 40.288-14.096 74.592-42.256 102.928s-62.223 42.48-102.144 42.48c-2.736 0-4.784-.16-6.144-.495v.495H120.816v-.512c-33.792-1.712-62.367-15.023-85.76-39.935C11.68 344.24 0 314.72 0 280.576z"/></symbol>
<symbol viewBox="0 0 514.8550415039062 347.53997802734375" aria-labelledby="aysi-zocial-email-title" id="si-zocial-email"><title id="aysi-zocial-email-title">icon email</title><path d="M0 316.758V30.782c0-.33.496-3.475 1.49-9.433l168.308 143.98L1.986 326.688c-1.323-4.634-1.985-7.944-1.985-9.93zM22.342 1.49C24.659.497 27.472 0 30.782 0h453.29c2.98 0 5.958.497 8.937 1.49L324.204 145.968l-22.342 17.873-44.187 36.244-44.187-36.244-22.342-17.873zm.496 344.56L192.14 183.7l65.536 53.123 65.536-53.124L492.513 346.05c-2.648.994-5.461 1.49-8.44 1.49H30.783c-2.649 0-5.297-.496-7.945-1.49zm322.716-180.719L513.366 21.35c.993 2.98 1.489 6.124 1.489 9.434V316.76c0 2.978-.496 6.288-1.49 9.93z"/></symbol>
<symbol viewBox="0 0 640.0180053710938 520.3389892578125" aria-labelledby="dnsi-zocial-twitter-title" id="si-zocial-twitter"><title id="dnsi-zocial-twitter-title">icon twitter</title><path d="M0 461.54c10.42 1.014 20.826 1.548 31.22 1.548 61.048 0 115.528-18.732 163.387-56.17-28.424-.352-53.933-9.041-76.477-26.043-22.57-16.99-37.984-38.675-46.323-65.056 6.933 1.418 15.102 2.095 24.456 2.095 12.15 0 23.766-1.575 34.862-4.684-30.517-5.866-55.766-20.891-75.709-44.996-19.955-24.13-29.919-51.969-29.919-83.527v-1.574c18.395 10.42 38.31 15.805 59.826 16.13-18.016-11.798-32.338-27.304-42.915-46.57-10.575-19.24-15.87-40.13-15.87-62.675 0-23.597 6.088-45.607 18.212-66.095 32.6 40.586 72.418 72.938 119.431 97.055 47 24.092 97.368 37.53 151.158 40.327-2.432-11.448-3.655-21.516-3.655-30.18 0-36.085 12.84-66.954 38.505-92.62C375.868 12.839 406.893 0 443.342 0c37.79 0 69.7 13.88 95.73 41.64 30.167-6.257 57.926-17.015 83.255-32.261-9.718 31.558-28.815 55.845-57.238 72.847 25.327-3.109 50.304-10.055 74.929-20.813-16.651 26.017-38.336 48.742-65.056 68.151v17.198c0 34.992-5.125 70.128-15.35 105.355-10.211 35.214-25.848 68.853-46.83 100.972-20.996 32.065-46.05 60.619-75.189 85.569-29.126 24.977-64.08 44.853-104.849 59.592-40.755 14.752-84.555 22.089-131.398 22.089-72.483-.014-139.606-19.605-201.345-58.8z"/></symbol>
  </defs>
</svg>

# 10 Things You'll Love About React

## Steven Hicks

<svg class="icon">
  <use xlink:href="#si-zocial-twitter" />
</svg>@pepopowitz

<svg class="icon">
  <use xlink:href="#si-zocial-email" />
</svg>steven.j.hicks@gmail.com

<svg class="icon">
  <use xlink:href="#si-zocial-cloudapp" />
</svg>stevenhicks.me/10-things-about-react

Notes: STICKERS!

- thanks to organizers

---

Footer: false

<!-- .slide: data-background="/images/artsy.svg" data-background-size="750px" data-background-color="black" -->

Notes:

NYC, MKE

our mission is to expand the art market,

and we're doing that with a platform for collecting and discovering art.

---

some sort of intro. Why are we talking about this?
---
Layout: module
# 1. Components
---

Trail: 1. Components

- mvc/mvvm: controllers & pages

---

Trail: 1. Components

- react & modern frameworks: components

  - most important thing about React: component mindset
  - what's the biggest advantage(s)?

---

Trail: 1. Components

- Legos

---

Trail: 1. Components, Legos

- draw out component boundaries in a site
  - https://your-first-react-app.stevenhicks.me/#p70

---

Trail: 1. Components

- Composability
  - passing props to children

---

Trail: 1. Components

- Isolation first; reuse comes as a natural side-effect.

  - Importance of identifying boundaries: https://your-first-react-app.stevenhicks.me/#p82

---

Trail: 1. Components

- suitcase principle factors in? (code organization)

---

Trail: 1. Components

- components in react are functions

  - https://your-first-react-app.stevenhicks.me/#p85

---

Trail: 1. Components, Are Functions

- they should be pure
  - what's a pure function?

---

Trail: 1. Components, Are Functions

- they take inputs (props)

---

Trail: 1. Components, Are Functions

- they render to the screen

---

Trail: 1. Components, Are Functions

- createElement

  - https://your-first-react-app.stevenhicks.me/#p98

---

Trail: 1. Components, Are Functions, createElement

- example with 1 arg

---

Trail: 1. Components, Are Functions, createElement

- example with 2 args

---

Trail: 1. Components, Are Functions, createElement

- example with 3 args

---

Trail: 1. Components, Are Functions, createElement

- complex example

Notes:

- transition:
  - but no one builds a react app with createElement, because there's a better way...
  - show me JSX!
---
Layout: module
# 2. JSX
---

Trail: 2. JSX

- https://your-first-react-app.stevenhicks.me/#p111

---

Trail: 2. JSX

- example with 1 arg

---

Trail: 2. JSX

- nested example

---

Trail: 2. JSX

- you might think you'll hate it
  - combo of xml & javascript, yikes!
  - but react.createElement is verbose & gross

---

Trail: 2. JSX

- complex example

---

Trail: 2. JSX

- separation of concerns
  - https://your-first-react-app.stevenhicks.me/#p121
  - no, separation of _technologies_

---

Trail: 2. JSX

- JSX lets us write everything in JavaScript

  - maybe you don't like JS?
  - but it means we get to use modern JS features!

---

Trail: 2. JSX

- components + jsx lead to _declarative_ code

---

Trail: 2. JSX, Declarative

- demo declarative vs imperative (https://your-first-react-app.stevenhicks.me/#p46)
  - how do you get to my house?

---

Trail: 2. JSX, Declarative

- show example of code

---

Trail: 2. JSX, Declarative

- imperative code is abstracted so we can call it declaratively

---

Trail: 2. JSX, Declarative

- declarative code leads to simplicity & predictability
---
Layout: module
# 3. Styling

Notes: (number 8 on the board)
---

Trail: 3. Styling

- so many options!

---

Trail: 3. Styling

- Most importantly, styles go with components

---

Trail: 3. Styling

- CSS/SCSS

---

Trail: 3. Styling

- CSS Modules

---

Trail: 3. Styling

- CSS-in-JS
  - Styled components

---

Trail: 3. Styling

- Separation of Concerns again

---

Trail: 3. Styling

- But you also might not like it! [X]
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
---
Layout: module
# 5. New Features

Notes:
#5 on the board
---

Trail: 5. New Features

- Hooks

---

Trail: 5. New Features, Hooks

- useState

---

Trail: 5. New Features, Hooks

- useContext

---

Trail: 5. New Features, Hooks

- useEffect

---

Trail: 5. New Features, Hooks

- closures
  - find a good way to explain how each render closes over its hooks
    - and how each time it renders, it gets a new closure

---

Trail: 5. New Features, Hooks, Closures

- you might not like them! [XX]

---

Trail: 5. New Features

- Suspense (no more "isLoading"!)

---

Trail: 5. New Features

- "Minor" version
  - Backwards compatible - you can do things the old way, too
---
Layout: module
# 6. Developer Experience

Notes: #3 on the board
---

Trail: 6. Developer Experience

- tooling

---

Trail: 6. Developer Experience, Tooling

- hot-reloading

---

Trail: 6. Developer Experience, Tooling

- webpack (if you don't have to worry about configuring it)

---

Trail: 6. Developer Experience, Tooling

- babel/modern JS

---

Trail: 6. Developer Experience, Tooling

- TypeScript/flow
  - https://your-first-react-app.stevenhicks.me/#p182

---

Trail: 6. Developer Experience, Tooling

- prettier!

---

Trail: 6. Developer Experience, Tooling

- You might not like Decision Fatigue! [XXX]

---

Trail: 6. Developer Experience

- react dev tools

---

Trail: 6. Developer Experience

- testing
---
Layout: module
# 7. Testing

Notes:

#4 on the board

https://your-first-react-app.stevenhicks.me/#p290

---

Trail: 7. Testing

- Jest
  - (https://steven-j-hicks-speaking.netlify.com/test-driven-javascript/#p18)

---

Trail: 7. Testing, Jest

- easy setup, no configuration

---

Trail: 7. Testing, Jest

- interactive watch mode

---

Trail: 7. Testing, Jest

- great error messages

---

Trail: 7. Testing, Jest

- syntax

---

Trail: 7. Testing, Jest

- matchers

---

Trail: 7. Testing

- react-testing-library

---

Trail: 7. Testing, react-testing-library

- render

---

Trail: 7. Testing, react-testing-library

- find

---

Trail: 7. Testing, react-testing-library

- assert

---

Trail: 7. Testing, react-testing-library

- interact

---

Trail: 7. Testing

- enzyme

---

Trail: 7. Testing, enzyme

- a ton more ways to test a react app
---
Layout: module
# 8. Performance

Notes:
#7 on the board
---

Trail: 8. Performance

- virtual dom/reconciliation

---

Trail: 8. Performance

- tell a component when to update

---

Trail: 8. Performance

- virtualization/windowing
  - react-window

---

Trail: 8. Performance, Windowing

- example: https://react-window.now.sh/#/examples/list/fixed-size

---

Trail: 8. Performance

- profiler
---
Layout: module
# 9. Community

Notes:
#10 on the board
---

Trail: 9. Community

- Core team

---

Trail: 9. Community, Core Team

- transparency about upcoming releases

---

Trail: 9. Community, Core Team

- stability
  - backwards compatible
  - prior to hooks/suspense, there were minimal changes for 5 years!

---

Trail: 9. Community

- Docs

---

Trail: 9. Community

- larger dev community

---

Trail: 9. Community, Others

- ryan florence, kent dodds, cory house

---

Trail: 9. Community, Others

- list some courses
---
Layout: module
# 10. create-react-app

Notes:
#6 on the board
---

Trail: 10. create-react-app

- Getting started is so easy

---

Trail: 10. create-react-app

- Drawing of cra boxing together

---

Trail: 10. create-react-app

- Eject

---

Trail: 10. create-react-app

- This is your next step!
---

Footer: false

<!-- .slide: data-background="/images/drawings/some-title.jpg" class="title" -->

# Thank you!

## Steven Hicks

<svg class="icon">
  <use xlink:href="#si-zocial-twitter" />
</svg>@pepopowitz

<svg class="icon">
  <use xlink:href="#si-zocial-email" />
</svg>steven.j.hicks@gmail.com

<svg class="icon">
  <use xlink:href="#si-zocial-cloudapp" />
</svg>stevenhicks.me/10-things-about-react

Notes:

- Thank you for your time!

- Questions afterward

- Enjoy the rest of \_\_\_

---

Layout: resources

Trail: Resources

- [resource](/link)
