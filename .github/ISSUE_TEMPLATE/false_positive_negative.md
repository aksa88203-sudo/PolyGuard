---
name: False Positive / False Negative
about: PolyGuard flagged safe code as vulnerable, or missed a real vulnerability
title: "[FP/FN] "
labels: detection-quality
assignees: ""
---

## Report Type

- [ ] **False Positive** — PolyGuard flagged this code as vulnerable, but it is safe
- [ ] **False Negative** — PolyGuard did not detect a vulnerability that exists

## Vulnerability Type

<!-- Which detector is involved? -->

- [ ] SQL Injection (CWE-89)
- [ ] XSS (CWE-79)
- [ ] Buffer Overflow / Memory Safety (CWE-120)
- [ ] Hardcoded Secret (CWE-798)
- [ ] Weak Cryptography (CWE-327)
- [ ] Broken Authentication (CWE-287)
- [ ] Other: <!-- describe -->

## Language

<!-- e.g. Python, JavaScript, C/C++, Go, Java, Ruby, PHP, Rust -->

## Code Sample

<!-- Paste the minimal code snippet that demonstrates the issue. Sanitize any real secrets before posting. -->

```python
# Paste code here
```

## Detection Source

- [ ] Rules Engine only (`--rules-only`)
- [ ] ML model
- [ ] Both
- [ ] Unknown

## Actual vs. Expected

**What PolyGuard reported:**

```
# Paste finding output or "No findings detected"
```

**What it should have reported:**

<!-- e.g. "Should have flagged line 7 as SQL Injection" or "Should not have flagged this — the query uses parameterized inputs." -->

## Analysis (Optional)

<!-- If you know why this happens — e.g. a regex gap in `sqli_detector.py`, a pattern the model has not seen — please share. -->

## References

<!-- CVE, CWE link, OWASP page, or any other context that establishes this as a real vulnerability or confirms it is safe. -->
