# Texas 2026* full Kansas-style reversal, seven statewide races — DRAFT, PRIVATE, NOT PUBLISHED

> \*2026 results are **unofficial** (SOS election-night file countyInfo_53815.json, enr/53815/117, last updated Nov 4 2026 22:48 CT, pre-canvass). The floor is the **Democratic share of March 2026 primary voters**, Dem ÷ (Dem + Rep) governor-primary totals (SOS 53814/53813). Texas has no party registration, so this is a stand-in for it. Tables are sorted by population, largest first (Census V2025). **Treating these removals as injected votes is the analyst's hypothesis. The arithmetic cannot test cause, and the results are not proof of fraud.**

## Method (the same structure as Kansas)

For each race, across all 254 counties:

1. S = Dem votes ÷ ballots cast × 100. D = Dem primary-voter share × 100. Gap G = S − D.
2. **Texas locked line for the race** (surplus form, fit by least squares on 254 counties): G = m·(D/100) + b. **b is the offset**, the Texas analog of Kansas's 6.3014.
3. Residual = G − (m·D/100 + b). **Removal (pts) = residual + b**, the full per-county removal and not the residual alone. Negative values are set to 0, as Kansas zeroed Wyandotte, Douglas, Nemaha and Trego.
4. Removal votes = removal pts ÷ 100 × ballots, rounded half away from zero per county (the Kansas rounding).
5. **Convention: the votes are moved.** Dem − removal and Rep + removal, so the race total is unchanged. Kansas's 'reassign' mode. A remove-only alternative (Dem − removal, total shrinks) is shown too.
6. Offset portion = b × ballots ÷ 100 summed over the counties that were not zeroed. County-gap portion = residual × ballots ÷ 100 over the same counties. The two add up to the total exactly (before per-county rounding).

Algebraically, removal = S − D·(1 + m/100). With m ≈ −30 to −37, every county loses roughly S − 0.65D to S − 0.70D. **A county sitting exactly on the Texas line still loses b points (about 12–14).**

## Statewide results

| Race (SOS ID) | Dem / Rep (SOS %) | Texas line m, b (R²) | Votes removed | Offset share | After: Dem % / Rep % | Margin before → after | Dem point shift | Counties won D: before → after |
|---|---|---|---|---|---|---|---|---|
| U.S. Senate (5075) | Talarico 55.06% / Paxton 42.97% | -30.0676, **14.2008** (0.587) | **1,889,815** | 74.3% | 35.95% / 62.08% | D +12.09 → R +26.13 | −19.11 | 40 → 19 |
| Governor (3579) | Hinojosa 52.80% / Abbott 45.67% | -31.6914, **13.4457** (0.629) | **1,758,291** | 75.6% | 35.05% / 63.42% | D +7.13 → R +28.37 | −17.75 | 37 → 16 |
| Lieutenant Governor (4714) | Goodwin 51.73% / Patrick 45.63% | -37.2059, **12.8342** (0.670) | **1,891,743** | 67.0% | 32.48% / 64.88% | D +6.09 → R +32.40 | −19.25 | 36 → 15 |
| Attorney General (3) | Johnson 52.38% / Middleton 45.94% | -31.9242, **12.0462** (0.565) | **1,673,652** | 71.0% | 35.30% / 63.01% | D +6.44 → R +27.71 | −17.08 | 36 → 17 |
| Comptroller (21) | Eckhardt 51.30% / Huffines 46.15% | -34.2188, **11.9287** (0.611) | **1,671,119** | 70.4% | 34.20% / 63.25% | D +5.15 → R +29.04 | −17.10 | 34 → 16 |
| Agriculture Commissioner (19) | Tucker 51.31% / Sheets 46.65% | -33.7397, **12.2224** (0.606) | **1,624,022** | 74.3% | 34.61% / 63.34% | D +4.66 → R +28.73 | −16.69 | 35 → 17 |
| Railroad Commissioner (4843) | Rosenthal 52.52% / French 45.55% | -33.1158, **12.1329** (0.588) | **1,703,699** | 70.3% | 34.98% / 63.08% | D +6.97 → R +28.10 | −17.53 | 36 → 17 |

**All seven races flip from D to R under the full reversal.** No race stays Democratic statewide.

