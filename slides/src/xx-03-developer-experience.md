---
Footer: false

<!-- .slide: data-background="/images/show-me-5-new-features.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-6-dev-ex.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

#3 on the board

The developer experience in React is top-notch

starting with some non-react specifics, that you'd want in any framework

---

Trail: 6. Developer Experience

## Hot-reloading

Notes:

When you're dev'ing locally, you make changes and see changes _instantly_ in your browser

---

Trail: 6. Developer Experience

## webpack

Notes:

- integrates really easily with webpack

- reduces size of JavaScript bundle via tree-shaking, which removes unused code

- _if_ you don't have to worry about configuring it. That can be confusing.

---

Trail: 6. Developer Experience

## babel

```jsx
function Artists({ artists }) {
  return artists.map(artist => <ArtistDetail {...artist} />);
}
```

<!-- .element: class="fragment" -->

Notes:

- integrates easily with babel

- converts modern javascript syntax into javascript that is understood by all the browsers your app needs to support.

- this means we can use the latest javascript specs in our app!

...

destructuring; fat arrow function w/ implicit return; object spread

---

Trail: 6. Developer Experience

## TypeScript

Notes:

integrates easily with typescript

- allows you to treat javascript as a strongly-typed language

---

Trail: 6. Developer Experience

## TypeScript

```
interface ArtistProps {
  name: string,
  origin: string,
  url: string
}

function Artist(props: ArtistProps) {
  return (
    <div id="artist">
      <h1>
        <a href={props.url}>{props.name}</a>
      </h1>
      <h2>{props.origin}</h2>
    </div>
  )
}
```

Notes:

- Describe types

  - interface
  - strings
  - props: ArtistProps

---

Trail: 6. Developer Experience

## TypeScript

<img data-src="/images/type-check-error.png" width="90%"/>

Notes:

- when you use TS, you get compile-time errors about missing props

---

Footer: false

<!-- .slide: data-background="/images/show-me-decision-fatigue-strike.jpg" data-background-size="100%" -->

<audio data-autoplay>
  <source data-src="/images/sounds-buzzer.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

You might be catching on that there are a lot of decisions to be made

Something like Angular or Ember is going to tell you how to do things, and not leave you a lot of freedom

React will leave you a _lot_ of freedom in your implementation

But that can be a thing that is really overwhelming.

---

Trail: 6. Developer Experience

## Prettier

<img data-src="/images/prettier.gif" width="70%"/>

<!-- .element: class="fragment" -->

Notes:

one tool that can help you eliminate _some_ decisions is called Prettier

prettier is an opinionated code-formatter

...

so you can write your code however you want

and prettier will autoformat for you, and everyone on your team

so you never have to worry about arguing over style

---

Trail: 6. Developer Experience

## React Dev Tools

Notes:

browser extensions to help you identify what's happening in your react app.

---

Trail: 6. Developer Experience, React Dev Tools

<img src="/images/react-dev-tools.jpg" alt="React dev tools" width="80%"/>

Notes:

It makes it really easy to see if your component is getting the props you're expecting

which is really useful for debugging

...

One more piece of the developer experience is so great that it warrants its own place on our list -

...
