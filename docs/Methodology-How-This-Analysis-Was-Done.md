# Methodology: How This Analysis Was Done

> **\*2026 results are unofficial** (Texas Secretary of State election-night file, election 53815, before the state canvass). **Texas has no party registration.** Every "Democratic primary voters" figure on these pages is the stand-in for registration. This is a hypothesis to examine. The math measures a pattern; it does not prove cause.

Back to [Full Reversal Analysis](Full-Reversal-Analysis.md) · [Home](../README.md)

This is exactly how the analysis was done, step by step, so anyone can check it and walk someone else through it.

## The steps

**(a) Democratic primary voters stand in for registration.** Texas has no party registration. So for each county the analyst used the Democratic share of the March 2026 Governor primary: Democratic primary votes ÷ (Democratic + Republican primary votes). It is labeled "Democratic primary voters" on every page, never "registration." Call this number **D**.

**(b) The forward equation.** For each county and each race: Democratic votes ÷ total ballots cast, as a percent. Call it **S**. Then subtract the Democratic primary share: **gap = S − D**. If a county voted exactly the way its primary voters did, the gap would be zero.

**(c) One statewide line through all 254 counties.** Every county's gap was plotted against its Democratic primary share and a straight line was fitted through them, with every county counted once:
**gap = multiplier × (D/100) + offset.**
For the Senate race that line is **gap = −30.0676(D/100) + 14.2008**. For the Governor race it is **gap = −31.6914(D/100) + 13.4457**. The offset is the constant at the end, the Texas counterpart of Kansas's 6.3014.

**(d) Residual: each county's distance above the line.** Take the county's actual gap and subtract what the line predicts for its primary share. Above the line is positive; below the line is negative.

**(e) The full reversal is the residual PLUS the offset.** Not just the residual. The offset is part of the fitted equation, so it is part of what gets removed, county by county, the same way Kansas did it:
**removal (points) = residual + offset.**
A county that comes out negative is set to zero (Kansas zeroed Wyandotte, Douglas, Nemaha and Trego). Points become votes: **removal votes = removal ÷ 100 × ballots cast**, rounded to the nearest whole vote.

**(f) Sum the counties for the statewide total.** The 254 county removals were added for each race.

**(g) Every top-ticket race, run on its own.** U.S. Senate, Governor, Lieutenant Governor, Attorney General, Comptroller, Agriculture Commissioner and Railroad Commissioner. Each race gets its own line, its own offset and its own total. Same voters, so the races are never added together.

**(h) Double verification.** Two separate programs re-read the raw Texas Secretary of State files for all 254 counties: one in pandas, one in plain Python with exact fractions that finds each race by name. Every cell had to match, and each race also had to match the Secretary of State's own statewide totals and percentages. **62,545 checks, 0 mismatches.** Nothing shipped before that.

**(i) 2026 is unofficial.** These are election-night numbers. County canvasses can still change them, and every page and graphic says so.

## How the votes are moved

With the injection removed, the removal comes **off the Democrat and goes to the Republican** in each county. The race total stays the same. That is how "who wins with the injection removed" is calculated. The Full Reversal page also shows the removed-only version, where the votes are taken away and not given to anyone: the Republican still wins all seven races.

## Worked example: Harris County, U.S. Senate

| Step | Number |
|---|---|
| Democratic primary voters (D) | 351,218 ÷ (351,218 + 191,225) = **64.75%** |
| Talarico share of ballots (S) | 907,617 ÷ 1,383,480 = **65.60%** |
| Gap (S − D) | **+0.86 pts** |
| Line predicts | −30.0676 × 0.6475 + 14.2008 = **−5.27 pts** |
| Residual (gap − line) | **+6.12 pts** |
| Plus the offset | 6.12 + 14.20 = **20.32 pts** |
| Removal votes | 20.3244% × 1,383,480 = **281,185** |
| With the injection removed | Talarico 907,617 → 626,432; Paxton 451,780 → 732,965 |

Harris flips to Paxton. Do that for all 254 counties and add them up, and the Senate total is **1,889,815** votes.

## What to say if someone challenges it

- **Most of the removal is the offset:** 67–76%, depending on the race. That is the Kansas structure, and the [Full Reversal page](Full-Reversal-Analysis.md#where-the-offset-fits-in) shows both parts for every race.
- **The line counts every county once.** The many small rural counties shape it, and the big metros sit above it.
- **Bad election-night data is flagged rather than hidden:** Duval, Starr, Zapata and the down-ballot over-counts are all on the [data-quality list](Full-Reversal-Analysis.md#data-quality-flags).

*2026 figures are unofficial. Source: Texas Secretary of State; U.S. Census Bureau Vintage 2025 population estimates.*

