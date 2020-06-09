# a11y.css

## Prefers Reduced Motion

```
@media (prefers-reduced-motion: reduce) {
```

> The prefers-reduced-motion CSS media feature is used to detect if the user has requested that the system minimize the amount of non-essential motion it uses. - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)

## Remove outline for mouse focus, preserves outline for keyboard users

```
:focus:not(:focus-visible) {
```

Original source code for altering focus outlines was inspired by an article published by [Patrick H. Lauke](https://developer.paciellogroup.com/blog/2018/03/focus-visible-and-backwards-compatibility/).

### Recommendation: Include active states in your custom CSS for your click events

Buttons when focused via keyboard for example should include outlines, or some visual feedback that the button is in a focus state.

However, when clicked using a mouse, the button would be active and not focused. Your styles _should_ reflect this new state for your users.

> It's a part of good UX to have :active styles, for feedback. This is usability, not accessibility. Focus outlines are not for clicking feedback. - [Lea Verou](https://twitter.com/LeaVerou/status/1047798141385359360)
