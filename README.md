# By Miles (by-miles)

By Miles is a London-based insurtech that pioneered pay-by-mile motor insurance in the United Kingdom, founded in 2016 for low-mileage drivers who cover under roughly 7,000 miles a year. Its single line of business is UK private motor (personal lines property and casualty), priced as a fixed annual premium covering the parked car plus a per-mile charge for the distance actually driven. Mileage is measured either by the OBD-II "Miles Tracker" telematics dongle or, on its "connect" trackerless policies, by pulling odometer data directly from the manufacturer's connected-car platform after the driver links a Tesla, Ford or Mercedes-Benz account.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/by-miles/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/by-miles/refs/heads/main/apis.yml)

## Tags

- Insurance
- United Kingdom
- Insurtech
- Property and Casualty
- Motor Insurance
- Usage Based Insurance
- Telematics
- Connected Car
- Direct to Consumer
- Open Banking
- No Public API

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None.** By Miles publishes no public, self-serve API.

Every first-party developer hostname was probed on 2026-07-25.
`developer.bymiles.co.uk` and `developers.bymiles.co.uk` do not resolve at all.
`/developers`, `/developer` and `/integrations` return 404 and `/api` returns 502.
The two hosts that do answer are both closed: `api.bymiles.co.uk` is an AWS API
Gateway returning `403 {"message":"Forbidden"}` — the private backend for the By
Miles consumer mobile app — and `docs.bymiles.co.uk` is a CloudFront distribution
behind signed URLs (`MissingKey / Missing Key-Pair-Id`) used to deliver policy
documents, not API reference docs. The only live "partner" surface,
[https://www.bymiles.co.uk/partners](https://www.bymiles.co.uk/partners) (HTTP 200),
is a press and marketing page whose entire integration mechanism is the email
address `partnerships@bymiles.co.uk`.

No OpenAPI, Swagger, AsyncAPI, GraphQL SDL, `.proto`, Postman collection or webhook
catalogue exists, so this repository has no `openapi/` directory.

### An API consumer, not an API producer

The honest reading of By Miles is that it was a sophisticated **consumer** of other
people's APIs:

- **UK Open Banking.** In January 2020 By Miles became the first UK insurtech
  directly authorised by the Financial Conduct Authority under the Open Banking /
  PSD2 regime, holding both AISP (account information) and PISP (payment initiation)
  permissions, in order to consume bank APIs for payment collection, affordability
  and identity verification. It is a TPP on those rails, not a provider of them.
- **OEM connected-car APIs.** Trackerless "connect" policies read odometer data
  after the customer links a Tesla, Ford or Mercedes-Benz account. By Miles is
  featured as a customer story on
  [developer.mercedes-benz.com](https://developer.mercedes-benz.com/success-stories/by_miles)
  — the OEM's developer portal, not one of its own.

Neither relationship is exposed outward. Nothing By Miles consumes is re-published
as a documented API for third parties.

### ACORD posture

**No ACORD reference found.** Searches of the By Miles website, its Zendesk help
centre index and the open web for ACORD, AL3, ACORD XML, ACORD certified and NGDS
returned nothing. This is expected for a UK direct-to-consumer motor insurtech:
ACORD AL3 and the IVANS agency-download rails are a North American agency-management
phenomenon, and the UK's market-wide data plumbing is the London Market's Blueprint
Two / PPL / Whitespace stack, which serves brokers and syndicates in the subscription
market. By Miles sat outside both.

### Quote / bind / issue / FNOL

None of the four insurance verbs is exposed as an API. Quoting and binding were a
first-party web and app funnel; policy issue and servicing run in the mobile app and
web dashboard against the private `api.bymiles.co.uk` backend; first notice of loss
is by phone and in-app 24-hour claims support. The audience was consumer-facing only
— there is no agent-facing or partner-facing API tier.

### Corporate status

By Miles was acquired by **Direct Line Group in April 2023**. Following Aviva's
acquisition of Direct Line Group, the brand is being wound down: new-business
quoting has stopped and renewal quotes to existing customers ceased **6 January
2026**. Existing policies run to expiry.

### Security posture

Despite publishing no API, By Miles does publish a real **responsible-disclosure
programme**: reports go to `vulnerability@bymiles.co.uk`, a PGP public key is
published for encrypted reports, the response target is 5 days, and confirmed
first reporters get swag, a place in the Hall of Fame and — for severe findings
— a discretionary cash award. There is no HackerOne/Bugcrowd/Intigriti listing.
Its ISMS policy (v2.1, 20 May 2026) states **alignment to the scope of ISO
27001** — alignment, not a published certificate — alongside UK GDPR and FCA
commitments. By Miles Ltd is FCA-authorised under **Firm Reference Number
773046**. Notably no RFC 9116 `security.txt` is served, even though all the
content one would point at is already published.

## Artifacts in this repository

- `security/by-miles-vulnerability-disclosure.yml` — the responsible-disclosure programme.
- `security/by-miles-domain-security.yml` — TLS/HSTS/DNSSEC/CAA/SPF/DMARC probes across all four live hosts.
- `conformance/by-miles-conformance.yml` — regulatory and standards posture, producer vs consumer role.
- `lifecycle/by-miles-lifecycle.yml` — company lifecycle and the dated wind-down (no API lifecycle exists).
- `well-known/by-miles-well-known.yml` — recorded absence of every `/.well-known/` document.
- `llms/by-miles-llms.txt` — agent-facing summary, generated from this record.

## Links

- [Website](https://www.bymiles.co.uk/)
- [Blog](https://www.bymiles.co.uk/insure/magazine/)
- [Support](https://help.bymiles.co.uk/hc/en-us)
- [Login](https://dashboard.bymiles.co.uk/account/login)
- [Partners](https://www.bymiles.co.uk/partners)
- [Security vulnerability reporting policy](https://www.bymiles.co.uk/security-vulnerability-reporting-policy)
- [Information security policy](https://www.bymiles.co.uk/information-security)
- [Terms of Business](https://www.bymiles.co.uk/terms-of-business)
- [Terms of Use](https://www.bymiles.co.uk/terms)
- [Privacy Policy](https://www.bymiles.co.uk/privacy-policy)
- [Press](https://www.bymiles.co.uk/press)
- [GitHub Organization](https://github.com/by-miles)
- [LinkedIn](https://www.linkedin.com/company/bymiles)
- [Twitter](https://www.twitter.com/bymiles)
- [Facebook](https://www.facebook.com/gobymiles)
