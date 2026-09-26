# Sock Hop Smackdown: live wrestling bracket

It's one file, `index.html`. On everyone's phone the Live page shows, from top to bottom:
**who's on the mat now → up next → the whole bracket → the ink board.**
Only the ref (you) can change anything.

## One-time setup
1. In `index.html`, change the three lines at the top of the `<script>`:
   `ROOM` (make it random), `HOST_PIN`, and `DEFAULT_PRIZE`.
2. Upload it to a GitHub repo and turn on Settings → Pages → Deploy from branch → `main`.
3. Share the link: `https://demi-qas.github.io/<repo>/`

## Running the bracket (from your phone)
Tap **ref login** in the footer, enter your PIN, then open the **🦓 Builder** tab.

**1 · Event**: set the name and the prize.

**2 · Wrestlers**: paste your list, one name per line. You can also pair people as you paste:
```
Demi vs Bex
Juno, Rory
Sal
Kit
```
Lines with two names become Round 1 matchups right away. Single names go into the unpaired pool.
If you'd rather use a Google Sheet, put names in column A and optional opponents in column B,
then Share → Anyone with the link → Viewer, paste the link, and tap Import.

**3 · Matchups**
- Tap one name, then another, and they're paired. With an odd number, tap a name and choose **Give a bye**.
- **Pair the rest in order** pairs up whoever's left, top to bottom.
- Use ↑ ↓ to set the match order (the top match goes first). ✕ removes a matchup.
- 🤼 🧦 ✍️ set the rules ahead of time. This is optional; you can also pick them at the mat.
- **+ Round** adds the next round. Its pool shows only people who won the previous round.
  Rename rounds whatever you like ("Semis", "Grudge Match"). If you need a rematch or a losers' round, tick "Show everyone".

**The round that's running right now**: use the dropdown on the Live tab ("Round running right now"),
or the "Make this the round running now" button in the Builder. Up next only lists matches
from that round onward.

## At the mat (Live tab, ref controls)
1. Pick the rules: Classic / Sock Off / Your Rules. For Your Rules, type what the two wrestlers agreed on,
   and it shows up on everyone's phone as you type.
2. Start the clock (it's visible to everyone).
3. Tap the winner. The loser gets a 🖊️ on the ink board, and the next match moves up automatically.
4. When a round is done, tap **Build the next round →** and pair the winners.

If you make a mistake: **Undo last change** (up to 25 steps back), or **clear result** on a match in the Builder.
To look around without going live: add `?demo`, `?demo=ref`, or `?demo=builder` to the URL.

## Honest limits
- Live sync runs through the free public service ntfy.sh. Anyone who reads the page source can see the ROOM name and PIN,
  which is fine for a party. Don't put private info in it.
- Keep the ref phone open. It re-sends the bracket every 20 minutes so people who show up late still get the current state.
- Only one ref phone at a time. Two refs editing at once will overwrite each other.