| Race | Dem votes → after | Rep votes → after | Dem share of ballots → after | Remove-only alternative (Dem % / Rep %) | Offset portion | County-gap portion (net; + / −) | Zeroed counties |
|---|---|---|---|---|---|---|---|
| U.S. Senate | 5,444,982 → 3,555,167 | 4,249,373 → 6,139,188 | 55.06% → 35.95% | 44.44% / 53.12% (R wins) | 1,403,676 | 486,136 (+509,762 / -23,626) | Reeves, La Salle, Kenedy, Loving |
| Governor | 5,230,789 → 3,472,498 | 4,524,527 → 6,282,818 | 52.89% → 35.11% | 42.61% / 55.52% (R wins) | 1,329,047 | 429,246 (+455,267 / -26,020) | Reeves, La Salle, Kenedy, Loving |
| Lieutenant Governor | 5,083,581 → 3,191,838 | 4,484,652 → 6,376,395 | 51.40% → 32.27% | 40.22% / 56.51% (R wins) | 1,268,178 | 623,566 (+646,360 / -22,794) | Zapata, Reeves, La Salle, Kenedy, Loving |
| Attorney General | 5,133,629 → 3,459,977 | 4,502,442 → 6,176,094 | 51.91% → 34.99% | 42.57% / 55.39% (R wins) | 1,188,738 | 484,917 (+507,045 / -22,128) | Starr, Zapata, Reeves, La Salle, Kenedy, Loving |
| Comptroller | 5,014,496 → 3,343,377 | 4,511,185 → 6,182,304 | 50.70% → 33.81% | 41.26% / 55.67% (R wins) | 1,177,145 | 493,970 (+515,053 / -21,082) | Starr, Zapata, Reeves, La Salle, Kenedy, Loving |
| Agriculture Commissioner | 4,991,896 → 3,367,874 | 4,538,736 → 6,162,758 | 50.48% → 34.05% | 41.55% / 55.99% (R wins) | 1,206,132 | 417,888 (+442,221 / -24,333) | Starr, Zapata, Reeves, La Salle, Kenedy, Loving |
| Railroad Commissioner | 5,103,177 → 3,399,478 | 4,426,141 → 6,129,840 | 51.60% → 34.37% | 42.42% / 55.23% (R wins) | 1,197,294 | 506,404 (+527,879 / -21,475) | Starr, Zapata, Reeves, La Salle, Kenedy, Loving |

The quoted percentages vs SOS: all match the SOS figures at one decimal, with one exception. Railroad Commissioner French is SOS 45.55% (45.549…), which rounds to 45.5%, not the quoted 45.6%. Comptroller Huffines (not quoted) is SOS 46.15%. The graphics use the SOS percentages to two decimals.

## Counties that flip D → R, and counties that stay D

**U.S. Senate**: 21 flip: Harris, Tarrant, Bexar, Collin, Denton, Fort Bend, Williamson, Cameron, Brazoria, Bell, Nueces, Hays, Jefferson, Brazos, Kaufman, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Brewster. 19 stay D: Dallas, Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Frio, Zapata, Reeves, Duval, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

**Governor**: 21 flip: Harris, Tarrant, Bexar, Collin, Denton, Fort Bend, Williamson, Cameron, Brazoria, Nueces, Hays, Jefferson, Brazos, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Frio, Brewster, Culberson. 16 stay D: Dallas, Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Zapata, Duval, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg.

**Lieutenant Governor**: 21 flip: Harris, Dallas, Tarrant, Bexar, Collin, Denton, Fort Bend, El Paso, Williamson, Cameron, Brazoria, Nueces, Hays, Jefferson, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Frio, Brewster. 15 stay D: Travis, Hidalgo, Webb, Starr, Maverick, Willacy, Zapata, Duval, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

**Attorney General**: 19 flip: Harris, Tarrant, Bexar, Collin, Denton, Fort Bend, Williamson, Cameron, Brazoria, Nueces, Hays, Jefferson, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Brewster, Duval. 17 stay D: Dallas, Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Frio, Zapata, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

**Comptroller**: 18 flip: Harris, Dallas, Tarrant, Bexar, Collin, Fort Bend, Williamson, Cameron, Nueces, Hays, Jefferson, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Brewster, Duval. 16 stay D: Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Frio, Zapata, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

