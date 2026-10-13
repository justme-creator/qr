# QR games

Tiny games that live entirely inside QR codes. Scan a code and the game runs in your browser. Nothing is downloaded or installed.

## How it works

Each QR code holds a normal web link to this site. The part after the `#` is the whole game, compressed. Browsers never send that part to a server, so the game really travels inside the QR code.

`index.html` unpacks the game and checks its fingerprint against `games.txt`. Only listed games are opened, and they run in a sealed box with no network access.

Opening this site without a game shows all QR codes. Each game also has its own page, for example `?snake`.

## Files

- `index.html`: the loader and the QR gallery. You never need to edit it.
- `games.txt`: the approved games, one per line: fingerprint, then name.
- `maker.html`: turns a game into a QR code and shows its line for `games.txt`.
- `*-qr.png`: the QR images shown in the gallery, named after each game.

## Adding a game

1. Open `maker.html`, pick or paste a game, and give it a name.
2. Click **Copy line** and add that line to `games.txt`.
3. Download the QR image and upload it here.

## Making your own

Copy this repository, turn on GitHub Pages, and replace `games.txt` and the QR images with your own.
