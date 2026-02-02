# Anki-Minimalist-CSS
CSS Styling for Anki Flashcards

A clean, high-readability CSS theme for Anki cards, specifically designed for law students or anyone dealing with complex lists and citations (like ZPO/BGB paragraphs).
## Features
* **Night Mode Ready:** Automatically switches to a dark charcoal theme to reduce eye strain.
* **Spacing Fixes:** Removes the awkward "double-gap" between text and lists.
* **Modern Aesthetic:** Includes subtle shadows and borders to make cards feel like physical objects.

## Code Explanation:

### 1. The Container (`.card`)
We use a soft blue-grey (`#2c3e50`) instead of pure black for the text. Pure black on white backgrounds creates high contrast that can tire the eyes during 500-card review sessions. The `border-radius` and `box-shadow` give the card a modern, "App-like" feel.

### 2. The List Fix (`.card ul`)
By default, browsers add a large top margin to lists. By setting `margin-top: 0;`, the first bullet point sits directly under your introductory text (e.g., "Eselsbrücke:"), keeping the logical connection between the header and the list. Note that CSS requires a dot (`1.5`) rather than a comma (`1,5`) for decimals.

### 3. Night Mode Logic
Anki uses a specific class `.nightMode`. By combining it with your card class (`.nightMode.card`), the colors "flip" automatically based on your app settings. We use `#2b2b2b` (Charcoal) instead of pure black to prevent "OLED smearing" and text bleeding.

### 4. Paragraph/Div Reset
Anki's editor often wraps text in `<div>` tags which add unexpected line breaks. The `margin-bottom: 0;` rule ensures your text stays compact and doesn't create huge white spaces between sentences.

---

## How to use

1. **Open Anki** and select your Deck.
2. **Click Edit** on a card, then click the **Cards...** button.
3. **Paste the code** into the **Styling** column (the center pane).
