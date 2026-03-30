# WHAT'S NEXT

A minimalist color memory game built as a single HTML file — no frameworks, no build tools, no dependencies.

## How to Play

Each of the 3 rounds follows two phases:

1. **Memorize** — A random color fills the screen for 3 seconds. Study it.
2. **Tune** — The color disappears. You have 15 seconds to recreate it using Hue, Saturation, and Lightness sliders.

Your score for each round (0.00–10.00) is calculated from the RGB Euclidean distance between the target color and your guess. The closer you get, the higher you score.

## Live Demo

Play it here: **https://YOUR_USERNAME.github.io/whats-next/**

## Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `whats-next`)
2. Push this project:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/whats-next.git
git push -u origin main
```

3. Go to **Settings → Pages** in your repository
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch, root `/`, then click **Save**
6. Your game will be live at `https://YOUR_USERNAME.github.io/whats-next/` within a minute

## Tech Stack

- Vanilla HTML / CSS / JavaScript
- [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) typeface (via Google Fonts CDN)
- Zero build steps — open `index.html` in any browser

## Scoring Algorithm

```
RGB distance = sqrt((r1-r2)^2 + (g1-g2)^2 + (b1-b2)^2)
Score = max(0, 10 - distance / 44.167)
```

Max possible distance (~441.67) maps to 0.00. A perfect match scores 10.00.

## License

MIT
