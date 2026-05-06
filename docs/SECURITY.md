# Security Policy

PolyGuard is a security tool — we hold ourselves to a high standard. If you find a vulnerability in PolyGuard itself, please help us fix it responsibly.

---

## Supported Versions

| Version         | Supported        |
| --------------- | ---------------- |
| `main` (latest) | ✅ Active        |
| `0.1.x`         | ✅ Active        |
| Older releases  | ❌ Not supported |

---

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security vulnerabilities.**

Report security issues by emailing: **security@quantumlogics.dev**

Include as much of the following as possible:

- A description of the vulnerability and its potential impact
- The affected component (e.g. `src/inference/api.py`, `rules_engine/`, Docker setup)
- Steps to reproduce or a minimal proof-of-concept
- The vulnerability type and relevant CWE if known (see our taxonomy in `data/labels/vulnerability_types.json`)
- Any suggested remediation

We will acknowledge your report within **48 hours** and aim to release a fix within **14 days** for critical issues.

---

## Scope

The following are in scope for security reports:

| Component                                     | Examples                                        |
| --------------------------------------------- | ----------------------------------------------- |
| **REST API** (`src/inference/api.py`)         | Auth bypass, injection via scan input, DoS      |
| **Rules Engine** (`src/rules_engine/`)        | False negatives on known vuln patterns, evasion |
| **ML Pipeline** (`src/inference/pipeline.py`) | Adversarial inputs that bypass detection        |
| **Configuration** (`configs/`)                | Insecure defaults shipped in the repo           |
| **Docker / deployment** (`Dockerfile`)        | Privilege escalation, exposed secrets           |
| **Dependencies** (`requirements.txt`)         | Known CVEs in pinned packages                   |

The following are **out of scope**:

- Vulnerabilities in code _submitted to_ PolyGuard for scanning (that's the point — we're supposed to find those)
- Theoretical attacks with no practical exploit path
- Rate-limiting or abuse on the public HuggingFace Spaces demo

---

## Known Security Considerations

These are acknowledged design decisions, not bugs:

**`configs/api_config.yaml` — `secret_key: "change-me-in-production"`**
The JWT secret key placeholder must be replaced before any production deployment. Never run with the default value. See `.env.example` for the correct environment variable pattern.

**`api.py` — Unauthenticated scan endpoint**
The public `/analyze` endpoint intentionally requires no auth for the open demo. Production deployments should sit behind authentication middleware or an API gateway.

**Model input trust boundary**
Code submitted to the ML model is treated as untrusted text. The pipeline does not execute submitted code. However, extremely long inputs may affect inference latency — set `MAX_CODE_LENGTH` in your environment to enforce limits.

---

## Dependency Vulnerabilities

We monitor dependencies via GitHub Dependabot. If you spot a CVE in `requirements.txt` that Dependabot has not caught, please open a security report as described above.

To audit locally:

```bash
pip install pip-audit
pip-audit -r requirements.txt
```

---

## Disclosure Policy

We follow **coordinated disclosure**:

1. Reporter notifies us privately.
2. We confirm, reproduce, and develop a fix.
3. We release the fix and credit the reporter (unless anonymity is requested).
4. Details are published in the release notes after users have had time to update.

---

## Hall of Fame

Researchers who have responsibly disclosed issues will be credited here.

_No disclosures yet — be the first!_

---

_PolyGuard — Secure code is not optional._
