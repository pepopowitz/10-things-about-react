---
Footer: false

<!-- .slide: data-background="/images/show-me-0.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-1-components.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

## Notes: React is based on components

---

Trail: 1. Components

> Build **encapsulated components** that manage their own state, then **compose them** to make complex UIs.

[reactjs.org](reactjs.org)

Notes:

straight from docs

This is _different_ from when we were doing MVC/MVVM

And the other major players right now are doing the same thing

---

Trail: 1. Components

<!-- .slide: data-background="/images/artsy-components-1.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

Whereas we used to think of an app like this in terms of one page and/or one controller

---

Trail: 1. Components

<!-- .slide: data-background="/images/artsy-components-2.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

Now we think in terms of this page being composed of many components

https://your-first-react-app.stevenhicks.me/#p70

---

Trail: 1. Components

<!-- .slide: data-background="/images/artsy-components-3.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

And those components are composed of _other_ components

...

This is actually an activity I do when I'm developing a new feature:

Draw out the component boundaries before I start coding it.

...

But if we do a good job of identifying our component boundaries,

---

Trail: 1. Components

Layout: inverse

<!-- .slide: data-background="/images/lego-artsy-bin.jpg" data-background-size="100%" -->

Notes:

It's almost like we have a bunch of legos ready to assemble

---

Trail: 1. Components

Layout: inverse

<!-- .slide: data-background="/images/lego-artsy-artwork.jpg" data-background-size="100%" -->

Notes:

And we can build bigger blocks with those legos,

---

Trail: 1. Components

Layout: inverse

<!-- .slide: data-background="/images/lego-artsy-artworks.jpg" data-background-size="100%" -->

Notes:

And then we can take a bunch of those slightly larger blocks

---

Trail: 1. Components

Layout: inverse

<!-- .slide: data-background="/images/lego-artsy-level-2.jpg" data-background-size="100%" -->

Notes:

And we can build an entire app with them

---

Trail: 1. Components

<!-- .slide: data-background="/images/building-blocks.jpg" -->

Notes:

https://your-first-react-app.stevenhicks.me/#p82

In order to do this well, we really need to focus on isolation of our components.

(left image: not properly isolated, one component that does several things)

(right image: properly isolated; components are building blocks.)

---

Trail: 1. Components

## **Isolation of components** leads to reusability

Notes:

_Not_ the other way around. So focus on proper isolation.

---

Trail: 1. Components

## The most important contribution from React is **thinking in terms of components**

Notes:

Components aren't unique to react,

but React popularized this approach

and it is IMO the single biggest contribution from React.

---

Trail: 1. Components

> Conceptually, components are like **JavaScript functions**. They accept arbitrary **inputs**... and return React elements describing **what should appear on the screen**.

[reactjs.org](reactjs.org)

---

Trail: 1. Components, Are Functions

<!-- .slide: data-background="/images/component-f-props.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

- they take inputs (props)

- they render to the screen

---

Trail: 1. Components, Are Functions

> [a component function...] **should be pure**, meaning that it does not modify component state, it returns the same result each time it’s invoked, and it does not directly interact with the browser.

[reactjs.org](reactjs.org)

Notes:

- they should be pure

- what's a pure function?

---

Trail: 1. Components, Are Functions, And Are Pure

## A pure function:

- ### is deterministic

- ### does not have side-effects

---

Trail: 1. Components, Are Functions, And Are Pure

## Pure 👍🏽

```
function add(a, b) {
  return a + b;
}
```

Notes:

examples

---

Trail: 1. Components, Are Functions, And Are Pure

## Impure 👎

```
function now() {
  return new Date();
}
```

Notes:

doesn't return the same result each time it's called

---

Trail: 1. Components, Are Functions, And Are Pure

## Impure 👎🏽

```
function decrement() {
  this.x = this.x - 1;
}
```

Notes:

It modifies state

---

Trail: 1. Components, Are Functions

```
import React from 'react';

function Artist(props) {
  console.log(props.name, props.url);
}
```

Notes:

Here's what a function component looks like.

This is a component that isn't actually _rendering_, it's just logging

But you can see it's got two inputs being passed in via props - a name and a url.

...

if this is what inputs look like; how does it render to the browser?

---

Trail: 1. Components, Are Functions, createElement

```
function Artist(props) {
  return React.createElement('div');
}
```

```
<div />
```

<!-- .element: class="fragment" -->

Notes:

using a helper from React named createElement

Give it the element type

...

rendered to browser as a div

---

Trail: 1. Components, Are Functions, createElement

```
function Artist(props) {
  return React.createElement(
    'div',
    { id: 'artist-wrapper' },
    'Hi!'
  );
}
```

```
<div id="artist-wrapper">Hi!</div>
```

Notes:

2nd arg - attributes to apply to element

3rd arg - child elements!

---

Trail: 1. Components, Are Functions, createElement

```
function Artist(props) {
  return React.createElement(
    'div',
    { id: 'artist-wrapper' },
    props.name
  );
}
```

```
<div id="artist-wrapper">Andy Warhol</div>
```

Notes:

We can use a prop as a child text element!

When the prop changes, React will re-render

---

Trail: 1. Components, Are Functions, createElement

```javascript
function Artist(props) {
  return React.createElement(
    'div',
    null,
    React.createElement('h1', null, 'Artworks by ' + props.name)
  );
}
```

```
<div>
  <h1>Artworks by Andy Warhol</h1>
</div>
```

Notes:

We've looked at some simple examples, but usually our components are more complex

We might want to render markup like this:

---

Trail: 1. Components, Are Functions, createElement

```
<div id="artist">
  <div id="bio">
    <h1>Andy Warhol</h1>
    <h2>American, 1928 - 1987</h2>
  </div>
  <div id="photo">
    <a href="/artists/andy-warhol">
      <img src="/artists/andy-warhol/image" alt="Andy Warhol" />
    </a>
  </div>
</div>
```

Notes:

And in that case, the createElement statements would look like this:

---

Trail: 1. Components, Are Functions, createElement

```
function Artist(props) {
  return React.createElement(
    'div',
    { id: 'artist' },
    React.createElement(
      'div',
      { id: 'bio' },
      React.createElement('h1', null, props.name),
      React.createElement('h2', null, props.origin + ', ' + props.lifespan)
    ),
    React.createElement(
      'div',
      { id: 'photo' },
      React.createElement(
        'a',
        {
          href: '/artists/' + props.id,
        },
        React.createElement('img', {
          src: props.profileImageUrl,
          alt: props.name,
        })
      )
    )
  )
}
```

Notes:

As you can see, that's just not sustainable.

So while you'll build your UI with a series of React.createElement calls,

there's another abstraction you'll want to use that will make your life easier.

And that brings us to....
