## Description

This mod adds additional fonts (and stroke order) to the front of the card. This mod currently adds 3 additional fonts:

Note: This specific mod will change in the future to allow more customization. Stay tuned.

- BOLD COMIC
- Kyokasho (More handwritten style)
- Stroke order

## Instructions

If you need help reading these instructions, this *[guide to modding anki](../../../How-To-Mod.md)* might help. Once you've read it, follow along below.

To get fonts into your Anki media folder, I have made a deck you have to import and sync.

1. Download, Import and Sync the deck(s) in [font_decks](font_decks). This will import the fonts you need for this mod to work.

2. In the "Front Template" tab of the card editor, copy the following and paste it on a new line after everything.

```html
<div>
  <span id="word" class="jp comic">{{furigana:Word}}</span>
  <span id="word" class="jp kyokasho">{{furigana:Word}}</span>
</div>
<span id="word" class="jp strokeorder">{{furigana:Word}}</span>
```

(Optional no-stroke order) If you want to remove the stroke order entry (It's pretty big so you can see the order numbers), you can use this instead.

```html
<div>
  <span id="word" class="jp comic">{{furigana:Word}}</span>
  <span id="word" class="jp kyokasho">{{furigana:Word}}</span>
</div>
```

3. In the "Styling" tab of the card editor, copy the following and paste it on a new line *after* everything that's already there

```css
@font-face { font-family: strokeorder; src: url('_strokeorder.ttf'); }
@font-face { font-family: hgrkk; src: url('_hgrkk.ttf'); }
@font-face { font-family: yugothb; src: url('_yugothb.ttc'); }

.comic {
	font-family: yugothb;
}

.kyokasho {
	font-family: hgrkk;
}

.strokeorder {
	font-family: strokeorder;
	font-size: 80px;
}
```

4. You're done! Hit save or "finished".



Support continued mod development. One time donation available.
[![Buy me a coffee!](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/mI8stwU4P)