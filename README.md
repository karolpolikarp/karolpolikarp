### Karol Polikarp Wilczyński | u/karolpolikarp | karolwilczynski.com

Chief Specialist in the Innovative Public Policies Division at Poland's **Ministry of Digital Affairs**, working on AI Act implementation and on putting AI to work across public administration. Lawyer by training. Outside that I build and run production systems end to end. Cloud where managed infrastructure earns its price, a self-hosted Raspberry Pi where it doesn't.

<div align="center">
<a href="https://zorza.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/zorza.webp" width="320" height="180" alt="Zorza — dark dashboard: a live TV news wall and market ticker beside columns of Telegram and RSS items, several tagged with a credibility score and a source count"></a> <a href="https://jakieprawo.pl"><img src="https://karolwilczynski.com/assets/images/jakieprawo.webp" width="233" height="180" alt="JakiePrawo.pl — landing page: ask in plain language, search statutes, or attach a document"></a>
<br>
<a href="https://upfor.pl"><img src="https://karolwilczynski.com/assets/images/upfor.webp" width="202" height="180" alt="UpFor.pl — weekly availability grid for a group, overlapping free slots highlighted"></a> <a href="https://parawan.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/parawan.webp" width="143" height="180" alt="Parawan — the four processing steps, a marker colour legend, and a source-text versus anonymised-output comparison"></a> <a href="https://replica.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/margiela.webp" width="258" height="180" alt="AutoMargiela — price tracker across three retailers: deal of the day, recent drops, and a record price per fragrance"></a>
</div>

#### What I run

- **[Zorza](https://zorza.karolwilczynski.com)** *(private repo, live instance)* — real-time OSINT aggregation. 100 content channels (41 Telegram over MTProto, 59 RSS) plus ~15 sensor APIs in one dashboard, every item carrying a credibility score and its sources. 25,210 LOC, 242 tests, 58,134 entries on a rolling 30-day archive, $2.06/day to run.
- **[JakiePrawo.pl](https://jakieprawo.pl)** — plain-language search across ~15,000 Polish statutes. A 7-layer pipeline validates every citation before it is shown. React, Supabase + pgvector, Claude API, an MCP server on a Pi.
- **[UpFor.pl](https://upfor.pl)** — availability calendar for gaming groups. Next.js 15, tRPC v11, 20 routers / ~125 procedures, Discord bot with 18 commands.
- **[AutoMargiela](https://replica.karolwilczynski.com)** — price monitor for Maison Margiela Replica across Notino, Sephora and Flaconi. Playwright on a 6-hour systemd timer, Flask + SQLite dashboard, z-score and percentile buy signals.

#### Open source

- **[parawan](https://github.com/karolpolikarp/parawan)** — PESEL, NIP, REGON, IBAN and personal names stripped from text before it reaches an AI chat. One self-contained HTML file, no network calls. <sub>TypeScript · Apache-2.0</sub> [![stars](https://img.shields.io/github/stars/karolpolikarp/parawan?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/parawan/stargazers)
- **[anonimizator-ai](https://github.com/karolpolikarp/anonimizator-ai)** — its optional on-device NER layer, still WIP. Recall on rare surnames climbs 21% → 79–90% while precision holds at 99.6%. <sub>TypeScript · Apache-2.0</sub>
- **[ISAP-scraper](https://github.com/karolpolikarp/ISAP-scraper)** — client for the Polish Parliament ELI API: fetch, monitor and pull the full text of Polish law. <sub>Python · MIT</sub> [![stars](https://img.shields.io/github/stars/karolpolikarp/ISAP-scraper?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/ISAP-scraper/stargazers)
- **[claude-usage-streamdeck](https://github.com/karolpolikarp/claude-usage-streamdeck)** — live Claude usage on Stream Deck keys: 5-hour session, week, credits, today's token cost. One dependency, no telemetry. <sub>JavaScript · MIT</sub>
- **[Stefka](https://github.com/karolpolikarp/Stefka-PPLuM-macOS.Silicon)** — offline meeting transcription and summaries on Apple Silicon. mlx-whisper + PLLuM-12B, nothing leaves the machine. <sub>Python · MIT</sub>
- **[Multi-Sequence-Clicker](https://github.com/karolpolikarp/Multi-Sequence-Clicker)** — auto-clicker with Bézier-curve cursor motion, so replayed sequences don't look robotic. <sub>Java · MIT</sub>

**Elsewhere** · [karolwilczynski.com](https://karolwilczynski.com) · [LinkedIn](https://linkedin.com/in/karolpwilczynski) · czesc@karolwilczynski.com
