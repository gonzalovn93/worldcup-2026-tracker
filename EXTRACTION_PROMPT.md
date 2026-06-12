# How to fill the tracker

You have 4 pools open in Chrome. For EACH tab, run the prompt below in
**Claude for Chrome**, then paste the JSON it returns into `data.js`
(under that pool's `predictions` and `specialAwards`).

Do them one tab at a time — it keeps the output clean.

---

## Paste this into Claude for Chrome (on each pool tab):

> Read my World Cup prediction picks on this page. Output ONLY a JSON object,
> no prose, in exactly this shape:
>
> ```json
> {
>   "predictions": [
>     { "matchKey": "MEX-KOR", "stage": "Group A", "home": "Mexico", "away": "Korea", "pick": "2-1" }
>   ],
>   "specialAwards": [
>     { "award": "Champion", "pick": "Argentina" },
>     { "award": "Top Scorer", "pick": "Mbappé" }
>   ]
> }
> ```
>
> Rules:
> - `matchKey` = the two teams as 3-letter codes joined by a hyphen, home first
>   (e.g. "MEX-KOR"). Use the SAME codes every time so the same game lines up.
> - `pick` = my predicted score (e.g. "2-1") or my predicted winner if the pool
>   only asks for a winner.
> - Include every game I've made a pick for. Skip games I left blank.
> - Put bracket/tournament-wide picks (champion, finalist, top scorer, best
>   player, etc.) in `specialAwards`.
> - Output the raw JSON only.

---

## Then:
1. Open `data.js`.
2. Find the matching pool block (lasmigas / haas / pollaya / golpredictor).
3. Replace its `predictions: []` and `specialAwards: []` with what Claude gave you.
4. Save, open `index.html`, refresh.

The **"All games (combined)"** tab lines all four pools up side-by-side per game,
so you can see at a glance what you played everywhere. Each pool also has its
own tab.

> Tip: if you'd rather not edit the file yourself, just paste all four JSON blobs
> back into your Claude chat and ask it to drop them into `data.js`.
