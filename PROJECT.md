# PROJECT.md
<!-- Read this before working on the project. The /clarify and /build skills read it first.
     Keep it short. Replace the <...> parts; /build can fill Stack and Commands for a new project. -->

## Project
Havalimanı Kuş Kaçışı: tarayıcıda oynanan, uçaklardan ve helikopterden kaçan sevimli bir kuş oyunu (spec: `specs/havalimani-kus-oyunu.md`).

## Stack
Tek dosya HTML + Canvas + saf JavaScript (`src/index.html`), bağımlılık yok. Testler: Node.js 18+ yerleşik test aracı (`node --test`). Oyun kuralları `<script id="game-logic">` bloğunda DOM'suz durur; testler bu bloğu Node'da çalıştırır.

## Commands
- Install: gerek yok (yalnızca Node.js 18+)
- Run: `open src/index.html` (macOS) veya dosyayı tarayıcıda açın
- Test: `npm test`

## Rules
- Reply in the language the user writes in.
- Prefer simple, readable code over clever code. Small functions, clear names.
- Every change comes with tests. Run them before saying something works.
- Don't add a dependency without asking.
- Never put passwords, API keys or tokens in code.
- Specs live in `specs/`. When the code and the spec disagree, ask.

## Don't touch
<Files or folders the AI must not change, e.g. `.env`>
