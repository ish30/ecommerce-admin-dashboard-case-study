# Testing and Safety

## Change principle

Admin redesigns can break more than appearance.

A small UI edit can affect:

- route links
- active navigation states
- filters
- form submission
- hidden compatibility contracts
- mobile behavior
- shared assets
- business wording

## Regression strategy

Tests protected:

- payment-recovery navigation
- payment-recovery calculations
- follow-up behavior
- dashboard widgets
- report links
- active sidebar states
- stylesheet completeness
- responsive selectors
- catalogue validation
- model-number sequencing
- slug synchronization
- product-readiness caching
- customisation workflow rules

## Public-safe test evidence

- 17 focused payment-recovery tests passed
- 236 full tests passed during payment-recovery UI stage
- 238 full tests passed with dashboard widget
- 242 full tests passed with analytics
- 262 tests passed for the initial review queue
- 268 tests passed for the corrected cached review queue

## Safer file-change rules

After truncated shared-file writes were detected:

- close the affected branch before merge
- confirm production and base branch were unchanged
- restart from a clean base
- prefer small isolated files
- avoid replacing long shared assets unnecessarily
- add minimum-length and closing-tag checks
- run complete CI before merge

## No fake proof

This case study does not claim:

- guaranteed revenue growth
- confirmed customer conversations from link clicks
- exact commercial recovery value
- public access to client source code
