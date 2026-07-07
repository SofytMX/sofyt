# sofyt.mx

The landing page for **Sofyt** — a small studio that builds measurement instruments for engineers who would rather be correct than encouraged.

**Live at [sofyt.mx](https://sofyt.mx)**

## The instruments

- **[PaperClob](https://paperclob.com)** — a paper CLOB wire-compatible with Polymarket, plus a simulator that grades trading bots against the real recorded tape: the edge your backtest promises vs the edge reality would actually fill. Built for AI agents. *Calibration: every strategy in our own catalog graded phantom or no-edge — the engine refuses to flatter us, too.*
- **[LLCrawler](https://llcrawler.com)** — an LLM-visibility auditor. Measures how visible and legible your site is to AI crawlers and models, then hands you the fixes as paste-ready output. *Calibration: the first site it audited was our own — 20/100. We fixed the site, not the scorer.*

## The stack

One hand-written HTML file. No framework, no build step, no tracking, nothing fetched from anywhere. What ships alongside it:

```
index.html      the entire site — inline CSS, system fonts, dark/light aware
og.png          social card (generated with PIL, reviewed by eye)
llms.txt        summary for AI agents — https://sofyt.mx/llms.txt
robots.txt      intentionally open; AI crawlers explicitly welcome
sitemap.xml     one URL, as it should be
```

View source on the live page — that's the entire codebase. This repo exists so it has a home and a history.

## Deploying

Served by a shared [Caddy](https://caddyserver.com/) behind Cloudflare. A deploy is:

```sh
rsync -a --exclude=.git ./ /srv/sofyt/
```

No pipeline. The page is 11 KB; the pipeline would be bigger than the product.

## Contact

**support@sofyt.mx**

---

MIT — see [LICENSE](LICENSE) if you want to borrow the layout. The words and the products they describe are ours.
