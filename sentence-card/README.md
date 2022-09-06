# Anki annotation cards / Sentence card

![Demo](https://raw.githubusercontent.com/nostrenz/anki-image-annotation-card/master/sentence-card/demo.gif)

An Anki card for annotating a sentence by selecting parts of the text.

## Setup

1. Create a new note type with at least the following fields:

	* Sentence
	* Meaning

2. Create a new card type and paste the code from this repository in it:

	* sentence-card/Front.html -> Front Template
	* sentence-card/Back.html -> Back Template
	* sentence-card/Styling.css -> Styling

## Usage

First, create a new card with any sentence in the "Sentence" field.
When opening the card using the Anki desktop application you can select any part of that sentence and a form will appear allowing to add a reading and a meaning to the selected part.
Then, by clicking the "OK" button under the form the selected part will be underlined and hovering it with the mouse cursor will display a popup with the added reading and meaning.

Each time you add a new word that way, you'll see a small popup in the top-left corner telling you the HTML content has been copied in the clipboard. To persist those changes into the card, simply paste what's now in the clipboard in the card's Sentence field (don't forget to toggle the HTML editor first by pressing `Ctrl+Shift+X` when the field is focused).