**Agriculture Commissioner**: 18 flip: Harris, Dallas, Tarrant, Bexar, Collin, Fort Bend, Williamson, Cameron, Nueces, Hays, Jefferson, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Brewster, Duval. 17 stay D: Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Frio, Zapata, Reeves, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

**Railroad Commissioner**: 19 flip: Harris, Tarrant, Bexar, Collin, Denton, Fort Bend, Williamson, Cameron, Brazoria, Nueces, Hays, Jefferson, Bastrop, Caldwell, Val Verde, Jim Wells, Kleberg, Brewster, Duval. 17 stay D: Dallas, Travis, Hidalgo, El Paso, Webb, Starr, Maverick, Willacy, Frio, Zapata, Zavala, Dimmit, Brooks, La Salle, Presidio, Jim Hogg, Culberson.

## Top 10 counties by votes removed

### U.S. Senate

| # | County | Population | Ballots | Talarico (D) | Paxton (R) | Removal pts | **Votes removed** | Talarico → | Paxton → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 907,617 | 451,780 | 20.32 | **281,185** | 626,432 | 732,965 |
| 2 | Dallas | 2,661,397 | 783,714 | 563,219 | 206,355 | 21.25 | **166,523** | 396,696 | 372,878 |
| 3 | Tarrant | 2,248,466 | 728,630 | 427,879 | 287,783 | 20.13 | **146,676** | 281,203 | 434,459 |
| 4 | Bexar | 2,160,088 | 658,445 | 440,271 | 206,838 | 20.88 | **137,471** | 302,800 | 344,309 |
| 5 | Travis | 1,389,670 | 548,782 | 430,707 | 109,791 | 23.26 | **127,667** | 303,040 | 237,458 |
| 6 | Collin | 1,297,179 | 457,641 | 252,403 | 197,096 | 22.19 | **101,535** | 150,868 | 298,631 |
| 7 | Denton | 1,069,346 | 396,235 | 211,266 | 177,859 | 19.90 | **78,858** | 132,408 | 256,717 |
| 8 | Fort Bend | 975,191 | 331,893 | 210,760 | 115,973 | 22.21 | **73,700** | 137,060 | 189,673 |
| 9 | Williamson | 752,827 | 278,668 | 164,626 | 108,074 | 20.98 | **58,455** | 106,171 | 166,529 |
| 10 | El Paso | 877,858 | 218,537 | 159,272 | 54,576 | 22.18 | **48,467** | 110,805 | 103,043 |

Top 10 total: **1,220,537** of 1,889,815 (64.6%).

### Governor

| # | County | Population | Ballots | Hinojosa (D) | Abbott (R) | Removal pts | **Votes removed** | Hinojosa → | Abbott → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 879,134 | 483,850 | 19.32 | **267,248** | 611,886 | 751,098 |
| 2 | Dallas | 2,661,397 | 783,714 | 539,682 | 231,770 | 19.42 | **152,197** | 387,485 | 383,967 |
| 3 | Tarrant | 2,248,466 | 728,630 | 410,931 | 307,297 | 18.70 | **136,258** | 274,673 | 443,555 |
| 4 | Bexar | 2,160,088 | 658,445 | 427,403 | 223,071 | 19.99 | **131,634** | 295,769 | 354,705 |
| 5 | Travis | 1,389,670 | 548,782 | 415,011 | 127,275 | 21.69 | **119,008** | 296,003 | 246,283 |
| 6 | Collin | 1,297,179 | 457,641 | 236,034 | 215,566 | 19.38 | **88,669** | 147,365 | 304,235 |
| 7 | Denton | 1,069,346 | 396,235 | 199,625 | 191,413 | 17.74 | **70,291** | 129,334 | 261,704 |
| 8 | Fort Bend | 975,191 | 331,893 | 200,996 | 126,055 | 20.22 | **67,118** | 133,878 | 193,173 |
| 9 | Williamson | 752,827 | 278,668 | 156,631 | 118,285 | 18.99 | **52,926** | 103,705 | 171,211 |
| 10 | El Paso | 877,858 | 218,537 | 153,639 | 61,410 | 20.78 | **45,407** | 108,232 | 106,817 |

