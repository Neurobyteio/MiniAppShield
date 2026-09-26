# MiniAppShield Evidence Model

MiniAppShield is built around a simple principle:

**observations should be separated from conclusions.**

Telegram Mini App analysis can easily become misleading when technical signals are treated as proof of ownership, fraud, advertising delivery, traffic quality, or malicious behavior.

The MiniAppShield Evidence Model is designed to reduce that problem.

It organizes technical observations into independent evidence layers and keeps the language conservative when the available data does not support a stronger conclusion.

Website: https://appshield.app/

---

## Why an Evidence Model Is Necessary

A Telegram Mini App can produce many kinds of technical signals during runtime.

Examples include:

- network requests
- JavaScript assets
- backend domains
- Telegram WebView events
- advertising SDKs
- publisher identifiers
- placement identifiers
- wallet integrations
- analytics endpoints
- runtime errors
- infrastructure artifacts

The existence of a signal does not automatically prove a broader claim.

For example:

**An advertising SDK does not prove that an ad was delivered.**

**A shared domain does not prove common ownership.**

**A runtime error does not prove malicious behavior.**

**A Telegram MAU value does not prove traffic quality.**

MiniAppShield therefore separates evidence collection from interpretation.

---

## Core Evidence Principles

### 1. Observed Means Observed

MiniAppShield reports what was observed during the available audit or historical observation.

It does not automatically generalize beyond that observation.

Preferred language:

> No active advertising delivery was observed during the captured session.

Not:

> This Mini App does not serve ads.

The first statement describes evidence.

The second statement makes a broader claim that may not be supported.

---

### 2. Absence of Evidence Is Not Evidence of Permanent Absence

A scanner may not observe a feature during one session.

That does not prove the feature never appears.

Examples:

- no ad was observed during the audit
- no wallet interaction was observed
- no exact technical relationship was observed
- no destination change was observed

These statements describe the current evidence scope.

They do not establish permanent absence.

---

## Advertising Evidence

Advertising analysis is divided into separate evidence stages.

### Advertising Technology

This can include:

- advertising SDKs
- scripts
- configuration
- publisher identifiers
- placement identifiers
- advertising endpoints

Technology presence alone does not establish active delivery.

---

### Advertising Runtime Activity

Runtime evidence may show that advertising-related code or endpoints were actively used.

This provides stronger evidence than static technology detection.

However:

**advertising runtime activity does not automatically prove an impression.**

---

### Creative Delivery

Creative-related evidence may indicate that advertising content was delivered or referenced during runtime.

This is stronger than simply detecting an advertising SDK.

---

### Impression Evidence

Impression-related evidence represents a later stage in the advertising lifecycle.

MiniAppShield keeps these stages separate to avoid overstating advertising activity.

---

## Advertising Evidence Hierarchy

A simplified evidence hierarchy can be represented as:

```text
Advertising component detected
        ↓
Advertising runtime activity observed
        ↓
Creative delivery evidence observed
        ↓
Impression-related evidence observed
