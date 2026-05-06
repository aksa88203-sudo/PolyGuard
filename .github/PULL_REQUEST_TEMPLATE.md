## Summary

<!-- One or two sentences describing what this PR does and why. -->

Closes #<!-- issue number -->

---

## Type of Change

- [ ] Bug fix
- [ ] New vulnerability detector / rule
- [ ] ML model improvement (architecture, training, data)
- [ ] API change
- [ ] Refactor / code quality
- [ ] Documentation
- [ ] CI/CD / tooling
- [ ] Other: <!-- describe -->

---

## Changes

<!-- List the key files changed and what was done. Be specific about logic changes. -->

- `src/rules_engine/` — 
- `src/inference/` — 
- `tests/` — 
- `configs/` — 

---

## Testing

### Test Suite

```bash
pytest tests/ -v
```

- [ ] All existing tests pass
- [ ] New tests added for new behaviour
- [ ] Flake8 passes: `flake8 src/ --max-line-length=100`

### For Detector Changes

| Test | Result |
|------|--------|
| Vulnerable pattern detected | ✅ / ❌ |
| Safe pattern not flagged | ✅ / ❌ |
| Language exclusion correct (e.g. memory safety skips Python) | ✅ / ❌ |

### For API Changes

- [ ] `test_api.py` updated
- [ ] Endpoint tested manually with curl or `05_api.ipynb`

### For ML / Training Changes

- [ ] Evaluation metrics recorded: Precision / Recall / F1
- [ ] Results added to `docs/model_report.md`
- [ ] Experiment config saved under `experiments/exp_XX_<name>/config.yaml`

---

## Security Checklist

<!-- PolyGuard is a security tool — hold the PR to a high standard. -->

- [ ] No secrets, API keys, or real credentials introduced (checked `.env.example` pattern)
- [ ] No new dependencies added without pinning to a specific version in `requirements.txt`
- [ ] Input validation in place for any new API parameters
- [ ] Docker image does not run as root (if Dockerfile modified)
- [ ] `configs/api_config.yaml` `secret_key` remains a placeholder, not a real value

---

## Breaking Changes

- [ ] This PR introduces breaking changes

If yes, describe what breaks and the migration path:

<!-- e.g. "The `/analyze` response schema adds a required `cwe` field — clients must be updated." -->

---

## Screenshots / Output (if applicable)

<!-- Paste scan output, API response, or model evaluation table here. -->

```
# Example scan output
```

---

## Reviewer Notes

<!-- Anything specific you want the reviewer to focus on, or areas you're uncertain about. -->
