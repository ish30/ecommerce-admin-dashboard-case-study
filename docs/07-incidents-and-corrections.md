# Incidents and Corrections

## Incident 1 — Product review queue timeout

### Cause

The initial page request scanned the full catalogue and performed repeated readiness and duplicate assessments.

### Response

- reverted the production-risking implementation
- moved assessment to a chunked command
- cached audit results
- kept HTTP requests read-only and paginated
- added stale-state handling
- validated with 268 passing tests

### Lesson

A useful feature can still have the wrong execution model.

---

## Incident 2 — Truncated management-report stylesheet

### Cause

A stylesheet write ended in the middle of a declaration and lacked its closing style tag. The browser treated following markup as CSS, causing blank report pages.

### Response

- restored the full stylesheet
- retained responsive rules
- added a completeness test
- verified server rendering to separate presentation failure from backend failure

### Lesson

Asset integrity deserves regression tests when write tooling can truncate files.

---

## Incident 3 — Truncated shared JavaScript / layout write

### Cause

Large shared-file replacement payloads were truncated on feature branches.

### Response

- closed the affected branches unmerged
- confirmed production and the base branch were unaffected
- recreated the changes from clean branches
- used smaller, isolated, safer modifications

### Lesson

Reversion and branch abandonment are valid engineering tools. Protecting the base branch matters more than rescuing a flawed change.
