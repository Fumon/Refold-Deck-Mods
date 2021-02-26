## Description

This mod allows the user to unhide furigana on desktop by pressing the `P` key. The key can also be customised.

## Instructions

If you need help reading these instructions, this *[guide to modding anki](../../../How-To-Mod.md)* might help. Once you've read it, follow along below.

1. In the "Front Template" tab of the card editor, copy the following and paste it on a new line after everything that's already there

```html
<script>
  document.addEventListener('keydown', (event) => {
    if (event.keyCode === 80) {
      const element = document.querySelector('#word ruby rt');
      element.style.visibility = "visible";
    }
  });
</script>
```

2. (optional) If you want to customise the key used to unhide the furigana, first make sure that the key isn't already used by Anki to perform another action while reviewing cards. Then use *[this website](https://keycode.info)* to figure out the corresponding keycode. Finally you can simply replace the current keycode `80` with your personal one in this line:
```js
if (event.keyCode === 80) {
```

3. You're done!
