# UpscaleMyRender

AI enhancer for architectural renders. Upload a basic interior or exterior render and get a
photorealistic, portfolio-quality version in the look of Corona Renderer or V-Ray, while the
architecture stays exactly as designed.

**Live page:** https://haralamposmoutidis-source.github.io/UpscaleMyRender/

![UpscaleMyRender: before and after](docs/screenshot.png)

## How it works
1. **Upload** a render (JPG or PNG, up to 20 MB).
2. **Choose** interior or exterior: each has its own enhancement instructions.
3. **AI enhancement:** the render is analysed (OpenAI GPT-4o), an enhancement prompt is written for
   it, and the new image is generated (DALL·E 3). The rules: never change walls, openings, furniture or
   proportions; improve only materials, lighting, textures, reflections and colour grading.
4. **Preview** with a watermark; pay €0.20 per render (Stripe) to download it in full resolution.

## Setup
The page is a single HTML file. To run the AI step, set the keys in the `CONFIG` block of `index.html`:
- `OPENAI_API_KEY` (platform.openai.com)
- `STRIPE_PUBLISHABLE_KEY` and the Stripe Payment Link (dashboard.stripe.com); without them the
  download is free (demo mode).

> **Before going live:** an OpenAI key placed in a public web page can be read by anyone who opens it.
> Move the OpenAI calls to a small server (for example a serverless function) that keeps the key secret.

## Tech
HTML, CSS and JavaScript in one file; OpenAI API; Stripe Payment Links; hosted on GitHub Pages.

---
© 2026 Haralampos Moutidis. All rights reserved.
