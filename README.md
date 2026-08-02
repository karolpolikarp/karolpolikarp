# Karol Polikarp Wilczyński

Lawyer at Poland's **Ministry of Digital Affairs**, working on AI Act regulatory sandboxes. Outside that I build and run production systems — real-time OSINT aggregation, legal search over ~15,000 Polish statutes, on-device PII anonymisation — mostly self-hosted on a Raspberry Pi.

[![karolwilczynski.com](https://img.shields.io/badge/karolwilczynski.com-004d2b?style=flat-square&logo=firefoxbrowser&logoColor=c9a962&labelColor=12100d)](https://karolwilczynski.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-6b1d1d?style=flat-square&logo=linkedin&logoColor=white&labelColor=12100d)](https://linkedin.com/in/karolpwilczynski)
[![Email](https://img.shields.io/badge/karolpwilczynski%40gmail.com-12100d?style=flat-square&logo=maildotru&logoColor=c9a962)](mailto:karolpwilczynski@gmail.com)

## Zorza — real-time OSINT aggregation

Telegram (MTProto), RSS, X and satellite/market sensors in one multi-column dashboard. Every item is scored for credibility; a push alert lands in about a second.

[![live](https://img.shields.io/badge/live-zorza.karolwilczynski.com-004d2b?style=flat-square&labelColor=12100d)](https://zorza.karolwilczynski.com)
![TypeScript](https://img.shields.io/badge/TypeScript-12100d?style=flat-square&logo=typescript&logoColor=c9a962)
![source](https://img.shields.io/badge/source-private-6b1d1d?style=flat-square&labelColor=12100d)

<img src="https://karolwilczynski.com/assets/images/zorza.webp" width="100%" alt="Zorza dashboard: live TV panes beside multi-column feeds of Telegram, RSS and sensor items, each row carrying a credibility score and source attribution">

Node 20 · Fastify 5 · SQLite + FTS5 · React 18 · Claude Haiku 4.5 for what the rules don't resolve · local embeddings, offline · Raspberry Pi 5 behind a Cloudflare Tunnel.

- 25,210 LOC · 242 tests · 32 API routes · 174 commits in 13 days
- 100 content channels (41 Telegram, 59 RSS) + ~15 sensor APIs · 58,134 archived entries
- Dedup threshold derived from measurement: literal repost `0.83` Jaccard, paraphrase `0.39` → cut at `0.70`
- Batching gate took LLM calls from 51 to 4 per hour — **$2.06/day** all in, against $31,980/yr for a Bloomberg Terminal

> Rules decide first. The LLM only runs on what the rules didn't resolve.

## Open source

| Repo | ⭐ | What | Lang |
|---|---|---|---|
| **[parawan](https://github.com/karolpolikarp/parawan)** · [live](https://parawan.karolwilczynski.com) | [![](https://img.shields.io/github/stars/karolpolikarp/parawan?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/parawan/stargazers) | Polish PII anonymiser — one self-contained HTML file, 100% offline, zero dependencies | TypeScript |
| **[anonimizator-ai](https://github.com/karolpolikarp/anonimizator-ai)** | | On-device NER layer for Parawan: recall on rare surnames **21% → 79–90%**, precision holds at **99.6%** | TypeScript |
| **[ISAP-scraper](https://github.com/karolpolikarp/ISAP-scraper)** | [![](https://img.shields.io/github/stars/karolpolikarp/ISAP-scraper?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/ISAP-scraper/stargazers) | Client for the Polish Parliament ELI API — fetch, monitor and pull full text of Polish law | Python |
| **[claude-usage-streamdeck](https://github.com/karolpolikarp/claude-usage-streamdeck)** · [page](https://karolwilczynski.com/claude-usage-streamdeck/) | | Live Claude usage on Stream Deck keys. 1 dependency, no telemetry | JavaScript |
| **[Stefka-PPLuM-macOS.Silicon](https://github.com/karolpolikarp/Stefka-PPLuM-macOS.Silicon)** | | Offline meeting transcription and summaries on Apple Silicon: mlx-whisper + PLLuM-12B | Python |
| **[Multi-Sequence-Clicker](https://github.com/karolpolikarp/Multi-Sequence-Clicker)** | | Auto-clicker with Bézier-curve humanised cursor motion, no dependencies beyond the JDK | Java |

## In production

<table>
<tr>
<td><a href="https://jakieprawo.pl"><img src="https://karolwilczynski.com/assets/images/obraz_2026-01-09_205957107.webp" width="210" alt="JakiePrawo.pl — a plain-language question answered with the exact statute and article"></a></td>
<td><a href="https://upfor.pl"><img src="https://karolwilczynski.com/assets/images/upfor.webp" width="210" alt="UpFor.pl — shared availability heatmap across a group"></a></td>
<td><a href="https://majeranek.vercel.app"><img src="https://karolwilczynski.com/assets/images/majeranek.webp" width="210" alt="Majeranek — drag-and-drop tier list feeding cross-media recommendations"></a></td>
<td><a href="https://replica.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/margiela.webp" width="210" alt="AutoMargiela — price history across three retailers with buy-signal markers"></a></td>
</tr>
</table>

| Product | What it does | Stack | Scale |
|---|---|---|---|
| **[JakiePrawo.pl](https://jakieprawo.pl)** `BETA` | Plain-language search across ~15,000 Polish statutes | React · Supabase + pgvector · Claude API · MCP server on a Raspberry Pi | ~55k LOC · a 7-layer pipeline validates every citation before it is shown |
| **[UpFor.pl](https://upfor.pl)** `BETA` | Availability calendar for gaming groups | Next.js 15 · tRPC v11 · Turborepo · `LISTEN/NOTIFY` → SSE · Claude Haiku with tool-use | ~113k LOC · 20 routers / ~125 procedures · Discord bot, 18 commands |
| **[Majeranek](https://majeranek.vercel.app)** `ALPHA` | Cross-media recommendations from drag-and-drop tier lists | Next.js 14 · Supabase (53 models, RLS) | ~110k LOC · ELO / Glicko-2 duel ranking |
| **[AutoMargiela](https://replica.karolwilczynski.com)** | Price monitor across Notino, Sephora and Flaconi | Python · Playwright on a systemd timer · Flask + SQLite | ~14k LOC · z-score and percentile buy signals |

## Data science

[ESPI → stock forecasts](https://github.com/karolpolikarp/ds-SGH-Prognozy-gieldowe-z-ESPI) (can GPT-4o-mini call Allegro from 134 filings over 1,050 sessions?) · [video game sales](https://github.com/karolpolikarp/ds-VideoGameSales) (~16.5k titles, K-Means + RandomForest) · [Airbnb Winnipeg](https://github.com/karolpolikarp/ds-Winnipeg) (R: MICE, k-means, leaflet) · [Airbnb D.C.](https://github.com/karolpolikarp/ds-WashingtonDC) (chi-square + OLS) · [speed dating](https://github.com/karolpolikarp/ds-speed-dating) (PCA + K-Means)

## Background

Lawyer, University of Warsaw. Postgraduate: Big Data (PJATK) · AI in Business and the Public Sector (SGH) · Python for AI (PJATK) · IT Systems and Databases (PJATK). Certificates: NVIDIA Deep Learning · AI_devs 4 Builders · AI_devs 3 Agents · Java Developer Plus · ITIL 4 Foundation.

<details>
<summary><b>Wersja polska</b></summary>

Prawnik w **Ministerstwie Cyfryzacji**, zajmuję się piaskownicami regulacyjnymi AI Act. Poza tym buduję i utrzymuję systemy produkcyjne: agregację OSINT w czasie rzeczywistym, wyszukiwarkę po ~15 000 polskich aktów prawnych i lokalną anonimizację danych osobowych — w większości self-hosted na Raspberry Pi.

**[Zorza](https://zorza.karolwilczynski.com)** — Telegram (MTProto), RSS, X i sensory satelitarno-rynkowe w jednym wielokolumnowym pulpicie, każdy wpis z oceną wiarygodności, alert push w około sekundę. Node 20, Fastify 5, SQLite z FTS5, React 18, Claude Haiku 4.5 tylko tam, gdzie reguły nie rozstrzygnęły, embeddingi lokalnie. 25 210 linii kodu, 242 testy, 100 kanałów treści, 58 134 wpisy w archiwum, 2,06 USD na dobę. Repozytorium prywatne, landing publiczny.

**Otwarty kod** — [parawan](https://github.com/karolpolikarp/parawan) (anonimizator polskich danych osobowych, jeden plik HTML, offline) · [anonimizator-ai](https://github.com/karolpolikarp/anonimizator-ai) (warstwa NER na urządzeniu, czułość na rzadkich nazwiskach 21% → 79–90%) · [ISAP-scraper](https://github.com/karolpolikarp/ISAP-scraper) (klient API ELI Sejmu) · [claude-usage-streamdeck](https://github.com/karolpolikarp/claude-usage-streamdeck) (zużycie Claude na klawiszach Stream Decka) · [Stefka](https://github.com/karolpolikarp/Stefka-PPLuM-macOS.Silicon) (offline'owa transkrypcja spotkań na Apple Silicon) · [Multi-Sequence-Clicker](https://github.com/karolpolikarp/Multi-Sequence-Clicker) (autoklikacz z ruchem po krzywych Béziera)

**W produkcji** — [JakiePrawo.pl](https://jakieprawo.pl) (wyszukiwarka ~15 000 polskich aktów prawnych, 7-warstwowy pipeline waliduje każdy przywołany przepis) · [UpFor.pl](https://upfor.pl) (kalendarz dostępności dla ekip growych, bot Discord) · [Majeranek](https://majeranek.vercel.app) (rekomendacje międzymedialne z tier list) · [AutoMargiela](https://replica.karolwilczynski.com) (monitor cen z sygnałami zakupu)

**Zaplecze** — prawnik, Uniwersytet Warszawski. Studia podyplomowe: Big Data (PJATK), Sztuczna inteligencja w biznesie i sektorze publicznym (SGH), Python w AI (PJATK), Systemy informatyczne i bazy danych (PJATK).

</details>
