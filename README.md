# pailiku-poker-data

Exact Texas Hold'em probability tables from Pailiku (pailiku.com, by Innora.ai), computed by deterministic enumeration — not Monte Carlo simulation.

Source page: https://pailiku.com/zh/poker-odds-dataset · Same data as JSON on the site: https://pailiku.com/poker-odds-dataset.json

## Files

| File | Contents |
|---|---|
| `hand-categories-5card.csv` | The 10 five-card hand categories: exact number of combinations out of C(52,5) = 2,598,960, probability, and odds against. The ten counts add up to exactly 2,598,960. |
| `outs-equity.csv` | For 1–20 outs: exact chance to hit at least one out after the flop (47 unseen cards, two cards to come) and after the turn (46 unseen cards, one card to come), next to the rule-of-4 / rule-of-2 approximations. |
| `poker-odds-dataset.json` | The same data in one JSON file, byte-identical to the copy on pailiku.com. |

Every number comes from the site's calculation module (`lib/poker-math.ts`) and was re-checked against the closed-form counts before publishing. Each figure states its sample space; for example, a royal flush is 4 of the 2,598,960 five-card hands. Seven-card figures are not included.

## Use

- License: CC BY 4.0 — attribution "Pailiku (pailiku.com)".
- These are mathematical facts about a deck of cards, for learning. Pailiku does not offer real-money games, does not link to gambling sites, and gives no betting advice.

## 中文说明

牌力库（Pailiku）德州扑克精确概率表，全部来自站内确定性计算（lib/poker-math.ts），不是模拟。

- `hand-categories-5card.csv`：五张牌组合总数 C(52,5) = 2,598,960，10 种牌型各自的精确组合数与概率，十项相加正好等于 2,598,960。
- `outs-equity.csv`：1–20 个 outs，翻牌后（剩 47 张、再发两张）和转牌后（剩 46 张、再发一张）的精确命中率，旁边附「乘 4 / 乘 2」近似值。
- `poker-odds-dataset.json`：与 pailiku.com 上的数据文件完全一致。

许可为 CC BY 4.0。本数据仅供学习，不提供真钱游戏、不链接博彩网站、不给下注建议。
