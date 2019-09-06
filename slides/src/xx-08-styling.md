---
Footer: false

<!-- .slide: data-background="/images/show-me-2-jsx.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-3-styling.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

---

Trail: 3. Styling

## Styles Go With Components

Notes:

- Most importantly, styles go with components

- No massive stylesheet to style your entire app

- Remember that not much is built into React, so you have **So many options**!

---

Trail: 3. Styling

## CSS/SCSS

```
.artist {
  color: blueviolet;
  border-bottom: 1px solid blueviolet;
}
```

artist.css

```
import './artist.css';

function Artist(props) {
  return <div className="artist">{props.name}</div>
}
```

artist.jsx

Notes:

But you don't have to get super complicated.

You can just stick CSS stylesheets alongside each component, and import them

(Or SCSS if you prefer that)

---

Trail: 3. Styling

## CSS Modules

[https://github.com/css-modules/css-modules](https://github.com/css-modules/css-modules)

```
.artist {
  color: blueviolet;
  border-bottom: 1px solid blueviolet;
}
```

artist.css

```
import styles from './artist.css';

function Artist(props) {
  return <div className={styles.artist}>{props.name}</div>
}
```

artist.jsx

Notes:

- `import styles from`
- `className={styles.artist}`

---

Trail: 3. Styling

## CSS Modules

[https://github.com/css-modules/css-modules](https://github.com/css-modules/css-modules)

```
.Artist__artist__31BtE {
  color: blueviolet;
  border-bottom: 1px solid blueviolet;
}
```

CSS

```
<div class="Artist__artist__31BtE">Andy Warhol</div>
```

HTML

Notes:

when emitted to browser

- class name is mangled
- can't possibly conflict!

---

Trail: 3. Styling

## Styled Components

[styled-components.com/](https://www.styled-components.com/)

```
import styled from 'styled-components';

const brandColor = 'blueviolet';

const StyledArtist = styled.div`
  color: ${brandColor};
  border-bottom: 1px solid ${brandColor};
`;

function Artist(props) {
  return <StyledArtist>{props.name}</StyledArtist>;
}
```

Notes:

- CSS-in-JS

  - many other flavors!

---

Trail: 3. Styling

## Styled Components

[styled-components.com/](https://www.styled-components.com/)

```
.31BtE {
  color: blueviolet;
  border-bottom: 1px solid blueviolet;
}
```

CSS

```
<div class="31BtE">Andy Warhol</div>
```

HTML

---

Trail: 3. Styling, Separation Of Concerns

<!-- .slide: data-background="/images/slicing-vertical.jpg" data-background-size="75%" data-background-color="#ffffff" -->

Notes:

Tons of options

But you might not like the options, as they tend to be controversial especially amongst fans of CSS

---

Footer: false

<!-- .slide: data-background="/images/show-me-styling-strike.jpg" data-background-size="100%" -->

<audio data-autoplay>
  <source data-src="/images/sounds-buzzer.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

so let's give our first strike
