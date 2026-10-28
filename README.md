# Client Policy Review

A one-page web app for insurance agents. Upload one client's policy detail PDFs or screenshots and get a clear policy summary:

- Client details and an at-a-glance view (policies, premium payable, fund value)
- Policy overview and coverage by benefit across all policies
- Investment funds, nomination and ownership
- Points to discuss with the client
- Advisor notes (internal) — things to verify, kept out of the client copy

Figures are copied exactly from the records; benefits are never guessed from plan names.

## How to use

1. Open the app link.
2. Under **Setup**, paste your Anthropic API key (create one at console.anthropic.com → API keys). It is saved only in your browser on that device and sent only to Anthropic.
3. Upload the client's policy detail PDFs or screenshots.
4. Press **Write policy summary**, then download the client copy or the version with advisor notes.

## Privacy

- Files are read in your browser. Nothing is stored on GitHub or any server.
- PDF text is sent to Anthropic only when you press the button. IC, email, phone and card numbers are masked first (on by default). Screenshots and scanned PDFs are sent as they are.
- Each user's API key stays in their own browser. Set a monthly spend limit in the Anthropic console, and don't save the key on shared computers.

## Technical notes

Single static `index.html` (no build step). Uses the official Anthropic TypeScript SDK in the browser (model `claude-opus-5-5`), pdf.js for reading PDFs, marked + DOMPurify for rendering.
