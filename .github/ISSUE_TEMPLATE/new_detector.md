---
name: New Detector / Rule Proposal
about: Propose a new vulnerability pattern for the rules engine
title: "[DETECTOR] "
labels: rules-engine, enhancement
assignees: ""
---

## Vulnerability to Detect

**Name:** <!-- e.g. "Command Injection" -->
**CWE:** <!-- e.g. CWE-78 -->
**Severity:** <!-- Critical / High / Medium / Low -->
**Category:** <!-- Injection / XSS / Memory Safety / Secrets / Crypto / Auth / Other -->

## Affected Languages

<!-- Which languages should this detector cover? e.g. Python, JavaScript, C/C++ -->

## Vulnerable Pattern

<!-- Paste a minimal code example that should be flagged. -->

```python
# Vulnerable — should be detected
```

## Safe Pattern

<!-- Paste a minimal code example that should NOT be flagged (to help define the true-negative case). -->

```python
# Safe — should NOT be detected
```

## Proposed Detection Strategy

<!-- How should the detector work? Regex? AST pattern? Taint analysis? Both? -->

```python
# Sketch of the detection logic (optional but helpful)
```

## References

- OWASP: <!-- link -->
- CWE: <!-- https://cwe.mitre.org/data/definitions/XX.html -->
- CVE examples (if any): <!-- -->

## Test Cases

<!-- List the test IDs you plan to add in `tests/test_rules_engine.py`. -->

- `test_<vuln>_detected_<pattern>`
- `test_<vuln>_safe_<pattern>`

## Additional Notes

<!-- Anything else the reviewer should know — edge cases, related detectors to look at, etc. -->
