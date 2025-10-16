# Mini Calculator + Captcha Viewer/Solver

## Overview
This is a small, single-page web app that demonstrates:
- A minimal calculator with a clean UI supporting +, -, *, /, %, parentheses, and keyboard input.
- A captcha viewer that:
  - Displays the captcha image pointed to by the URL provided via the `?url=...` query parameter (or pasted into the input).
  - Attempts to automatically solve the captcha text within 15 seconds using on-device OCR (Tesseract.js) with a cloud OCR fallback.

The project is intentionally self-contained with inline HTML/CSS/JS for easy drop-in use.

License: MIT

## Setup
- No build tools required.
- Open `index.html` directly in a modern browser with internet access (for the OCR library/CDN).
- Optional: Provide a captcha image URL through the query parameter `?url=...` to auto-load and attempt solving.

Example:
- file path: `./index.html?url=https://dummyimage.com/150x60/ffffff/000000.png&text=12345`

Note: The app uses a CORS-friendly proxy for image display and Tesseract-based OCR. It also includes a fallback call to the OCR.Space demo endpoint for improved reliability.

## Usage
- Calculator:
  - Click buttons or type an expression in the input field.
  - Press Enter or click equals (=) to evaluate, or keep typing to see live results.
  - Operators supported: `+`, `-`, `*`, `/`, `%`, and parentheses `()`.
  - Utilities: `C` clears, `⌫` deletes last character.

- Captcha:
  - Auto mode: Open the page with `?url=YOUR_IMAGE_URL` to auto-load and solve.
  - Manual mode: Paste a captcha URL or data URL into the textbox and click “Load”, then click “Solve”.
  - The page shows:
    - The exact captcha URL you provided.
    - The captcha image (via a CORS-friendly proxy).
    - OCR progress and the solved text upon completion or timeout (15 seconds).

Tips:
- Prefer clear, high-contrast images for best OCR accuracy.
- Data URLs are supported. For remote images, make sure they are publicly reachable.

## License (MIT)
Copyright (c) 2025 Mini Calculator + Captcha Viewer/Solver contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.