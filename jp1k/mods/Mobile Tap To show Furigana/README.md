## Description

This mod adds a "tap anywhere to view furigana" feature on mobile Anki apps. This makes it easier to check the hidden furigana if you have a tall phone or if you like leaving your fingers near the buttons.

**Warning** Untested: what this does with the AnkiDroid "Gestures" feature turned on

## Instructions

1. In the "Styling" tab of the card editor, copy the following and paste it on a new line after everything that's already there

```css
/* [mobile-only] Tap to show furigana */
 html.mobile:hover #word ruby rt {visibility:visible;}
```

2. You're done!


Support continued mod development. One time donation available.
[![Buy me a coffee!](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/mI8stwU4P)