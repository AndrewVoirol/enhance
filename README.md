![Enhance! — AI-powered infinite zoom](screenshots/initial-state.png)

# Enhance!

The CSI "zoom and enhance" meme, but it actually works. Click any region of an image and Gemini generates high-resolution detail for it. Keep clicking to zoom deeper — each enhancement becomes the canvas for the next.

![Mid-enhancement — pixelated crop being analyzed](screenshots/mid-flight.png)

![Enhanced result with nano banana easter egg](screenshots/enhanced-result.png)

## Quick Start

> Requires Node.js 18+ and a [Gemini API key](https://aistudio.google.com/apikey)

```bash
git clone https://github.com/yourusername/enhance.git
cd enhance
npm install
```

Add your API key to `.env.local`:
```
VITE_GEMINI_API_KEY=your_key_here
```

```bash
npm run dev
```

## How It Works

Click anywhere on the image. The app crops your selection, sends it to Gemini to understand what it's looking at, then asks Gemini to generate a high-res version with invented detail. A pixel-dissolve animation reveals the result, which replaces the current view — so you can keep zooming forever.

Undo/redo your zoom history, regenerate any step, or export the whole journey as an animated GIF.

There's also a hidden nano banana 🍌 easter egg. The AI occasionally sneaks one into enhanced images.

## Tech Stack

| Layer | Tech |
|---|---|
| Framework | React 19 |
| Build | Vite 6 |
| Styling | Tailwind CSS 3 |
| AI | Gemini 2.5 Flash (describe) + Gemini 2.5 Flash Image (enhance) |
| GIF Export | gifenc |
| Language | TypeScript |

## Origin

This is a Google AI Studio starter app ("ENHANCE!") that was exported and cleaned up to run standalone. The original code is licensed under Apache 2.0.

## License

[Apache 2.0](LICENSE)
