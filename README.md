# Self-Hosted Bug Bounty & Disclosure Programs

**A list of 7,586 bug bounty and vulnerability disclosure programs
run by the organisations themselves — not on HackerOne, Bugcrowd or Intigriti.**

Built from `/.well-known/security.txt` files and published disclosure policies,
indexed by country, and rebuilt daily. 6,570 of these are
self-hosted VDP and bug bounty programs, which is the half that platform
directories do not list.

## 📊 Statistics

| Metric | Count |
|---|---|
| **Total Programs** | 7,586 |
| **Self-hosted** | 6,570 |
| **Platform-hosted** | 1,016 |
| **Active** | 5,777 |
| **Offering a reward** | 2,160 |
| **Stating safe harbour** | 734 |
| **Countries** | 55 |

*Last Updated: August 19, 2026 at 08:01 UTC*

## Find bug bounty programs by country

| Category | Description |
|---|---|
| [Self-hosted](self-hosted/) | Programs run by the organisation itself |
| [Platform-hosted](platform/) | Programs run through a disclosure platform |

Each section indexes its programs by country, so you can scope a hunt to a
region or a jurisdiction.

## Which programs offer a reward, and which state safe harbour

Every row records whether the policy offers a reward — `monetary`, `swag` or
`recognition` — and whether it explicitly states safe harbour. 2,160
programs offer some reward; only 734 state safe harbour outright, which
is the number worth checking before you test anything.

## security.txt and disclosure policy URLs

`programs.txt` gives a domain and a URL per line: the disclosure policy where
one is published, and the `/.well-known/security.txt` file otherwise. Every one
of the 7,586 entries carries a URL, so it loads straight into a
recon pipeline.

## Data files

- `programs.json` — every program, structured
- `programs.txt` — flat domain and policy URL list

## About

A directory of organisations that accept vulnerability reports, built from what
those organisations publish about themselves — their `/.well-known/security.txt`
and their disclosure policy pages.

Most of it is **self-hosted**: 6,570 of 7,586 programs run their own
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

Only 734 of 7,586 programs state safe harbour explicitly. That is the
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

## Related projects

- [HackerOne Disclosed Reports Payloads](https://github.com/ashikkunjumon/HackerOne-Disclosed-Reports-Payloads)
  — real payloads extracted from disclosed HackerOne reports, by vulnerability class
- [Bug Bounty Dorks Automation](https://github.com/ashikkunjumon/Bug-Bounty-Dorks-Automation)
  — search-engine dorks for recon and for finding programs to test
