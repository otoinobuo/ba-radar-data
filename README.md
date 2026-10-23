# BA Cybersecurity radar data

Daily snapshots of the five public radars published at [ba-cybersecurity.com/radar](https://ba-cybersecurity.com/radar/). Each snapshot is the `data.json` that the live page was rendered from on that day, copied from the live site.

| Radar | Page | What it records |
|---|---|---|
| `japan` | [Japan Breach Radar](https://ba-cybersecurity.com/radar/) | Cyber incidents publicly disclosed by organisations in Japan |
| `us` | [US Breach Radar](https://ba-cybersecurity.com/radar/us/) | Cyber incidents disclosed by US organisations (SEC 8-K Item 1.05, HHS, state attorney-general notices) |
| `waf` | [WAF Rule Watch](https://ba-cybersecurity.com/radar/waf/) | Public rule updates by WAF vendors and which exploited vulnerabilities their texts name |
| `php2shell` | [PHP2Shell Watch](https://ba-cybersecurity.com/radar/php2shell/) | Public reports on exploitation of CVE-2026-109618 and CVE-2026-109619, and how many say an attack succeeded |
| `ransomware` | [Ransomware Radar](https://ba-cybersecurity.com/radar/ransomware/) | Ransomware leak-site claims worldwide and statistics from publicly released negotiation chats (snapshots from 2026-10-24) |

## Files

- `data/<radar>/<YYYY>/<YYYY-MM-DD>.json` — the snapshot for that day (Japan time). A file is written only on days when the content changed; the generation timestamp alone does not count as a change. If a page changes twice in one day, the later version is kept.
- `latest/<radar>.json` — the most recent snapshot.
- `snapshots.csv` — one row per snapshot: date, radar, file, generation time, reference date, SHA-256 and size.

The structure of each file is described in the Method section of its page. JSON is written with sorted keys and one value per line so that day-to-day changes are readable as diffs.

## Corrections

Corrections are made in later snapshots. Earlier snapshots are kept exactly as they were published, so the history shows what was public on each day, including entries that were later corrected or removed. To report an error, write to otoi@ba-cybersecurity.com.

## Licence and citation

Counts, tables and classifications are licensed under [CC BY 4.0](LICENSE). Titles, headlines and figures quoted from third parties remain with their owners. Please cite the page you use, for example:

> BA Cybersecurity. PHP2Shell Watch [data set]. https://ba-cybersecurity.com/radar/php2shell/ . Snapshot of 2026-10-23, https://github.com/otoinobuo/ba-radar-data .

Published by BA Cybersecurity, Tokyo, Japan · [ORCID 0009-0001-1445-3612](https://orcid.org/0009-0001-1445-3612)

---

## 日本語

[ba-cybersecurity.com/radar](https://ba-cybersecurity.com/radar/) で公開している 5 つのレーダーの、日ごとの記録です。各ファイルは、その日に公開ページが描画に使った `data.json` を、公開中のサイトから写したものです。

- `data/<レーダー>/<年>/<年-月-日>.json` — その日(日本時間)の記録。内容が変わった日だけ書きます(生成時刻だけの違いは変化に数えません)。同じ日に 2 回変わったときは後の版を残します。
- `latest/<レーダー>.json` — 最新の記録。
- `snapshots.csv` — 記録ごとに 1 行(日付・レーダー・ファイル・生成時刻・基準日・SHA-256・サイズ)。

**訂正について:** 訂正は後の版で行い、過去の版は公開したときのまま残します。後に訂正・削除した項目も含めて、その日に何が公開されていたかを履歴でたどれるようにするためです。誤りのご連絡は otoi@ba-cybersecurity.com へ。

件数・表・分類は CC BY 4.0 で提供します。引用した題名や数値など第三者の情報の権利は各権利者にあります。
