---
Footer: false

<!-- .slide: data-background="/images/show-me-4-state-mgmt.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-5-new-features.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

#5 on the board

React hadn't really changed for a few years

until this year.

---

Trail: 5. New Features

## Hooks

> Hooks are functions you can use in a Component to perform impure actions from a pure function.

Notes:

Remember we said our components are pure functions,

and pure functions shouldn't have side-effects, or change state

Hooks allow us to do that safely,

and in a way that allows React to re-render components when it needs to

---

Trail: 5. New Features, Hooks

## `useState`

## `useReducer`

<!-- .element: class="fragment" -->

## `useContext`

<!-- .element: class="fragment" -->

Notes:

- useState: For managing component state

- useReducer: For managing more complicated state

- useContext: For managing state across large subtrees

...

You might notice a pattern - all start with "use"

---

Trail: 5. New Features, Hooks

## `useEffect`

```jsx
function ArtistDetails(props) {
  const [artist, setArtist] = useState(null)

  useEffect(() => {
    const apiArtist = loadArtistFromApi(props.artistId)
    setArtist(apiArtist)
  }, [])

  return ( ... )
}
```

<!-- .element: class="fragment" -->

---

Trail: 5. New Features, Hooks

## `useEffect`

```jsx
function Chat(props) {
  useEffect(() => {

    socket.emit('join', { id: props.friendId });

    return () => {
      socket.emit('leave', { id: props.friendId });
    }

  }, [ props.friendId ])

  return ( ... )
}
```

Notes:

For performing side-effects from a component

- What to do to fire the effect
- what to do to clean up the effect
- when the effect should re-run

...

Notice: the "leaving" of a socket is going to happen in the future sometime

but we're still able to reference the friendId prop from when it rendered

---

Trail: 5. New Features, Hooks

## Closures

> A closure is the combination of a function and the lexical environment within which that function was declared.

[developer.mozilla.org](developer.mozilla.org)

Notes:

That's because JavaScript forms closures over variables when you declare a function

This is really helpful for the `useEffect` hook especially, and its multiple callback functions:

---

Trail: 5. New Features, Hooks

## `useEffect`

```jsx
function Chat(props) {
  useEffect(() => {

    socket.emit('join', { id: props.friendId });

    return () => {
      socket.emit('leave', { id: props.friendId });
    }

  }, [ props.friendId ])

  return ( ... )
}
```

Notes:

you know when your cleanup function executes, it's going to disconnect from the right friend's socket

...

But that's the happy path to closures in JavaScript.

They can be really difficult to understand and manage, even in React hooks,

---

Footer: false

<!-- .slide: data-background="/images/show-me-closures-strike.jpg" data-background-size="100%" -->

<audio data-autoplay>
  <source data-src="/images/sounds-buzzer.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

And so we'll give a strike for closures.

---

Trail: 5. New Features

## Suspense

> Suspense lets components “wait” for something before rendering.

[reactjs.org](reactjs.org)

Notes:

This is a really neat way to solve the problem that it takes time for browsers to load things.

Until Suspense, we've had to manage "isLoading" flags all over our app

---

Trail: 5. New Features, Suspense

```jsx
const ArtistGraphs = React.lazy(() => import('./ArtistGraphs'));

function Artist() {
  return (
    <React.Suspense fallback={<Loading />}>
      <ArtistGraphs />
    </React.Suspense>
  );
}
```

Notes:

now, we can use React Suspense to emit fallback content,

like a loading indicator,

until something finishes loading.

...

That currently includes the ability to load the code for a component separate from the main application, lazily, when the user actually needs it,

Soon, it will include the ability to emit fallback content

until **data fetching** is complete for a component

---

Trail: 5. New Features

## Backwards compatible

Notes:

- released as "Minor" version

- Backwards compatible - you can do things the old way, too

- This shows the care & consideration the React team takes to let you build your app the way YOU want to
