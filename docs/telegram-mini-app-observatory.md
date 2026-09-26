# Telegram Mini App Observatory

MiniAppShield is building a structured historical intelligence layer for the Telegram Mini App ecosystem.

The goal is not to maintain the largest possible list of Telegram usernames.

The goal is to build a clean, normalized, evidence-based, historical dataset of real Telegram Mini Apps and their observable technical behavior.

Website: https://appshield.app/

---

## What Is the Telegram Mini App Observatory?

The Telegram Mini App Observatory is a long-term intelligence dataset designed to combine:

- Mini App discovery
- candidate normalization
- duplicate removal
- Mini App validation
- runtime observations
- infrastructure intelligence
- advertising intelligence
- technical relationships
- advertising relationships
- audience observations
- historical monitoring
- change detection

A one-time scan provides a snapshot.

An Observatory provides context over time.

---

## Why an Observatory Is Needed

Telegram Mini Apps are dynamic systems.

Their behavior can change after launch.

A Mini App may:

- move to a new WebView destination
- change backend infrastructure
- add or remove SDKs
- change advertising integrations
- contact new domains
- modify runtime behavior
- introduce new wallet or blockchain functionality
- change technical relationships with other applications
- change Telegram audience metadata

A single audit cannot show these transitions.

Historical observations can.

---

## From Scanner to Intelligence Layer

A scanner answers:

> What was observed right now?

An Observatory can also answer:

> What changed?

> When did it change?

> Has this Mini App been observed before?

> Did its destination change?

> Did its advertising stack change?

> Did new technical relationships appear?

> Is the current observation consistent with previous observations?

This transition from point-in-time scanning to historical intelligence is a central part of MiniAppShield.

---

## Discovery

The first step is finding Telegram Mini Apps.

MiniAppShield uses public-source discovery to identify potential applications from multiple sources.

Candidate discovery is intentionally separated from final validation.

A public catalog entry does not automatically prove that a Telegram object is a currently operational Mini App.

The discovery pipeline can include:

- public Telegram Mini App directories
- public catalog metadata
- Telegram-related public sources
- previously observed candidates
- structured external references

Candidates are normalized before further processing.

---

## Candidate Normalization

Different sources may refer to the same Telegram object in different forms.

Examples:

