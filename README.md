# 🤥 Fib Finder!

A family bluffing game for 3–12 players in the same room, one phone each. Everyone sees a weird-but-true fact with a word missing, makes up a fake answer, then tries to spot the real one among everyone's fibs.

**Play:** https://atlashome88ai.github.io/fibfinder/ (also on the Atlas **🎮 Games** page). The full guide is in the game: tap **📖 How to play**.

## Set up
1. One person taps **Host the game**, types their name and taps **Create game** (the host plays too).
2. Everyone else scans the QR code (or taps **Join as a player** and types the 4-letter code), types their name and taps **Join**.
3. The host picks a category (or 🎲 Mix it up) and taps **Start game**.

## Each question
1. Read the fact, type a believable **fake answer**, tap **Send my fib**. (Type the real answer by accident and the game asks for another.)
2. When all fibs are in, every phone shows all the answers mixed with the real one. Tap the one you think is **true** (your own fib isn't shown to you).
3. The reveal shows the truth, who wrote each fib and who fell for it.
4. Host taps **Next question**, or **Finish game** for the winner.

## Points
- **+2** for picking the real answer.
- **+1** for every player your fib fools.

## Adding questions
Questions live in `_shared/fibfinder/game.js` (`CATS`) on the Atlas laptop: `["Fact with a ___.", "answer|other accepted spelling"]`. Run `python3 ~/games-src/_shared/build.py`, then push.

## How it works
One `index.html`, no server of its own: the host's phone runs the game and other phones connect to it with PeerJS (WebRTC). Same engine as Imposter!, built from `~/games-src/_shared` on the Atlas laptop. Hosted on GitHub Pages.
