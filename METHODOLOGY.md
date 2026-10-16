# Methodology

Data as of **2026-10-16**, game version **c31715d** (PokéSurvivor code commit of 2026-10-14). Everything below is written in our own words; no text from the sources is copied.

## 1. Starter tiers (`data/starter-tiers.json`)

**Status: provisional, stat-based, low confidence. Not a community consensus.**

### Why stat-based?
At launch, players barely discussed which starter is strongest. The talk is about Pokémon pulled from the gacha. Only three starters (Froakie, Sprigatito, Mudkip) had any real player reports, each a single personal experience. So the ranking has to lean on stat models for now.

### Inputs
1. **A guide site's weighted score** for the 29 starters: base stat total 40 %, attack 20 %, speed 20 %, starting-move damage per second 20 %. The site states it has not tested this in game.
2. **A community-made "mega tier list" chart** of all 966 Pokémon (dated 2026-10-13, game build a9b21f0), which its author describes as their own estimate combining kill power at minute 15, survivability at minute 15, and speed. It was referenced in an Italian creator's [tier-list video](https://www.youtube.com/watch?v=M5biNLZgsgc).
3. **Scattered player reports** from public posts on X (listed in `best-pokemon.json` and on the website), used only as supporting notes, never to move a tier on their own.
4. **Game facts** from the official [guide](https://pokesurvivor.com/en/guide/), [news](https://pokesurvivor.com/en/news/) and the game's public [repository](https://github.com/JPTER78/pokesurvivor) (starting moves, balance changes).

### Method
- For each starter, take its rank in model 1 and its position among the 29 starters in model 2, and average them.
- Sort by that average and cut: **S = 1–4, A = 5–11, B = 12–19, C = 20–25, D = 26–29**.
- Confidence is `medium` when both models agree closely (Litten, Scorbunny, Sobble, Fennekin, Snivy); otherwise `low`.
- Charmander is placed in D but flagged `beginnerFriendly`: a guide site recommends it to new players because it is easy to use, not because it is strong.

### Where the models disagree
Model 1 rewards starting-move damage; model 2 rewards survivability (HP) at minute 15. That is why Popplio (high in model 1, low in model 2), Tepig and Fuecoco (the reverse) and Oshawott land in the middle tiers.

### Limits
- Starter gaps are small: base stat totals span only 307–320 and attack 0.95–1.09.
- Not modelled: move upgrades and evolutions, held items, Bonds, co-op, player skill.
- Version-sensitive: the game updates almost daily (e.g. Psychic moves were weakened on 2026-10-11). Any ranking should be read together with its date and game version.
- At the C/D boundary Squirtle, Treecko and Charmander have the same average; the research we relied on places Charmander in D.

## 2. Best Pokémon — community picks (`data/best-pokemon.json`)

- Sources: public YouTube videos (titles, descriptions and, where available, auto-generated subtitles) and public posts on X, plus the official changelog. Each entry lists its sources with links and dates.
- `mentions` counts distinct sources singling the Pokémon out; `consensus` is `strong` (many independent mentions), `moderate` (2–3) or `single source`.
- Counterpoints from stat models are kept next to the praise (e.g. one stat chart places Mewtwo only in its A tier).
- Not yet covered: Reddit and Discord. Treat this as a snapshot, not an official ranking.

## 3. Updating

We review weekly. When the ranking changes, `updatedAt`/`asOf` and `gameVersion` change with it. The website always shows the current version: <https://pokesurvivortierlist.com/>.
