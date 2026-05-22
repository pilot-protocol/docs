# docs

[![ci](https://github.com/pilot-protocol/docs/actions/workflows/ci.yml/badge.svg)](https://github.com/pilot-protocol/docs/actions/workflows/ci.yml)
[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

Pilot Protocol design documents — the source of truth for what the
protocol does, why it does it that way, and how to operate it.

User-facing documentation (getting started, tutorials, API references)
lives on the website at [pilotprotocol.network](https://pilotprotocol.network).
This repo is the protocol-internal counterpart: deeper specs, IETF
drafts, runbooks, and academic-style writeups.

## Layout

| Path | What it is |
|---|---|
| `SPEC.md` | Canonical protocol spec — addresses, frame format, layered architecture. |
| `SPEC-compat-mode.md` | Compat mode (TLS/443) layered on top of the native UDP path. |
| `SPEC-skillinject-openclaw-per-prompt.md` | Spec for the skillinject plugin's per-prompt injection. |
| `RUNBOOK-pilot-ca.md` | Root-CA ceremony procedure — key generation, rotation, audit. |
| `RUNBOOK-compat-443-only.md` | Operating a daemon when only port 443 is reachable. |
| `INVESTIGATION-cloudflare-workers.md` | Cloudflare Workers viability writeup. |
| `ANALYSIS-per-prompt-injection.md` | Threat-model analysis of the per-prompt injection path. |
| `AGENT-APPS.md` | Notes on the agent-apps model and pilot-store grants. |
| `WHITEPAPER.{tex,pdf}` | The protocol whitepaper. |
| `enterprise-readiness-report.{tex,pdf}` | Enterprise audit catalog. |
| `ietf/` | IETF draft text + Makefile. |
| `research/comparison/` | Comparison paper vs. other overlay protocols. |
| `research/social-structures/` | Trust-network social-structure paper. |
| `media/` | Diagrams and screencasts referenced by other docs. |

## Building TeX → PDF

Each `.tex` is built with `pdflatex` (run twice for cross-references).
The `ietf/` drafts use `kramdown-rfc` via the Makefile there.

```bash
cd ietf && make
```

## License

AGPL-3.0-or-later. See [LICENSE](LICENSE).
