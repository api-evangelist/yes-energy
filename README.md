# Yes Energy (yes-energy)

Yes Energy is a Boulder, Colorado power market data company serving the North American wholesale electricity markets — the seven ISOs and RTOs (ERCOT, PJM, MISO, CAISO, SPP, ISO-NE, NYISO) plus Canadian and Western markets. It aggregates, cleans, and enriches nodal locational marginal prices, FTR auction results, transmission and generation outages, real-time generation and flow telemetry, constraints, load, weather, and fuels data, and sells it through DataSignals (a REST API), DataSignals Cloud (Snowflake Secure Data Sharing), DataSignals Lake (bulk load into a customer warehouse), the PowerSignals and QuickSignals analyst front ends, EnCompass modeling, Live Power telemetry, Infrastructure Insights, Position Management, and bid-to-bill Submission Services. It sits in the private, commercial layer of the energy value chain: it does not generate, distribute, or retail electricity and it holds no consumer relationship — it resells and enriches public ISO/RTO market data to traders, IPPs, utilities, and asset developers. Its API posture is honestly closed: the DataSignals REST API is real and confirmed live at `https://services.yesenergy.com/PS/rest/`, but it answers every anonymous request with HTTP 401 and `WWW-Authenticate: Basic`, and even the product documentation (help.yesenergy.com) redirects through services.yesenergy.com to a customer login. No public developer portal, no self-serve signup, no machine-readable specification, and no free tier are published. Home market is the United States. There is no consumer energy data mandate that applies to Yes Energy — it is not a utility, retailer, or metering agent, so Green Button, ESPI, and the Consumer Data Right are all out of scope — and while the underlying ISO/RTO market data is publicly available at the source, Yes Energy itself publishes none of it openly.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/yes-energy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/yes-energy/refs/heads/main/apis.yml)

## Tags

- Energy
- United States
- Energy Markets
- Electricity
- Grid
- Market Data
- Wholesale Power
- ISO RTO
- Renewables
- Trading

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

### Yes Energy DataSignals API

DataSignals is Yes Energy's REST API for automated access to its North American wholesale power market data — nodal prices, transmission, generation, outages, constraints, weather, and fuels — covering real-time and 15+ years of history, with time-series and object endpoints intended for Excel, Python, R, and system integration. The service host is live and confirmed at `https://services.yesenergy.com/PS/rest/`, which returns HTTP 401 with `WWW-Authenticate: Basic realm="Realm"` to anonymous callers; HTTP Basic credentials are issued only to paying subscribers. The endpoint reference and code examples live in the customer knowledge base at help.yesenergy.com, which 302-redirects to the services.yesenergy.com customer login, so no endpoint list, no scopes, and no machine-readable specification could be verified anonymously.

- **Human URL:** [https://www.yesenergy.com/products/datasignals](https://www.yesenergy.com/products/datasignals)
- **Base URL:** `https://services.yesenergy.com/PS/rest/`

#### Tags

- Energy Markets
- Market Data
- Electricity
- Wholesale Power
- Time Series

#### Properties

- [Documentation](https://www.yesenergy.com/products/datasignals)
- [Documentation](https://www.yesenergy.com/datasignals-20)
- [Documentation](https://www.yesenergy.com/solutions/it-data-scientist)
- [Authentication](https://services.yesenergy.com/PS/rest/)

## Energy Data Posture

| Dimension | Finding |
| --- | --- |
| Home market | United States |
| Mandate regime | none |
| Mandate status | not-applicable |
| Data standard | no standard reference found (proprietary REST under `/PS/rest/`) |
| Consumer data API | No — holds no retail customer usage or billing data |
| Market data open | No — sells wholesale market data that is public at the ISO/RTO source |
| Access gate | customer-account-required (sales-led subscription, then HTTP Basic credentials) |
| Auth model | HTTP Basic (`WWW-Authenticate: Basic realm="Realm"`); no OIDC discovery document served |

Yes Energy is not a utility, retailer, distribution network operator, or metering agent, so Green Button / ESPI, the Australian Consumer Data Right, and the Ontario Green Button regulation do not apply to it. No compliance claim was made and none needed downgrading — this is a genuine `none`.

## Common Properties

- [Website](https://www.yesenergy.com/)
- [Products](https://www.yesenergy.com/products)
- [Support](https://www.yesenergy.com/support)
- [Documentation](https://help.yesenergy.com/) — customer login required
- [Sign Up](https://www.yesenergy.com/demo) — demo request, not self-serve
- [Contact](https://www.yesenergy.com/contact)
- [Pricing](https://www.yesenergy.com/packages)
- [Status Page](https://status.yesenergy.com/)
- [Blog](https://www.yesenergy.com/blog)
- [Blog RSS](https://www.yesenergy.com/blog/rss.xml)
- [News](https://www.yesenergy.com/news)
- [About](https://www.yesenergy.com/about)
- [LinkedIn](https://www.linkedin.com/company/yes-energy/)
- [Partners](https://www.yesenergy.com/partners/snowflake)
- [Data Marketplace](https://app.snowflake.com/marketplace/providers/GZSOZ71OEK/Yes%20Energy)

## Maintainers

- Kin Lane — kin@apievangelist.com
