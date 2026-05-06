---
name: Bug Report
about: Something in PolyGuard isn't working correctly
title: "[BUG] "
labels: bug
assignees: ""
---

## Description

<!-- A clear, concise description of what the bug is. -->

## Component

<!-- Which part of PolyGuard is affected? -->

- [ ] Rules Engine (SQLi / XSS / Memory Safety / Secrets / Crypto detector)
- [ ] ML Inference Pipeline (`src/inference/pipeline.py`)
- [ ] REST API (`src/inference/api.py`)
- [ ] Data Pipeline (`src/data_pipeline/`)
- [ ] Training (`src/training/`)
- [ ] CLI / Scripts (`scripts/`)
- [ ] Docker / Deployment
- [ ] Other: <!-- describe -->

## Steps to Reproduce

```python
# Minimal code snippet or curl command that triggers the bug
```

1.
2.
3.

## Expected Behavior

<!-- What should happen. -->

## Actual Behavior

<!-- What actually happens. Include the full error message / traceback if applicable. -->

```
Paste traceback or error output here
```

## Environment

| Field | Value |
|-------|-------|
| OS | <!-- e.g. Ubuntu 22.04, macOS 14, Windows 11 --> |
| Python | <!-- e.g. 3.11.4 --> |
| PolyGuard version / commit | <!-- e.g. `0.1.0` or git SHA --> |
| GPU / device | <!-- e.g. CUDA 12.1 / CPU-only --> |
| Deployment | <!-- local / Docker / HuggingFace Spaces --> |

## Additional Context

<!-- Screenshots, log snippets from `experiments/logs/polyguard.log`, or anything else that helps. -->
