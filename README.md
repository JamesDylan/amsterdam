# Amsterdam

Investment-theme deck for the Serko B4B Amsterdam Q3 2026 face-to-face with Booking.com.

**Live site:** auto-deployed by Vercel on push to `main`.

## Structure

```
amsterdam/
├── index.html                              # Landing page
├── vercel.json                             # URL rewrites for clean paths
├── activate_themes_plan_simplified.html    # /activate
├── company_themes_plan_simplified.html     # /company
└── README.md
```

## Adding a new section

1. Drop the new HTML file into the repo root (e.g. `travel_arranger_plan.html`).
2. Add a rewrite in `vercel.json`:
   ```json
   { "source": "/travel-arranger", "destination": "/travel_arranger_plan.html" }
   ```
3. In `index.html`, find the matching draft card and:
   - Change `class="card draft cN"` to `class="card live cN"`
   - Change `<a class="card live cN" href="/...">` (wrap the div in an anchor)
   - Update the status pill from `status draft` to `status live`
   - Replace the `—` arrow with `Open →`
4. Commit and push. Vercel will redeploy in ~30 seconds.

## Sections in scope

| # | Section              | Slide ref     | Status   |
|---|----------------------|---------------|----------|
| 1 | Acquisition & Activation | Slides 4–9    | ✅ Live   |
| 2 | Company Management   | Slides 10–14  | ✅ Live   |
| 3 | Travel Arranger      | Slides 15+    | ✅ Live    |
| 4 | Growth Loops   | n/a      | ✅ Live    |
| 5 | Supply & Foundations | Slide 17      | Draft    |
| 6 | Payment Parity       | Slide 18      | Draft    |
| 7 | Tech Modernisation   | Slides 20–22  | Draft    |

## Design language

All section pages use the same stack:
- Outfit (display) + Inter (body) + DM Mono (mono) + Fraunces (editorial italic)
- Off-white canvas (`#F7F5F2`), dark sidebar (`#1A1625`)
- Four-colour accent palette per section: teal / purple / pink / amber
- The landing page extends the palette with blue / green / violet for future sections

Keep the format consistent across sections so a reader can navigate any one of them the same way.

## Deploying

Pushes to `main` auto-deploy via Vercel.

Manual deploy:
```bash
npx vercel --prod
```

Vercel project ID: `prj_aAOyT3gDCHIOovnV5hfUEbDFcXoM`
