# pertpert

This repository contains a small, whimsical tribute page to my cat Rupert — a charming black cat. Rupert is older and a little grumpy, not much into toys, but he absolutely insists on his meals arriving on time. The page uses `boyboy.webp` as a full-page background and includes interactive, lightweight effects.

Rupert's personality details:

- Black cat, retired nap champion
- A little grumpy and mostly solitary
- Not toy-friendly; prefers meals on schedule
- Use the "Feed Rupert" button in the page to record when you last fed him — the value is stored locally in your browser.

How to view

1. Place `boyboy.webp` in the repository root (if not already placed).
2. Open `index.html` in a browser or run a tiny local server:

   ```pwsh
   # Simple way using Python 3 – opens the repo at http://localhost:8000
   python -m http.server 8000
   ```

Performance & optimization tips

- Prefer `boyboy.webp` for modern browsers (already used), but add a `boyboy.jpg` fallback if you need to support legacy systems.
- Keep the image resolution close to the display size you need (e.g., 1920x1080) to avoid unnecessarily large files.
- Compress with tools such as `cwebp`, `imagemin`, or TinyPNG before committing.
- Serve via CDN for production deployments.

Accessibility & performance

- The page uses `prefers-reduced-motion` to respect users who request less animation.
- It's important to include `alt` text for the background image when applicable; an inline `<img>` with the `alt` text is used here.

- The UI includes a simple "Feed Rupert" button that stores the last feeding time in your browser's `localStorage`; this is purely local and intended as a playful way to track a quick schedule.
- Because Rupert is older and darker, we default the play/toy animations off — you can optionally enable them with the button if you like.
- Since Rupert is black, the page includes a subtle overlay to ensure text is readable against his dark fur. If your photo has very low exposure, consider increasing overlay brightness or using a radial spotlight in CSS to highlight the subject.

License & notes

- This sample is intentionally small and playful — adapt it as you like. If you’d like help generating a proper fallback JPG or optimizing the WebP, tell me the maximum resolution you want and I’ll provide commands or a script.
