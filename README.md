# Mandarin Anki Flashcards

A starter Anki note type and example deck for studying Mandarin vocabulary.

## Files

- `cards.tsv` — 10 example cards, ready to import into Anki.
- `template/front.html` — Front card template (shows the hanzi).
- `template/back.html` — Back card template (pinyin, English, example sentence, notes).
- `template/styling.css` — Card styling, with dark-mode support.

## Note type fields

| # | Field          | Description                            |
|---|----------------|----------------------------------------|
| 1 | Hanzi          | Chinese characters (front of card)     |
| 2 | Pinyin         | Romanized pronunciation with tone marks|
| 3 | English        | English meaning                        |
| 4 | ExampleHanzi   | Example sentence in characters         |
| 5 | ExamplePinyin  | Example sentence pinyin                |
| 6 | ExampleEnglish | Example sentence translation           |
| 7 | Notes          | Usage notes, mnemonics, etc.           |

## One-time setup in Anki

1. **Tools → Manage Note Types → Add → Add: Basic** → name it `Mandarin Vocabulary`.
2. Click **Fields…** and add the seven fields above (delete the default `Front`/`Back`).
3. Click **Cards…**:
   - Paste the contents of `template/front.html` into **Front Template**.
   - Paste the contents of `template/back.html` into **Back Template**.
   - Paste the contents of `template/styling.css` into **Styling**.
4. Save and close.

## Importing the example cards

1. **File → Import…** and select `cards.tsv`.
2. Confirm:
   - Type: `Mandarin Vocabulary`
   - Deck: `Mandarin::Vocabulary`
   - Fields separated by: **Tab**
   - **Allow HTML in fields**: ✅ checked
3. Click **Import**. You should get 10 new cards.

> The header lines in `cards.tsv` (starting with `#`) tell Anki which note type, deck, and field order to use, so most settings are auto-detected.

## Adding more cards

Append rows to `cards.tsv` using the same tab-separated format, then re-import — Anki will skip duplicates of the `Hanzi` field.
