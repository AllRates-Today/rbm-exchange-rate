# Reserve Bank of Malawi Exchange Rates API — rbm-exchange-rate

[![npm version](https://img.shields.io/npm/v/rbm-exchange-rate.svg)](https://www.npmjs.com/package/rbm-exchange-rate)
[![license](https://img.shields.io/npm/l/rbm-exchange-rate.svg)](https://github.com/AllRates-Today/rbm-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/rbm-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/MWK today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Frbm%3Fsource%3DUSD%26target%3DMWK&query=%24.rate&label=USD%2FMWK%20published%20by%20Reserve%20Bank%20of%20Malawi&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/rbm/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Frbm%3Fsource%3DUSD%26target%3DMWK&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/rbm/)

**Official Reserve Bank of Malawi (Malawi) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Reserve Bank of Malawi itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — Reserve Bank of Malawi's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2016** — point-in-time tables and daily series for any past date
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Reserve Bank of Malawi itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## ⚡ Try it without a key

The latest Reserve Bank of Malawi table is also served keyless, CORS-open and edge-cached, for evaluation, embeds and AI agents:

```bash
curl "https://allratestoday.com/api/open/central-bank/rbm?source=USD&target=MWK"
```

```js
const r = await fetch('https://allratestoday.com/api/open/central-bank/rbm').then((x) => x.json());
console.log(r.rate_date, r.rates.length); // the central bank's latest published table, no key
```

The open endpoint serves the *latest* table only and asks for a visible attribution link. The client below uses the keyed API, which adds point-in-time tables, history, and CSV/XML/Excel output.

## 📈 Latest published table

Today's full Reserve Bank of Malawi table, straight from the central bank's latest publication. On GitHub it is refreshed by [a daily Action](.github/workflows/daily-table.yml) that reads the keyless endpoint above and commits only when the central bank publishes a new table; the copy on npm is as of the package's publish date.

<!-- daily-table:start -->
Published **2026-10-09** by Reserve Bank of Malawi — 114 rates, first 60 shown. Updated 2026-10-09.

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | MWK | buy | 467.5226 |
| AED | MWK | middle | 472.1483 |
| AED | MWK | sell | 476.7739 |
| ARS | MWK | buy | 1.1326 |
| ARS | MWK | middle | 1.1438 |
| ARS | MWK | sell | 1.155 |
| AUD | MWK | buy | 1199.0389 |
| AUD | MWK | middle | 1210.9021 |
| AUD | MWK | sell | 1222.7653 |
| BWP | MWK | buy | 123.6256 |
| BWP | MWK | middle | 124.8488 |
| BWP | MWK | sell | 126.0719 |
| CAD | MWK | buy | 1207.9806 |
| CAD | MWK | middle | 1219.9323 |
| CAD | MWK | sell | 1231.884 |
| CHF | MWK | buy | 2128.7125 |
| CHF | MWK | middle | 2149.7739 |
| CHF | MWK | sell | 2170.8353 |
| CMD | MWK | buy | 1717.0236 |
| CMD | MWK | middle | 1734.0118 |
| CMD | MWK | sell | 1751 |
| CNY | MWK | buy | 256.387 |
| CNY | MWK | middle | 258.9237 |
| CNY | MWK | sell | 261.4604 |
| DKK | MWK | buy | 257.912 |
| DKK | MWK | middle | 260.4638 |
| DKK | MWK | sell | 263.0156 |
| ETB | MWK | buy | 10.6404 |
| ETB | MWK | middle | 10.7457 |
| ETB | MWK | sell | 10.851 |
| EUR | MWK | buy | 1985.3567 |
| EUR | MWK | middle | 2004.9997 |
| EUR | MWK | sell | 2024.6428 |
| GBP | MWK | buy | 2340.6552 |
| GBP | MWK | middle | 2363.8136 |
| GBP | MWK | sell | 2386.9719 |
| HKD | MWK | buy | 218.8072 |
| HKD | MWK | middle | 220.972 |
| HKD | MWK | sell | 223.1369 |
| IDR | MWK | buy | 0.096 |
| IDR | MWK | middle | 0.097 |
| IDR | MWK | sell | 0.0979 |
| IEP | MWK | buy | 1204.5062 |
| IEP | MWK | middle | 1216.4236 |
| IEP | MWK | sell | 1228.3409 |
| INR | MWK | buy | 17.7727 |
| INR | MWK | middle | 17.9486 |
| INR | MWK | sell | 18.1244 |
| JPY | MWK | buy | 10.8569 |
| JPY | MWK | middle | 10.9643 |
| JPY | MWK | sell | 11.0718 |
| KES | MWK | buy | 13.2435 |
| KES | MWK | middle | 13.3746 |
| KES | MWK | sell | 13.5056 |
| KRW | MWK | buy | 1.2792 |
| KRW | MWK | middle | 1.2918 |
| KRW | MWK | sell | 1.3045 |
| KWD | MWK | buy | 5572.9427 |
| KWD | MWK | middle | 5628.0812 |
| KWD | MWK | sell | 5683.2197 |

[Full table on the Reserve Bank of Malawi rates page](https://allratestoday.com/central-bank-rates-api/rbm/) · Source: [Official rates published by RBM, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/rbm/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📦 Installation

```bash
npm install rbm-exchange-rate
```

```bash
yarn add rbm-exchange-rate
```

```bash
pnpm add rbm-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/rbm-exchange-rate`](https://www.npmjs.com/package/@allratestoday/rbm-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'rbm-exchange-rate';

const pair = await getRate('USD', 'MWK', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Reserve Bank of Malawi rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('USD', 'MWK', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'rbm',
  name: 'Reserve Bank of Malawi',
  rate_date: '2026-10-08',   // Reserve Bank of Malawi's own publication date
  source: 'USD',
  target: 'MWK',
  rate: 1734.0118,
  rate_type: 'middle',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'rbm-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'rbm',
  name: 'Reserve Bank of Malawi',
  rate_date: '2026-10-08',
  rates: [
    { "base": "USD", "quote": "MWK", "type": "middle", "value": 1734.0118 },
    { "base": "USD", "quote": "MWK", "type": "sell", "value": 1751 },
    { "base": "USD", "quote": "MWK", "type": "buy", "value": 1717.0236 },
    // … the rest of the published table (37 currencies vs MWK)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2016 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'rbm-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'MWK' });
```

**Response:**

```javascript
{
  bank: 'rbm',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'rbm-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'MWK', from: '2026-01-01', to: '2026-10-08' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'rbm',
  source: 'USD',
  target: 'MWK',
  from: '2026-01-01',
  to: '2026-10-08',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-08', rate: 1734.0118, rate_type: 'middle', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Reserve Bank of Malawi currently publishes rates covering **37 currencies** against the MWK (as of the latest table):

🇦🇪 `AED` · 🇦🇷 `ARS` · 🇦🇺 `AUD` · 🇧🇼 `BWP` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇲 `CMD` · 🇨🇳 `CNY` · 🇩🇰 `DKK` · 🇪🇹 `ETB` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇭🇰 `HKD` · 🇮🇩 `IDR` · 🇮🇪 `IEP` · 🇮🇳 `INR` · 🇯🇵 `JPY` · 🇰🇪 `KES` · 🇰🇷 `KRW` · 🇰🇼 `KWD` · 🇱🇰 `LKR` · 🇲🇬 `MGA` · 🇲🇾 `MYR` · 🇲🇿 `MZN` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇵🇭 `PHP` · 🇵🇰 `PKR` · 🇸🇦 `SAR` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇹🇭 `THB` · 🇹🇷 `TRY` · 🇹🇿 `TZS` · 🇺🇸 `USD` · `XDR` · 🇿🇦 `ZAR`

## 🏛️ Source

The Reserve Bank of Malawi publishes daily buying, middle and selling rates for the kwacha against around 38 currencies. Through the kwacha's managed float — including the sharp official devaluations of recent years — the RBM table is the official series Malawian banks, importers and the revenue authority must cite.

- Publisher's own page: [Major rates](https://www.rbm.mw/Statistics/MajorRates/) · [www.rbm.mw](https://www.rbm.mw)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [Reserve Bank of Malawi rates page](https://allratestoday.com/central-bank-rates-api/rbm/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Reserve Bank of Malawi quotes **MWK per 1 unit of foreign currency** (e.g. `base: "USD", quote: "MWK"` means MWK per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the central bank's series a row belongs to (`middle` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Reserve Bank of Malawi rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/rbm/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('rbm')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate rbm ...` command
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If Reserve Bank of Malawi does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via MWK from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Reserve Bank of Malawi |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'rbm-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('rbm-exchange-rate');

getRate('USD', 'MWK', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2016 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRates/central-bank-exchange-rates](https://huggingface.co/datasets/AllRates/central-bank-exchange-rates) — one CSV per institution (`rates/rbm.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- CDN JSON: `https://cdn.jsdelivr.net/gh/AllRates-Today/central-bank-exchange-rates@main/data/rbm/latest.json`

## 🔗 Links

- [Reserve Bank of Malawi rates page](https://allratestoday.com/central-bank-rates-api/rbm/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Package docs on the site](https://allratestoday.com/docs/sdk/rbm-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (free)](https://allratestoday.com/register) · [Pricing](https://allratestoday.com/pricing/)
- [GitHub](https://github.com/AllRates-Today/rbm-exchange-rate)

## 📜 License

MIT
