---
Footer: false

<!-- .slide: data-background="/images/show-me-7-testing.jpg" data-background-size="100%" data-background-color="#ffffff" -->
---

Footer: false

<!-- .slide: data-background="/images/show-me-8-performance.jpg" data-background-size="100%" data-background-color="#ffffff" -->

<audio data-autoplay>
  <source data-src="/images/sounds-bing.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

Notes:

Performance is built into react

---

Trail: 8. Performance

## Reconciliation

Notes:

Some neat techniques to make sure your app renders quickly

including the most well-known, Reconciliation

- aka virtual-dom diffing

- renders component to a "virtual" dom

- compares that virtual dom to actual dom

- only updates that which has changed

- perf because slowest part of any UI is the actual commits to the DOM.

---

Trail: 8. Performance

## Tips from the pros

[reactjs.org/docs/optimizing-performance.html](https://reactjs.org/docs/optimizing-performance.html)

Notes:

Tips from the React docs

Unusual, these types of tips usually come in unofficial blog posts

more than 6 suggestions, from...

- Use prod build to...
- not mutating data unnecessarily
- windowing/virtual scroll - render only the visible parts of a large list

---

Trail: 8. Performance
Footer: false

## Profiling

<img src="/images/react-profiler.jpg" alt="React profiler" width="80%"/>

Notes:

Includes tips for profiling via your browser,

or via a profiler built into the React dev tools.