Top 10 total: **1,130,756** of 1,758,291 (64.3%).

### Lieutenant Governor

| # | County | Population | Ballots | Goodwin (D) | Patrick (R) | Removal pts | **Votes removed** | Goodwin → | Patrick → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 859,832 | 479,785 | 21.49 | **297,342** | 562,490 | 777,127 |
| 2 | Dallas | 2,661,397 | 783,714 | 532,006 | 227,311 | 22.43 | **175,802** | 356,204 | 403,113 |
| 3 | Tarrant | 2,248,466 | 728,630 | 403,724 | 305,214 | 20.75 | **151,225** | 252,499 | 456,439 |
| 4 | Bexar | 2,160,088 | 658,445 | 412,605 | 221,647 | 21.37 | **140,713** | 271,892 | 362,360 |
| 5 | Travis | 1,389,670 | 548,782 | 408,059 | 120,085 | 24.77 | **135,952** | 272,107 | 256,037 |
| 6 | Collin | 1,297,179 | 457,641 | 232,267 | 211,916 | 21.15 | **96,799** | 135,468 | 308,715 |
| 7 | Denton | 1,069,346 | 396,235 | 195,793 | 189,464 | 19.41 | **76,900** | 118,893 | 266,364 |
| 8 | Fort Bend | 975,191 | 331,893 | 197,070 | 124,376 | 22.30 | **74,000** | 123,070 | 198,376 |
| 9 | Williamson | 752,827 | 278,668 | 153,704 | 114,540 | 20.95 | **58,371** | 95,333 | 172,911 |
| 10 | El Paso | 877,858 | 218,537 | 147,167 | 61,050 | 21.81 | **47,673** | 99,494 | 108,723 |

Top 10 total: **1,254,777** of 1,891,743 (66.3%).

### Attorney General

| # | County | Population | Ballots | Johnson (D) | Middleton (R) | Removal pts | **Votes removed** | Johnson → | Middleton → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 866,656 | 485,518 | 18.57 | **256,855** | 609,801 | 742,373 |
| 2 | Dallas | 2,661,397 | 783,714 | 541,306 | 224,254 | 19.80 | **155,141** | 386,165 | 379,395 |
| 3 | Tarrant | 2,248,466 | 728,630 | 406,594 | 307,316 | 18.23 | **132,857** | 273,737 | 440,173 |
| 4 | Bexar | 2,160,088 | 658,445 | 416,674 | 220,580 | 18.52 | **121,913** | 294,761 | 342,493 |
| 5 | Travis | 1,389,670 | 548,782 | 408,082 | 122,554 | 20.61 | **113,088** | 294,994 | 235,642 |
| 6 | Collin | 1,297,179 | 457,641 | 234,882 | 211,982 | 19.23 | **88,019** | 146,863 | 300,001 |
| 7 | Denton | 1,069,346 | 396,235 | 196,793 | 189,394 | 17.14 | **67,900** | 128,893 | 257,294 |
| 8 | Fort Bend | 975,191 | 331,893 | 198,035 | 125,030 | 19.47 | **64,614** | 133,421 | 189,644 |
| 9 | Williamson | 752,827 | 278,668 | 154,372 | 116,306 | 18.31 | **51,020** | 103,352 | 167,326 |
| 10 | El Paso | 877,858 | 218,537 | 151,206 | 59,060 | 19.83 | **43,343** | 107,863 | 102,403 |

Top 10 total: **1,094,750** of 1,673,652 (65.4%).

### Comptroller

