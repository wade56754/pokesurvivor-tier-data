# PokéSurvivor Tier Data

Open data behind **[pokesurvivortierlist.com](https://pokesurvivortierlist.com/)**: our provisional tier list for the 29 starter partners in PokéSurvivor, plus the community's picks for the strongest gacha Pokémon.

- Interactive tier list: <https://pokesurvivortierlist.com/>
- Best Pokémon (community picks): <https://pokesurvivortierlist.com/best-pokemon/>

> **Unofficial fan project.** Not affiliated with or endorsed by Nintendo, Game Freak, The Pokémon Company, or the PokéSurvivor developer (JPTER78). Pokémon and all related names are trademarks of their respective owners. Play the official game at [pokesurvivor.com](https://pokesurvivor.com).

## Files

| File | What it contains |
|---|---|
| [`data/starter-tiers.json`](data/starter-tiers.json) | The 29 starters in tiers S–D, with position within the tier, confidence (`low` / `medium`) and a one-line reason in our own words |
| [`data/best-pokemon.json`](data/best-pokemon.json) | Community picks (Mewtwo, Gengar, Lucario, Tentacruel) plus notes (e.g. Arceus as a partner), each with a mention count, consensus strength, our summary, counterpoints and source links |
| [`METHODOLOGY.md`](METHODOLOGY.md) | How the tiers and picks were put together, and their limits |

Both files carry `updatedAt` / `asOf` and the game version (code commit) they refer to.

## Status

**Provisional.** The starter tiers combine two stat-based models with a few player reports. They are **not a community consensus**, confidence is low, and starter differences are small — real power comes from gacha Pokémon. We review the data weekly as the game updates; see the website for the current version.

## What is *not* here

- No game sprites, artwork, logos, audio or other game assets.
- No game code and no copies of the game's data files. Game stats (hp, spd, atk, base stat total, star rating) are deliberately **not** included; they come from the game itself — see the official [PokéSurvivor repository](https://github.com/JPTER78/pokesurvivor) and its license.
- No website source code.

## License

The data and documentation in this repository — our tier assignments, confidence ratings, summaries and notes — are licensed under **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)**. See [`LICENSE`](LICENSE).

Attribution: “PokéSurvivor Tier Data by pokesurvivortierlist.com (https://pokesurvivortierlist.com/), CC BY 4.0”.

The license covers only our own work. Pokémon names are trademarks of their owners, and linked third-party sources (videos, posts) remain their authors' property.
