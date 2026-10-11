# Arcade Legends

A browser arcade with 7 games you can play right now (Star Catcher, Snake Classic, Memory Match, Pong Duel, Tank Battle, Zombie Escape, Tetris Blocks), plus a catalog of upcoming titles, credits, an avatar shop and badges.

## Technologies

- One static `index.html` file containing plain HTML, CSS and vanilla JavaScript (games are drawn on a `<canvas>`)
- Accounts and progress are stored in the browser's `localStorage`
- Hosted on Netlify as a static site (`netlify.toml` publishes the repo root)

## Running locally

Open `index.html` in a browser, or run:

```
netlify dev
```

## Roadmap

Ideas for later: real accounts and saved progress that work across devices (Netlify Identity + Netlify Database), and more playable games.
