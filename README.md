# Ball Knowledge

A daily NBA player guessing game. Four players a day, five clues each, five guesses each.

- `index.html` — the whole game (static page, served by GitHub Pages)
- Puzzles live in the `WEEKS` array inside `index.html`; a new week is appended every Sunday.
- Accounts, results, streaks and the leaderboard live in Supabase (project `ball-knowledge`).

## Scoring
- Each day starts at 1000 points.
- Each wrong guess or skip costs 80 / 60 / 40 / 20 on Players 1–4; missing a player costs 5× that.
- Getting all 4 right extends your streak. At a streak of 3+, each perfect day earns +100 (🔥 on the leaderboard).
- Rating (0–10) = your average daily score ÷ 100, before bonuses.
