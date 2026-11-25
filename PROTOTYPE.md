# Splendor — UI prototype (throwaway)

This branch holds a throwaway prototype. It is not production code and should never be merged into `main`.

## The question

What should receiving beauty on Splendor feel like?

## The three variants

All three run the whole flow: home, choosing a Pack and a Session length, the Moment screen, moving between Moments, and the Session ending (fade to dark, a soft chime, one line to carry with you).

- **A · Gallery** — a museum. The painting fills the screen, the Passage sits on a placard in the corner, Credits are small and exact. Home is a quiet wall of Pack covers. A Moment with no Image becomes wall text.
- **B · Chapel** — candlelit and dark. The Image is dimmed and drifts slowly, the Passage is revealed line by line in large serif. Entering asks "How long do you have?" and then "Enter".
- **C · Book** — an illuminated book. The Image is a framed plate, the Passage is set like a printed page with a drop cap, and Moments turn like pages. Packs are a table of contents.

## How to switch

- Add `?variant=A`, `?variant=B` or `?variant=C` to the URL.
- Or use the black bar at the bottom centre: the arrows, or the left and right arrow keys.
- Add `&fast=1` to make every Moment 15 seconds and Sessions short, for testing the ending.

## Run it

Open `index.html` through any web server (GitHub Pages serves it from this branch), for example `python3 -m http.server` and visit http://localhost:8000/?variant=B. Sound comes from YouTube, so it needs a connection and one tap to start.

All data lives in the `PACKS` constant at the top of `index.html`.
