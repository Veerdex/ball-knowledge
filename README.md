# Ball Knowledge

A daily NBA player guessing game. Four players a day, five clues each, five guesses each.

- `index.html` — the whole game (static page, served by GitHub Pages)
- Two sports (basketball `nba`, football `nfl`), 4 players each per day. Puzzles, guess lists, guesses, results, streaks and per-sport leaderboards live in Supabase (project `ball-knowledge`, tables `bk_*`).
- The page never receives answers: clues are revealed and guesses are checked by database functions (`bk_get_day`, `bk_make_guess`, `bk_week_status`).
- New weeks are added to the `bk_puzzles` and `bk_names` tables for both sports every Sunday; this file doesn't change.

## Scoring
- Each day starts at 1000 points.
- Each wrong guess or skip costs 80 / 60 / 40 / 20 on Players 1–4; missing a player costs 5× that.
- Getting all 4 right extends your streak. At a streak of 3+, each perfect day earns +100 (🔥 on the leaderboard).
- Rating (0–10) = your average daily score ÷ 100, before bonuses.
