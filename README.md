# Anki image annotation card

![Demo](https://raw.githubusercontent.com/nostrenz/anki-image-annotation-card/master/gif/demo.gif)

An Anki card for highlighting words and displaying translations on top of an image.
Works in the Anki desktop application as well as in AnkiDroid.

## Setup

1. Create a new note type with at least the following fields:

	* Content
	* Image

2. Create a new card type and paste the code from this repository in it:

	* Front.html -> Front Template
	* Back.html -> Back Template
	* Styling.css -> Styling

And that's it. From there you can start creating cards.
For each new card, you'll have to drag & drop an image into the "Image" field (which will simply fill it with an image tag like `<img src="image.jpg">`).
The content field will contain the HTML for words and translations added on top of the image, fortunalty you don't have to write that yourself as the card can [produce it for you](#Edition).

Optionnally, you can also install the font "_CC Wild Words_" on your system.
If not installed, a default font will be used instead.

## Controls

Here's what the different buttons above the image do:

### ☀

Switches between the light and dark theme.

### Word <-> Translation

Switches between displaying the words or the translations.

* Words consit of a box ideally placed above a word in the image.
Each word can have a reading and meaning which will be displayed in a popup next to the word when you place your mouse cursor over it (or tap on it in AnkiDroid).

* Translations are text bubbles ideally placed above a whole text in the image.
The bubble can contain whatever text you want.

### Edit

Toggles the edit mode.
Refer to the [Edition](#Edition) section below to learn how it works.

### Debug

Toggles the debug view.
Display some informations which could be useful if you want to modify the code yourself.

### Font size slider

Changes the font size for the text inside a word popup or a translation.

## Edition

Allows to add, update or remove words and translation on top of the image.
When enabled, you'll see a box appearing near the center of the image with a form attached next to it.

![Edit](https://raw.githubusercontent.com/nostrenz/anki-image-annotation-card/master/gif/edit.gif)

* To **add** a word, simply move the box by dragging the top-left corner and resize it with the bottom-right corner.
Once the box is above a word in the image, you can fill the fields next to it then click the `Add` button.

* To **update** or **delete** an existing word, simply click on it and the box will move over it. From there, you can delete
it by clicking the `Delete` button, or you can update it by changing what's in the form fields and clicking on the `Update` button.
If you move/reisze the box before clicking the `Update` button, the word will also be moved to that new location.

Editing translations works exactly the same way as words, you just have to switch mode with the `Word <-> Translation` button above.

The selected theme (light/dark) and font size (with the slider) are also taken into account during edition so they can be persisted with the card.

Once you're done editing, click the `Edit` button again to disable the edit mode, and the new HTML content will be copied into the clipboard.
You'll then need to put it in the card's Content field to persit the changes.

The edit view doesn't work properly on AnkiDroid as the box can't be moved/resized and the keyboard doesn't show up when focusing one of the text fields,
but that's probably not too much of a problem as editing on a phone would probably not be very practical anyway.
