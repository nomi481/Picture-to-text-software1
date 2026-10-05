# Image to Text

A single-page web app that extracts text from **handwritten + printed pictures**, **PDF**, **Word (.docx)**, **PowerPoint (.pptx)**, **Excel/CSV** and **text files**. Text appears on the right side; you can edit, copy, download as `.txt`, or translate it.

- Pictures and scanned PDF pages are read by Claude AI (handles pen handwriting; Urdu, Pashto, Arabic, Hindi, English and more).
- PDF text, Word, PowerPoint, Excel and text files are read directly in your browser (no AI key needed).

## Deploy on GitHub Pages
1. Create a new GitHub repository and upload `index.html`, `README.md` and `.nojekyll` (drag & drop works).
2. Go to **Settings → Pages**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`, then **Save**.
3. Open `https://<your-username>.github.io/<repo-name>/`.

## Reading engines (pictures and scanned PDF pages)
Choose one in the **Reading engine** box:
1. **Free offline OCR (default)** – runs in your browser, no key, no limit, nothing uploaded. Good for **printed** text (English, Urdu, Arabic, Pashto, Hindi, Persian); weak on pen handwriting.
2. **Gemini AI (free key)** – reads handwriting. Get a free key at https://aistudio.google.com/apikey. It has daily/per-minute limits, and on the free tier Google may use the data to improve its models, so avoid private student data.
3. **Claude AI (paid key)** – best handwriting. Key from https://console.anthropic.com (needs credit).

Keys are kept only in your browser's localStorage. **Never commit a key into the code.** Anyone using your public site enters their own key.

PDF text, Word, PowerPoint, Excel and text files never need a key.

## Notes
- Limits: 6 files at once, 40 PDF pages, 10 scanned PDF pages sent to AI per file.
- Old `.doc` files are not supported — save as `.docx` or PDF.
- PDF/Word/PowerPoint/Excel readers load from cdnjs.cloudflare.com; the free OCR loads from cdn.jsdelivr.net and downloads language data on first use, so an internet connection is needed.
