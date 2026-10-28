# Start.ng Pocket Gameling

A whimsical take on the [Start.ng](https://start.ng) landing page, built for the HNG 15 individual task.

The page itself stays plain: start.ng's cream-and-lime look with simple game cards. The whimsy is in what you can do on it.

## What's in it

- **Pocket Gameling.** A small creature lives on the page and follows your cursor on a spring, so it trails and overshoots a little.
  - Hover a card and it hops over to read the title.
  - Hover Play and it gets excited.
  - Scroll fast and it gets dizzy.
  - Leave the page alone for 10 seconds and it falls asleep. Move the mouse and it wakes.
  - Click it and it says a line. Drag it onto a card and it re-grows as that game's creature.
- **Physical cards.** Pick up any game card and throw it. Cards fall, bounce and collide, and a hard hit knocks neighbouring cards loose. "Tidy up the cards" (or 15 quiet seconds) springs them back to their slots. On touch screens, long-press a card to pick it up so normal scrolling still works.
- **Creatures from titles.** Each creature is drawn by a small generator that seeds a random number generator from the game's title, so the same title always grows the same creature. It works for any game name, including ones that don't exist yet.

## Run it

It is a single static file with no build step.

```bash
python3 -m http.server 8765   # then open http://localhost:8765
```

## Deploy

Import the repo on Vercel with the framework preset **Other** and no build command. Every push to `main` redeploys.

## Notes

- Plain HTML, CSS and JavaScript. [GSAP](https://gsap.com) drives the creature and the tidy-up animation. [Matter.js](https://brm.io/matter-js/) is fetched once the page is idle and runs the card physics. Both load from cdnjs.
- With `prefers-reduced-motion`, or if GSAP fails to load, the creature just sits in its corner and the cards stay put. The Play links are ordinary links either way.
- Game titles, creators, publish steps and the tournament text come from start.ng. Everything else is original to this design.
- The creature is decorative and hidden from assistive technology.