| # | County | Population | Ballots | Eckhardt (D) | Huffines (R) | Removal pts | **Votes removed** | Eckhardt → | Huffines → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 844,026 | 486,236 | 18.42 | **254,779** | 589,247 | 741,015 |
| 2 | Dallas | 2,661,397 | 783,714 | 525,146 | 228,966 | 19.39 | **151,998** | 373,148 | 380,964 |
| 3 | Tarrant | 2,248,466 | 728,630 | 398,080 | 310,449 | 18.33 | **133,569** | 264,511 | 444,018 |
| 4 | Bexar | 2,160,088 | 658,445 | 408,036 | 218,527 | 18.71 | **123,211** | 284,825 | 341,738 |
| 5 | Travis | 1,389,670 | 548,782 | 401,617 | 122,918 | 21.24 | **116,566** | 285,051 | 239,484 |
| 6 | Collin | 1,297,179 | 457,641 | 228,670 | 214,170 | 18.96 | **86,758** | 141,912 | 300,928 |
| 7 | Denton | 1,069,346 | 396,235 | 191,748 | 191,932 | 16.96 | **67,200** | 124,548 | 259,132 |
| 8 | Fort Bend | 975,191 | 331,893 | 192,722 | 124,827 | 19.22 | **63,798** | 128,924 | 188,625 |
| 9 | Williamson | 752,827 | 278,668 | 151,699 | 116,619 | 18.60 | **51,831** | 99,868 | 168,450 |
| 10 | El Paso | 877,858 | 218,537 | 146,995 | 58,121 | 19.57 | **42,768** | 104,227 | 100,889 |

Top 10 total: **1,092,478** of 1,671,119 (65.4%).

### Agriculture Commissioner

| # | County | Population | Ballots | Tucker (D) | Sheets (R) | Removal pts | **Votes removed** | Tucker → | Sheets → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 831,663 | 504,898 | 17.21 | **238,124** | 593,539 | 743,022 |
| 2 | Dallas | 2,661,397 | 783,714 | 525,633 | 233,507 | 19.11 | **149,767** | 375,866 | 383,274 |
| 3 | Tarrant | 2,248,466 | 728,630 | 398,161 | 309,723 | 18.08 | **131,724** | 266,437 | 441,447 |
| 4 | Bexar | 2,160,088 | 658,445 | 408,042 | 220,095 | 18.40 | **121,142** | 286,900 | 341,237 |
| 5 | Travis | 1,389,670 | 548,782 | 392,710 | 128,077 | 19.24 | **105,583** | 287,127 | 233,660 |
| 6 | Collin | 1,297,179 | 457,641 | 224,532 | 216,102 | 17.83 | **81,586** | 142,946 | 297,688 |
| 7 | Denton | 1,069,346 | 396,235 | 190,169 | 192,070 | 16.33 | **64,713** | 125,456 | 256,783 |
| 8 | Fort Bend | 975,191 | 331,893 | 192,970 | 126,409 | 19.01 | **63,107** | 129,863 | 189,516 |
| 9 | Williamson | 752,827 | 278,668 | 148,723 | 117,748 | 17.27 | **48,127** | 100,596 | 165,875 |
| 10 | El Paso | 877,858 | 218,537 | 148,971 | 58,011 | 20.13 | **43,984** | 104,987 | 101,995 |

Top 10 total: **1,047,857** of 1,624,022 (64.5%).

### Railroad Commissioner

| # | County | Population | Ballots | Rosenthal (D) | French (R) | Removal pts | **Votes removed** | Rosenthal → | French → |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Harris | 5,045,026 | 1,383,480 | 864,866 | 471,449 | 19.21 | **265,738** | 599,128 | 737,187 |
| 2 | Dallas | 2,661,397 | 783,714 | 539,050 | 218,936 | 20.37 | **159,645** | 379,405 | 378,581 |
| 3 | Tarrant | 2,248,466 | 728,630 | 407,510 | 299,130 | 19.02 | **138,564** | 268,946 | 437,694 |
| 4 | Bexar | 2,160,088 | 658,445 | 412,910 | 216,732 | 18.73 | **123,309** | 289,601 | 340,041 |
| 5 | Travis | 1,389,670 | 548,782 | 405,135 | 116,453 | 21.01 | **115,304** | 289,831 | 231,757 |
| 6 | Collin | 1,297,179 | 457,641 | 232,026 | 207,935 | 19.17 | **87,734** | 144,292 | 295,669 |
| 7 | Denton | 1,069,346 | 396,235 | 194,504 | 187,651 | 17.13 | **67,867** | 126,637 | 255,518 |
| 8 | Fort Bend | 975,191 | 331,893 | 198,032 | 121,490 | 20.17 | **66,946** | 131,086 | 188,436 |
| 9 | Williamson | 752,827 | 278,668 | 152,598 | 113,887 | 18.32 | **51,055** | 101,543 | 164,942 |
| 10 | El Paso | 877,858 | 218,537 | 149,276 | 57,661 | 19.81 | **43,301** | 105,975 | 100,962 |

