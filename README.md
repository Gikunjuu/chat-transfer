# Chat Transfer

Move conversations between Claude, ChatGPT and Gemini, or from one account to another.

Neither ChatGPT nor Claude has a way to import a conversation. Both can export one. This page reads those exports in your browser and turns them into text you paste into a new chat on the other side.

## How it works

1. Export your data. ChatGPT: Settings, Data controls, Export data. Claude: Settings, Privacy, Export data (several zips, including memory). Gemini: takeout.google.com, My Activity, Gemini Apps.
2. Open the page and drop the .zip files onto it. Your chats and Claude Projects appear in a list.
3. Tick what you want, pick a destination, copy, and paste into a new chat in the other account.

For two or more items you choose how to move them: one chat at a time (each becomes its own new chat), one bundle (a single chat that remembers all of them, split into numbered parts when it is too long for one paste), a Markdown file to add to a Claude Project, or a folder of files as a plain-text backup.

Before copying you can redact emails, phone numbers, card numbers and API keys. Duplicate chats (same title, started within a day) are grouped and left unticked by Select all.

## Privacy

Everything runs in the browser. Nothing is uploaded. Imported chats are stored in the browser's IndexedDB on your machine and can be removed from the page or by clearing site data.

The only network request is for [JSZip](https://stuk.github.io/jszip/) from cdnjs, used to read the export .zip.

## Hosting

Static files, no build step. Point Netlify, GitHub Pages, or any static host at the repository root. `_headers` sets cache rules for Netlify.

## Files

- `index.html`: the whole app
- `fonts/`: web fonts
- `_headers`: Netlify cache headers
