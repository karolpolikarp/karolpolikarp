### Karol Polikarp Wilczyński

Chief Specialist in the Innovative Public Policies Division at Poland's **Ministry of Digital Affairs**, working on AI Act implementation and on putting AI to work across public administration. Lawyer by training. Outside that I build and run production systems end to end. Cloud where managed infrastructure earns its price, a self-hosted Raspberry Pi where it doesn't.

<div align="center">
<a href="https://zorza.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/zorza.webp" height="230" alt="Zorza — multi-column dashboard of Telegram, RSS and sensor items, each row carrying a credibility score and source attribution"></a> <a href="https://jakieprawo.pl"><img src="https://karolwilczynski.com/assets/images/obraz_2026-01-09_205957107.webp" height="230" alt="JakiePrawo.pl — a plain-language question answered with the exact statute, article and a link to the official text"></a>
<br>
<a href="https://upfor.pl"><img src="https://karolwilczynski.com/assets/images/upfor.webp" height="230" alt="UpFor.pl — weekly availability grid rendered as an overlap heatmap for a group"></a> <a href="https://parawan.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/parawan.webp" height="230" alt="Parawan — source text on the left, the same text with personal data masked on the right"></a> <a href="https://replica.karolwilczynski.com"><img src="https://karolwilczynski.com/assets/images/margiela.webp" height="230" alt="AutoMargiela — price history for a fragrance across three retailers, with buy-signal markers"></a>
</div>

**What I run**

- **[Zorza](https://zorza.karolwilczynski.com)** — real-time OSINT aggregation. Telegram (MTProto), RSS and ~15 sensor APIs in one dashboard, every item scored for credibility, push alert in about a second. 25,210 LOC, 242 tests, 58,134 archived entries, **$2.06/day** on a Raspberry Pi 5. Source private, instance live.
- **[JakiePrawo.pl](https://jakieprawo.pl)** — plain-language search across ~15,000 Polish statutes. A 7-layer pipeline validates every citation before it is shown. React, Supabase + pgvector, Claude API, an MCP server on a Pi.
- **[UpFor.pl](https://upfor.pl)** — availability calendar for gaming groups. Next.js 15, tRPC v11, 20 routers / ~125 procedures, Discord bot with 18 commands.
- **[Parawan](https://parawan.karolwilczynski.com)** — Polish PII anonymiser (PESEL, NIP, REGON, IBAN, names) in one self-contained HTML file. Fully offline, zero dependencies.
- **[AutoMargiela](https://replica.karolwilczynski.com)** — price monitor for Maison Margiela Replica across Notino, Sephora and Flaconi. Playwright on a 6-hour systemd timer, Flask + SQLite dashboard, z-score and percentile buy signals.

**Open source**

- **[parawan](https://github.com/karolpolikarp/parawan)** [![](https://img.shields.io/github/stars/karolpolikarp/parawan?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/parawan/stargazers) — the anonymiser above. PESEL, NIP, REGON, IBAN and personal names stripped from text before it reaches an AI chat, in one self-contained HTML file. <sub>TypeScript · Apache-2.0</sub>
- **[anonimizator-ai](https://github.com/karolpolikarp/anonimizator-ai)** — its optional on-device NER layer. Recall on rare surnames climbs 21% → 79–90% while precision holds at 99.6%. <sub>TypeScript · Apache-2.0</sub>
- **[ISAP-scraper](https://github.com/karolpolikarp/ISAP-scraper)** [![](https://img.shields.io/github/stars/karolpolikarp/ISAP-scraper?style=flat-square&label=&labelColor=12100d&color=004d2b)](https://github.com/karolpolikarp/ISAP-scraper/stargazers) — client for the Polish Parliament ELI API: fetch, monitor and pull the full text of Polish law. 6 CLI modes. <sub>Python · MIT</sub>
- **[claude-usage-streamdeck](https://github.com/karolpolikarp/claude-usage-streamdeck)** — live Claude usage on Stream Deck keys: 5-hour session, week, credits, today's token cost. One dependency, no telemetry. <sub>JavaScript · MIT</sub>
- **[Stefka](https://github.com/karolpolikarp/Stefka-PPLuM-macOS.Silicon)** — offline meeting transcription and summaries on Apple Silicon. mlx-whisper + PLLuM-12B, nothing leaves the machine. <sub>Python · MIT</sub>
- **[Multi-Sequence-Clicker](https://github.com/karolpolikarp/Multi-Sequence-Clicker)** — auto-clicker with Bézier-curve cursor motion, so replayed sequences don't look robotic. <sub>Java · MIT</sub>

**Elsewhere** · [karolwilczynski.com](https://karolwilczynski.com) · [LinkedIn](https://linkedin.com/in/karolpwilczynski) · karolpwilczynski@gmail.com
