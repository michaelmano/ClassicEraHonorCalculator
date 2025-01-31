# Classic Era Honor Calculator
![Build](https://github.com/soFFe/ClassicEraHonorCalculator/actions/workflows/angular-gh-pages.yml/badge.svg)

A simple Angular Web-App intended for World of Warcraft Classic Era PvP players.
The 1.14.4 PvP System Update indirectly introduced limits to the amount of Rank Progress you can gain in one week.
This Calculator is meant for people who want to min/max these limits.

## Terminology
"Contribution Points" as explained by Blizzard, is a term that was very confusing to everyone I spoke to, as Blizzard uses the term Contribution Points for 2 very different things.
That's why I have decided to rephrase this to two different phrases:
1. Rating / Rating Points that represent your actual rank and your Progress within this rank. These are rewarded at specific milestones you qualify for.
2. Qualification Points that represent the rank you have qualified for by farming a specific amount of Honor within 1 week.

## Ranking information used in this Calculator
| Rank | Rating Required for Rank | Change factor for Rank |
|:----:|:------------------------:|:----------------------:|
| 1    | 0                        | 1.0                    |
| 2    | 2000                     | 1.0                    |
| 3    | 5000                     | 1.0                    |
| 4    | 10000                    | 0.8                    |
| 5    | 15000                    | 0.8                    |
| 6    | 20000                    | 0.8                    |
| 7    | 25000                    | 0.7                    |
| 8    | 30000                    | 0.7                    |
| 9    | 35000                    | 0.6                    |
| 10   | 40000                    | 0.5                    |
| 11   | 45000                    | 0.5                    |
| 12   | 50000                    | 0.4                    |
| 13   | 55000                    | 0.4                    |
| 14   | 60000                    | 0.34                   |

Honor requirements have been provided by Beastinblack @ Firemaw-EU. Thank you!

## Honor Conversion Brackets
What I call Conversion Brackets are the Ranges of Ranks that have different QP/Honor Conversion Rates, as stated in Blizzards Bluepost.
These are equal for all Ranks within the Bracket.

| BracketId | MinimumRank | MaximumRank | QP to Honor Conversion Rate |
|:---------:|:-----------:|:-----------:|:-------------------------------------:|
| 0         | 1           | 6           | 45000/20000 = 2.25                    |
| 1         | 7           | 10          | (175000-45000)/(40000-20000) = 6.5    |
| 2         | 11          | 14          | (500000-175000)/(60000-40000) = 16.25 |

## Decay
What we know about Decay:
1. You will decay if you could not qualify for your current Rank
2. You cannot downrank by Decay
3. Decay will take away up to 2500 Rating Points (exact formular unknown)

## References
- [Dishonorable Kills Change](https://us.forums.blizzard.com/en/wow/t/so-how-does-this-dishonorable-kill-system-work/1664598/38)
- [WoW Classic Era 1.14.4 PvP Ranking Update Examples](https://eu.forums.blizzard.com/en/wow/t/wow-classic-era-1144-pvp-ranking-update-examples/463646)
- [Classic Era 1.14.4 PvP Update](https://eu.forums.blizzard.com/en/wow/t/classic-era-1144-pvp-update/457615)
- [Beastinblack-Firemaw's Calculation Google Doc](https://docs.google.com/spreadsheets/d/1vX1eXeDflKf7mC1PHm_5OhSKv6LjjjZEe3DzWHqyCKM/copy)

## Project Dependencies
- Angular 16.2
- node
- npm
- Bootstrap 5.3.1
