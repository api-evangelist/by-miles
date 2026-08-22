# By Miles (by-miles)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
