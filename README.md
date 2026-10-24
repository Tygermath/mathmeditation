# Math Meditation app

Open `index.html` in a browser (double-click). No install or server needed. Keep the `assets` folder next to it.

- Menu tree: Vol → Chapter → Section → Trick (left side).
- Each trick: ① Catchy phrase (口訣), ② Visual aid (圖像), ③ Exemplar problems (啟蒙題/典範題: the fixed questions from the worksheets, shown side by side for comparison), ④ Random practice (隨機練習題: endless similar questions). Both practice pages have: type answer, Check, Show answer & explanation, Upload working.
- 3 correct answers in a row in Random practice (first try, no peeking) earns a ★. Exemplar problems show a done-count only.
- Progress is saved in the browser (localStorage); uploaded photos/PDFs are saved in the browser (IndexedDB) and never leave the device.

## Languages
English (default), 中文, Français — switch with the buttons at the top of the left menu; the choice is remembered.

## Adding content
Everything is in `index.html`:
- `TRICKS['1A-2.3-1'] = { name, zh0, tip, explain, pic, gen() } (name, tip, explain are X(en, zh, fr))` — `gen()` returns `{q, a, steps}` (or `{q, choices, a: index, steps}` for multiple choice).
- `FIXED['id']` lists the exemplar problems (built with the `B.*` helpers) for each trick.
- `TREE` lists which tricks belong to which volume / chapter / section.
