# Start.ng Lagos Street

A whimsical redesign of the [Start.ng](https://start.ng) landing page, built for the HNG 15 individual task.

Start.ng is a free browser-game platform for the HNG community. This version turns the home page into a Lagos street.

## What's in it

- **Hero street scene.** A flat illustrated skyline and a yellow danfo that drives in once on load.
- **Games as market stalls.** Each game gets a striped awning and a hand-painted-style sign. The Hangout is the glowing stall at the end of the street.
- **Bus-stop steps.** The four steps for publishing a game are shown as numbered bus-stop plates.
- **Evening tournament band.** String lights and a live Lagos clock, with the daily tournament description.
- **Day and night.** A theme toggle switches between a day street and a night market. The page follows the system theme by default.

## Run it

It is a single static file with no build step.

```bash
open index.html
```

## Deploy

Import the repo on Vercel with the framework preset **Other** and no build command. Every push to `main` redeploys.

## Notes

- Game titles, creators, publish steps and the tournament text come from start.ng. Everything else, including the illustrations, is original to this design.
- Plain HTML, CSS and JavaScript. Characters and scenery are hand-written inline SVG, and all motion is CSS keyframes. It respects `prefers-reduced-motion`.
- The painted-sign lettering uses the Bowlby One font from Google Fonts.
