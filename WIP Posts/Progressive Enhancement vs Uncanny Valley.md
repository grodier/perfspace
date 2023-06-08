- Progressive Enhance or Uncanny Valley?
  - How to test?
    - Page with a link and long loading JavaScript - can link be clicked while JavaScript is loading/executing
    - Page with a link that has a button handler added early on but long running JavasScript in script following that - can link fall back to anchor or will wait for JavaScript?
    - Slow JavaScript:

```javascript
let startTime = performance.now();
while (performance.now() - startTime < 700) {
  // Do nothing for 700 ms to emulate extremely slow code
}
```

- Claims
  - This also introduces a new “uncanny valley” problem where your site appears loaded (HTML) but is unresponsive since the application JavaScript logic is still loading in the background. -- [Astro - MPA vs SPA](https://docs.astro.build/en/concepts/mpa-vs-spa/)
  - Functional is the baseline - JS used to enhance not enable -- [Kent C Dodds - PESPA](https://www.epicweb.dev/the-webs-next-transition)
