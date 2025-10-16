# Random Quote SPA

## Overview
This is a minimal single-page web app that fetches a random quote from a local quotes.json file and displays it inside the #quote element. It includes a button to fetch another random quote and a copy-to-clipboard helper.

- Data source: quotes.json (array of strings)
- Tech: Vanilla HTML/CSS/JS
- License: MIT

## Setup
Because modern browsers restrict fetching local files via the file:// protocol, you should serve the folder over a local static web server.

1) Place the provided files in the same directory:
   - index.html
   - quotes.json

2) Start a static server in that directory (choose any):
   - Python 3: python -m http.server 8080
   - Node (npx): npx serve -l 8080
   - Deno: deno run --allow-net --allow-read https://deno.land/std/http/file_server.ts

3) Open the app in your browser:
   - http://localhost:8080

Note: Caching is disabled for quotes.json in development via a timestamp query parameter to always get the latest content.

## Usage
- Upon load, the app fetches quotes.json and displays a random quote inside the #quote element.
- Click “New quote” to show another random selection from the same dataset.
- Click “Copy” to copy the current quote to your clipboard.

The default expected format of quotes.json is an array of strings, for example:
[
  "This is a random quote.",
  "Share your knowledge.",
  "Create little just for fun."
]

The app also tolerates an array of objects with a text property:
[
  { "text": "This is a random quote." },
  { "text": "Share your knowledge." }
]

## License (MIT)
Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.