```text
@ExampleBot
examplebot
https://t.me/examplebot
t.me/examplebot


These should not become four independent records.
Normalization helps reduce:
- duplicate usernames
- aliases
- inconsistent capitalization
- repeated catalog entries
- malformed candidates
This is important because raw catalog size is not the same thing as clean dataset size.
Bots Are Not Automatically Mini Apps
Telegram contains many ordinary bots that do not expose a Mini App runtime.
Therefore:
Telegram bot ≠ Telegram Mini App
The Observatory separates different object types and validation states.
A candidate can exist in public sources without being promoted to a confirmed Mini App.
Positive Mini App evidence is required before treating it as part of the confirmed Mini App dataset.
Validation
Validation determines whether a candidate has sufficient evidence to be treated as a Telegram Mini App.
Potential evidence can include:
- Telegram Mini App metadata
- Main App configuration
- WebView destination
- explicit Mini App launch references
- observable runtime behavior
- trusted public Mini App classification
Validation should be performed conservatively.
The system should not convert weak catalog evidence into strong runtime claims.
Runtime Observation
Confirmed Mini Apps can be observed in a controlled runtime environment.
Runtime analysis may collect structured signals such as:
- initialization state
- HTTP status
- rendered DOM
- Telegram WebView bridge activity
- network requests
- contacted domains
- JavaScript assets
- interactive elements
- runtime failures
- page errors
- console errors
- advertising activity
These observations become structured intelligence rather than raw browsing history.
Historical Monitoring
Repeated observations allow the Observatory to compare a Mini App against its own history.
Historical monitoring can reveal:
- destination changes
- runtime changes
- infrastructure changes
- advertising stack changes
- SDK changes
- relationship changes
- audience metadata changes
This creates a timeline of observable technical behavior.
Destination Intelligence
A Mini App's destination can be commercially and technically important.
If a Mini App changes from:
example-a.com

to:
example-b.com

the Observatory can record that transition.
A destination change does not independently prove malicious behavior.
It is simply a meaningful historical event that may deserve review.
Advertising Stack Intelligence
Advertising integrations can also change over time.
For example:
Observation A:
No advertising component observed

Observation B:
Advertising SDK detected

Observation C:
Advertising runtime activity observed

These are different states.
Historical tracking can show when the advertising profile changed.
Infrastructure Intelligence
A Mini App's runtime may interact with multiple infrastructure components.
Examples include:
- backend APIs
- content delivery networks
- analytics platforms
- advertising endpoints
- authentication services
- wallet infrastructure
- blockchain APIs
- telemetry services
- third-party SDKs
The Observatory can preserve structural observations that are useful for later comparison.
Technical Relationship Mapping
Historical technical artifacts can reveal relationships between Mini Apps.
Potential relationship signals may include:
- exact application-specific artifacts
- exact infrastructure identifiers
- exact technical fingerprints
- shared backend characteristics
- repeated configuration patterns
MiniAppShield treats technical relationships as evidence of technical overlap.
It does not automatically convert them into ownership attribution.
Advertising Relationship Mapping
Advertising identity can also connect multiple Mini Apps.
Examples of potentially relevant evidence include:
- exact publisher identifiers
- exact placement identifiers
- shared advertising configuration
- shared observed advertising infrastructure
These relationships can help ad networks, advertisers, and analysts understand connected advertising contexts.
Audience Intelligence
Where Telegram exposes audience metadata, the Observatory can preserve those observations over time.
This can support analysis of:
- current monthly active users
- previous audience observations
- increases
- decreases
- periods without sufficient history
Audience intelligence remains separate from traffic quality.
Audience size does not prove audience authenticity or advertising performance.
Observation Depth
Not every Mini App has the same historical depth.
A newly discovered Mini App may have only one deep observation.
An established monitored Mini App may have many.
Observation depth can be described independently.
For example:
Single observation
Repeated observation
Established observation history

This helps analysts understand how much historical evidence exists behind a conclusion.
Change Intelligence
The Observatory is designed to detect meaningful differences between comparable observations.
Potential change categories include:
- destination
- advertising stack
- SDK composition
- infrastructure
- runtime behavior
- audience metadata
- technical relationships
The important distinction is:
change observed ≠ reason for change known
MiniAppShield records the observable transition without inventing a motive.
Exact Evidence vs Generic Similarity
The Observatory distinguishes between exact and generic signals.
Generic examples:
- React
- Cloudflare
- Google Analytics
- Telegram Web Apps SDK
- common CDN providers
These technologies are widely used.
They should not independently establish strong relationships.
More specific application-level evidence can support stronger relationship statements.
Structured Intelligence vs Raw Data
The Observatory is designed around structured intelligence rather than indefinite raw-data retention.
A useful model is:
Structured Observatory Facts
Long-term information such as:
- normalized identities
- historical statuses
- relationships
- change records
- runtime summaries
- audience observations
Evidence Supporting Findings
Evidence required to explain or support important observations.
Temporary Raw Material
Large raw artifacts such as:
- HTML
- response bodies
- temporary runtime captures
- other high-volume raw data
Raw material does not need to be retained forever if it does not support a meaningful finding.
Why Clean Data Matters More Than Raw Volume
A public directory may contain thousands of entries.
That does not necessarily mean it contains thousands of:
- unique Mini Apps
- operational Mini Apps
- currently active Mini Apps
- deeply analyzed Mini Apps
Catalog datasets can include:
- ordinary bots
- channels
- aliases
- duplicates
- inactive applications
- malformed entries
- outdated listings
For MiniAppShield, dataset quality matters more than headline size.
A smaller clean historical dataset can be more useful than a larger unverified directory.
Observatory Data Quality Principles
The MiniAppShield Observatory follows several principles:
Candidate ≠ confirmed Mini App

Bot ≠ Mini App

Catalog presence ≠ runtime proof

One observation ≠ historical consistency

Shared infrastructure ≠ common ownership

SDK detected ≠ ad delivery

No observed activity ≠ permanent absence

These rules help keep classifications explainable.
Monitoring Strategy
Not every Mini App needs to be scanned continuously.
Monitoring can be prioritized based on factors such as:
- commercial relevance
- previous change activity
- advertising activity
- technical relationships
- new discovery status
- historical importance
- client interest
This allows historical intelligence to grow without treating every application identically.
Commercial Use Cases
Ad Networks
An ad network may use historical Mini App intelligence to review sources before accepting or expanding traffic relationships.
Advertisers
Advertisers may want to know whether a Mini App has materially changed since a previous review.
Agencies
Performance agencies can use current and historical context before allocating budget.
Security Teams
Security teams can investigate technical relationships, infrastructure, runtime behavior, and changes.
Web3 and TON Teams
Telegram Mini Apps are widely used across gaming, wallets, blockchain products, and Web3 services.
Historical technical intelligence can provide additional context around these applications.
Due-Diligence Teams
Historical technical observations can complement financial, legal, product, and operational due diligence.
Example: Why History Matters
Imagine a Mini App is observed in January.
Destination: app-a.example
Advertising technology: not observed
Runtime: stable

It is observed again in March.
Destination: app-a.example
Advertising SDK: observed
New analytics endpoint: observed

It is observed again in June.
Destination: app-b.example
Advertising runtime activity: observed
New exact technical relationship: observed

No single event automatically establishes wrongdoing.
But the historical sequence provides substantially more context than one scan.
That is the purpose of the Observatory.
What the Observatory Is Not
The MiniAppShield Observatory is not intended to be:
- a list of accusations
- an ownership attribution database
- a fraud blacklist
- a substitute for legal investigation
- an automatic campaign approval system
- a traffic-quality certification service
It is a structured technical intelligence layer.
The goal is to improve the evidence available to human reviewers.
Long-Term Direction
MiniAppShield is evolving from a point-in-time Telegram Mini App scanner into a historical intelligence platform.
The long-term direction includes:
- broader public-source discovery
- cleaner Mini App validation
- deeper historical monitoring
- stronger technical relationship mapping
- advertising relationship intelligence
- runtime change detection
- infrastructure change detection
- audience history
- comparative intelligence
The value of the Observatory increases as historical depth grows.
Technical history cannot be recreated retrospectively if it was never observed.
Current MiniAppShield Focus
Current areas include:
- Telegram Mini App discovery
- Full Audit
- runtime intelligence
- advertising intelligence
- infrastructure intelligence
- technical relationships
- advertising relationships
- change intelligence
- historical monitoring
- Telegram audience observations
Learn More
MiniAppShield Website
https://appshield.app/
Telegram
https://t.me/MiniAppShield
Telegram Bot
https://t.me/MiniAppShield_bot
Related Research Topics
- Telegram Mini App Observatory
- Telegram Mini App intelligence
- Telegram Mini App database
- Telegram Mini App monitoring
- Telegram Mini App discovery
- Telegram Mini App audit
- Telegram Mini App security
- Telegram Mini App advertising
- Telegram Mini App runtime analysis
- Telegram Mini App infrastructure
- Telegram Mini App relationships
- Telegram WebView analysis
- Telegram ad-tech
- TON Mini Apps
- Web3 Mini Apps
- Mini App due diligence

Для коммита:

**Commit message:**  
`Add Telegram Mini App Observatory documentation`

После этого у тебя уже будет хороший публичный кластер:

```text
README.md
docs/telegram-mini-app-audit.md
docs/evidence-model.md
docs/telegram-mini-app-observatory.md
