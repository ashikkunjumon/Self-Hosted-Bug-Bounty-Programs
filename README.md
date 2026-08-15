# Self-Hosted Bug Bounty & Disclosure Programs

Vulnerability disclosure and bug bounty programs published by the
organisations that run them, discovered from their own policy pages.

## 📊 Statistics

| Metric | Count |
|---|---|
| **Total Programs** | 7,530 |
| **Self-hosted** | 6,519 |
| **Platform-hosted** | 1,011 |
| **Active** | 5,868 |
| **Offering a reward** | 2,148 |
| **Stating safe harbour** | 714 |
| **Countries** | 55 |

*Last Updated: August 15, 2026 at 14:24 UTC*

## 📁 Browse

| Category | Description |
|---|---|
| [Self-hosted](self-hosted/) | Programs run by the organisation itself |
| [Platform-hosted](platform/) | Programs run through a disclosure platform |

Each section indexes its programs by country.

## 📄 Data

- `programs.json` — every program, structured
- `programs.txt` — flat domain and policy URL list

## About

A directory of organisations that accept vulnerability reports, built from what
those organisations publish about themselves — their `/.well-known/security.txt`
and their disclosure policy pages.

Most of it is **self-hosted**: 6,519 of 7,530 programs run their own
disclosure process rather than sitting on a platform. Those are the hard ones to
find. Programs on HackerOne, Bugcrowd and Intigriti are already indexed
everywhere; a company that quietly published a security.txt is not.

### What the fields mean

| Field | Values |
|---|---|
| `reward` | `monetary`, `swag`, `recognition`, or `none` — what the policy offers, not what it pays |
| `safe_harbour` | `stated` only when the policy says so explicitly. `not_stated` and `unknown` both mean **assume none** |
| `status` | `active`, `expired` (the policy set an expiry that has passed), `retired` |
| `live` | whether the domain still resolves and serves |
| `policy_dead` | the policy URL was published but no longer loads |

Only 714 of 7,530 programs state safe harbour explicitly. That is the
single most important column here, and the number is low.

### Before you test anything

**This directory is an index, not permission.** A security.txt means an
organisation will accept a report; it does not define scope, and it is not
authorisation to test. Read the program's own policy first — it is linked on
every row — and stay inside what it allows. Where a policy is missing, expired
or dead, treat that as no permission at all.

### Freshness and accuracy

Rebuilt daily, and committed only when something actually changed. Every record
carries `first_seen` and `last_seen`. Policies move and lapse, so a row is
evidence of what was published when it was last checked, nothing stronger.

Country is derived and often absent — `global` is the largest bucket, not a
finding about where these organisations are.

### Removal

Open an issue and the domain is excluded from the next build.