Top 10 total: **1,119,463** of 1,703,699 (65.7%).

## Honest notes for defending the method

- **Most of each total is the offset.** The offset accounts for 67.0% (Lt. Governor) to 75.6% (Governor) of the votes removed. The county gaps account for the remaining 24–33%. Kansas's write-up flagged the same pattern.
- **The offset is in every county by design.** Because removal = residual + b, a county that matches the Texas line exactly still has b points (about 12–14) of its Democratic share removed. Least-squares residuals sum to zero in points across the 254 counties (unweighted), but not in votes: the counties above the line are the big ones, so the county-gap part still comes to 417,888–623,566 votes per race. The flip comes mainly from applying the offset everywhere.
- **Where the county-gap portion sits.** The Texas line is unweighted, so the many small rural counties set it. The big metro counties sit above it, which is why Harris, Dallas, Tarrant, Bexar and Travis lead every top-10 list. If the line were instead fitted with each county weighted by its ballots, the county-gap portion would net to zero statewide by construction.
- **The metro numbers are large because the counties are large.** Removal points are similar everywhere (about 17–25 in the big counties); multiplying by Harris's 1.38 million ballots produces 238,000–297,000 votes.
- **Ballots denominator.** The SOS 'ballots cast' field in the election-night file equals the U.S. Senate race total in every county. Down-ballot races can therefore exceed it. Governor exceeds it in 241 counties, and Governor Dem + Rep exceeds it in 11 (Starr, Maverick, Zapata, Duval, Zavala, La Salle, Jim Hogg, Culberson, Terrell, Kent, McMullen).
- **Duval** shows the known down-ballot reporting problem in AG, Comptroller, Agriculture and Railroad: Dem + Rep exceeds its 3,280 ballots (AG: 3,532 D + 1,522 R). Its 'flip' in those four races rests on that bad data. Throckmorton is also over-ballot in Comptroller.
- **Starr and Zapata** have election-night ballot counts known to run low against the canvass (Starr canvass 14,930 vs 13,082 in the file). Both come out negative and are zeroed in several races.
- **Railroad Commissioner:** the SOS file has a single race, 'RAILROAD COMMISSIONER' (ID 4843, Rosenthal vs French). The 'Term Exp 2032' label is not in the file.
- The exact Kansas full-reversal script was not found on this machine. This build follows the t70u spec: residual + offset, negatives zeroed, votes moved D → R. The Governor line here (−31.69, 13.45) reproduces the provisional 2026 Texas Governor line exactly.

## Verification

Pass A (pandas/statsmodels) and Pass B (Python standard library, exact Fractions, race and candidate IDs discovered by office name and party) each re-read the raw SOS JSON for all 254 counties. Each race also checks SOS statewide candidate totals and the SOS-published percentages (election_53815.json; compared at the SOS's own precision).

| Race | County cells | Summary checks | SOS statewide checks | Total | Mismatches |
|---|---|---|---|---|---|
| U.S. Senate | 8,890 | 40 | 5 | 8,935 | 0 |
| Governor | 8,890 | 40 | 5 | 8,935 | 0 |
| Lieutenant Governor | 8,890 | 40 | 5 | 8,935 | 0 |
| Attorney General | 8,890 | 40 | 5 | 8,935 | 0 |
| Comptroller | 8,890 | 40 | 5 | 8,935 | 0 |
| Agriculture Commissioner | 8,890 | 40 | 5 | 8,935 | 0 |
| Railroad Commissioner | 8,890 | 40 | 5 | 8,935 | 0 |
| **All** | | | | **62,545** | **0** |

## Files
- master/TX_<race>_full_reversal_master.xlsx (sheets: All 254 counties with a SUM total row, Top 10 removals, Statewide) and master/TX_<race>_full_reversal_master_254_counties.csv
- master/TX_<race>_top10_removals.csv
- graphics/1–7_TX_<race>_injection_removed.png (2160×2160)
- passA/, passB/, verification/ (logs, compare_summary.json), scripts/