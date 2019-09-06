---
Footer: false

<!-- .slide: data-background="/images/show-me-6-dev-ex.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-7-testing.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

#5 on the board

I am a _huge_ fan of writing automated tests in general

and the tooling for writing tests in React is the best I've experienced.

---

Trail: 5. Testing

## Jest

> Jest is a **delightful** JavaScript Testing Framework with a focus on **simplicity**.

[jestjs.io](https://jestjs.io)

Notes:

jest is not required to test React,

and React isn't required to use Jest

but Jest was born out of the React community

---

Trail: 5. Testing, Jest

## Easy setup

Notes:

- easy setup

- no configuration needed

- finds your tests if they're there

---

Trail: 5. Testing, Jest

## Interactive watch mode

Notes:

- by default runs only the tests affected by your uncommitted local changes

- great for TDD

- running only a few tests that you're actively interested in

---

Trail: 5. Testing, Jest

## Great error messages

<img data-src="/images/jest-error.jpg" width="70%"/>

Notes:

- helps you quickly identify what's wrong with your test

---

Trail: 5. Testing, Jest

```javascript
describe('findSimilarArtists', () => {
  it('finds similar artists for Andy Warhol', () => {
    const result = findSimilarArtists('Andy Warhol');

    expect(result[0]).toEqual('Robert Indiana');
  });
});
```

Notes:

syntax

- describe
- it
- act
- assert
  - assertions are called "matchers"

---

Trail: 5. Testing, Jest

```javascript
expect(a).toEqual(b);

expect(a).not.toEqual(b);

expect(a).toBeGreaterThan(b);

expect(a).toBeNull();

expect(a).toBeUndefined();
```

Notes:

Over 30 different matchers out of the box

You can write custom ones

---

Trail: 5. Testing

## react-testing-library

Notes:

And then for specifically testing React,

there's a great library called r-t-l

You can use it with Jest

---

Trail: 5. Testing, react-testing-library

```javascript
describe('ArtistDetail', () => {
  it('renders something', () => {

    const context = render(
      <ArtistDetail artist={...} />
    );

    const button = context.queryByText('Details');
    fireEvent.click(button);

    expect(context.getByTestId('artist-details'))
      .toHaveTextContent('Andy Warhol')

  });
});
```

Notes:

Great API for

- rendering
- interacting with elements
- asserting presence of elements

...

There are other libraries for testing React, too - Enzyme is a popular one

But this is the boss hog of testing in react.
