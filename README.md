<img src="assets/channels4_profile.jpg" width="100%"/>

## Hi there
- 🙋‍♂️ I'm free to give a few hours a week to volunteer (for something meaningful)
- 🌎 I freelance, travel (currently SEA) and manage a few startups
- 🥋 Either working or working out


## What I do:
### Freelancing
<img width="200px" src="https://pbs.twimg.com/media/FQgl89aXMAAreT7?format=jpg&name=small" />
I work on projects of all lengths and levels of complexity: e-commerce platforms, SaaS, PaaS, automation scripts and more. I like a high degree of novelty, so I keep picking different, contrasting projects. You'll find the languages and tools I use at the end of the page.

### Devancer B.V.
Stage: **Live and growing.** In production, shipping weekly (v1.113).

Devancer brings e-learning into one place: a searchable library of courses, books and tutorials from across the web, user-written study guides, and learning paths that put resources in order.

What's there today:
- 📚 **Library from 140+ platforms.** Each source has its own extraction plugin. Course data is normalised, de-duplicated across platforms (one canonical page per course) and enriched with descriptions, tables of contents, levels and prices in several currencies.
- 📝 **Study guides.** Readable as full pages on the site or downloaded as watermarked PDFs.
- 🧭 **Learning paths.** Ordered resources plus actions. Any finished path can be copied and adapted.
- 🏆 **Rewards and reviews.** A rewards engine for contributors. Reviews feed the recommendations.
- 🌍 **Multilingual.** Localised pages, plus latinisation of Chinese, Japanese, Thai and Arabic creator names.

Tools: TypeScript, NestJS, GraphQL, PostgreSQL (materialised views for facets), pg-boss, Next.js, Docker, Cloudflare, LLM-based enrichment, OpenTelemetry/Jaeger.

### Credit Marketplace (FinTech, Kazakhstan)
Stage: **Built, waiting for a license.** The MVP is ready and launch depends on the regulatory license.

A neutral credit-visibility and loan-matching platform on web, Android and iOS. Kazakhstan comes first, then other markets in gated phases. It helps people see their whole debt picture and find better loans:
- 🧮 **Debt optimizer and payoff simulator.** Users can import an on-device credit report and get the best repayment order.
- 📅 **Payment calendar and rate-watch**
- 🏦 **Loan marketplace.** Planned next: credit-bureau and eGov integration with consent and an audit trail, prequalification ("approval odds") and direct bank APIs.
- Shared loan math on every surface (schedules, effective annual rate, debt-to-income, affordability) and versioned statutory parameters with effective dates.
- Built for compliance from day one: per-jurisdiction data cells with residency guards, PII-safe logging, kk/ru/en legal texts checked for completeness in CI.

Tools: TypeScript, NestJS + Fastify, Next.js, Expo/React Native, PostgreSQL, Redis, Turborepo, OpenTelemetry, OpenTofu.

### Web3 MVPs
Two DeFi protocols on **Base Sepolia**. They run on testnet with play money only and share a faucet token. The protocols are done; the apps, indexers and bots are next.

**🔮 Forecastr: a self-resolving prediction market**
Binary, multi-outcome and scalar markets traded against an automated market maker.

| Challenge | Solution |
|---|---|
| New markets have nobody to trade against | An LMSR market maker always quotes a price, and its loss is capped by the liquidity parameter *b* |
| `exp`/`ln` on-chain without overflow or rounding exploits | A fixed-point LMSR library, plus price-impact quotes and slippage limits on every trade |
| Whoever runs the market shouldn't decide who wins | Positions live in Gnosis-style conditional tokens (ERC-1155) that only the market's resolver can settle |
| Resolving user-created markets fairly | An optimistic resolver: bonded proposal, dispute, then a staked vote. Markets that can't be resolved refund at the last price |

**⚓ Keel: isolated lending markets plus a risk lab**
Supply USDC, borrow against WETH/cbBTC, and stress-test the parameters against historical crashes.

| Challenge | Solution |
|---|---|
| One bad or manipulated oracle can drain a lending protocol | Two feeds (Chainlink + Pyth): the **lower** price for borrows, the **higher** for liquidations. Borrowing is blocked if either feed is down |
| A crash in one collateral spreading bad debt to others | Isolated markets, each with its own oracle, rate curve and risk parameters (covered by a test) |
| Liquidations need capital that keepers may not have | A liquidator that runs on an ERC-3156 flash loan: borrow, liquidate, sell, repay in one transaction |
| Admin changes as an attack vector | A 1-day timelock on parameter and oracle changes |
| Picking LTVs and bonuses that survive a crash | The risk lab replays historical crashes against the protocol and sweeps the parameters |

Tools: Solidity, Foundry, Chainlink, Pyth, ERC-1155/2612/3156, Python (simulations), TypeScript, Next.js, viem.


### Languages and Tools:
CSS: CSS3, Tailwind CSS, Material UI, Bootstrap, Semantic UI, jQuery

Frontend: HTML5, JavaScript, TypeScript, React, Next.js, Angular, Jinja2

Backend: Node.js, NestJS, Express, Fastify, GraphQL, Python, Flask, Django, Java Spring

Mobile: React Native, Expo

Web3: Solidity, Foundry, Chainlink, Pyth, viem

Databases: PostgreSQL, Redis, MySQL, MongoDB, Firebase, SQLite

Other tools: Docker, Git, AWS, Cloudflare, OpenTofu, Turborepo, Jira

Data scraping: Selenium, BeautifulSoup, Cheerio

Data analytics: Google Colab, Matplotlib, Pandas, Plotly, Seaborn, IBM SPSS, Jupyter

Data visualization: Tableau


<img src="https://strokingfire.files.wordpress.com/2020/12/this-cruel-design-2-this-mortal-coil-book-review-pic-03-by-casey-carlisle.gif" />
