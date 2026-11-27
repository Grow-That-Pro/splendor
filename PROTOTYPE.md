# Splendor — UI prototype (throwaway)

This branch holds a throwaway prototype. It is not production code and should never be merged into `main`.

## The question

What should receiving beauty on Splendor feel like?

## The design: Chapel, evolved

Lincoln picked Chapel from round 1. The three round-1 variants (Gallery, Chapel, Book) are in commit `33abfc8` on this branch if you want them back.

- **Home** shows Today's Moment, taken from the newest Pack (each Pack has an `added` date): its Image softly visible, the Pack name, and one Begin button. "How long do you have?" is a light choice (just play, five, ten or fifteen minutes). "All Packs" opens the Library, a calm wall of Covers: one painting per Pack with its name and curator. "Best with sound on" has a small speaker button that plays a few seconds of today's Sound.
- **Reveal**: the Image is dimmed and drifts slowly, and the Passage appears line by line in large serif, centred.
- **Rest**: about two seconds per line after the last line appears (at least four seconds), the Passage and its Credits move in one continuous motion into a small block in the bottom-left corner, and the Image comes up to full brightness with no dark overlay. Only a soft local shadow sits behind the corner text, darker or lighter depending on how bright that corner of the painting is. The Image keeps drifting.
- **Sound player** in the bottom-right corner: title and credit, play or pause, next, mute, a thin progress line with elapsed and remaining time, and small level bars while it plays. A Moment with no Sound says "Silence".
- **Just play carries on**: when a Pack runs out, the Session moves into the unplayed Pack that shares the most `tags` (Advent, then Saints, then Builders). The new Pack's name appears softly for a few seconds as its first Moment begins. When every Pack has played, the Closing follows.
- **A Moment with no Image** uses the candlelit Backdrop and keeps the Passage centred.
- **Closing**: the last seconds fade to dark, the Sound fades out, a soft chime plays, and a quiet "Return" takes you home.

## Sound

Each Moment's Sound is `{ title, credit, youtube, spotify? }`, and the page plays it through YouTube. The YouTube player is created hidden when the page loads, so the Begin tap can start it straight away. If a browser still refuses (strict autoplay settings, likely iPhone Safari), the small video appears in the corner with "This browser needs one tap on the video to play its Sound".

## Testing tricks

- Add `?fast=1` to make every Moment short, so you can reach the ending quickly.
- The yellow "PROTOTYPE" pill marks it as a prototype.

## Run it

GitHub Pages serves this branch at https://grow-that-pro.github.io/splendor/. Locally, run `python3 -m http.server` in this folder and open http://localhost:8000/.

All data lives in the `PACKS` constant at the top of `index.html`.
