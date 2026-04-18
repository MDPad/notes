---
Theme:
  - "[[Software development]]"
---

## Development methodology

- **Small, focused merge requests**
    1.  Target MR size is 100–200 lines to keep reviews fast and manageable.
    2.  The only exception is large architectural refactoring when splitting isn't practical.
- **Refactor first, feature second**
    1.  We aim to reduce cognitive complexity and minimize future tech debt by preparing the architecture or module structure before adding product logic.
    2.  Backend follows the DDD concepts
- **Everyone reviews MR**
    1.  Regular reviews help spread domain knowledge, ensure consistency, and keep our merge flow efficient.
- **Backward compatibility by default**
    1. Backend evolves APIs additively, with gradual deprecation.
    2. Frontend manages incompatible changes behind feature toggles.
- **Frequent small rollouts**
    1.  Even if a change doesn’t include visible product functionality (refactoring, contract updates), we still ship early to validate behavior in real conditions and reduce risk.


## Bug-fixing workflow  

When fixing a bug:  
- first write a test that reproduces the issue
- then implement the fix
 This approach helps us build a solid regression suite over time.  
  
## Testing agreements  

**General**  
- Frontend and backend develop independently.
- Breaking changes go behind feature toggles.
- Backend provides mocks; frontend develops and tests against them.
- Quality gate: all linting and test pipelines must be green.

**Feature validation**  
- After both sides complete their parts, QA tests the feature with toggles enabled.
- Critical issues return the feature to development.
- Once stable, toggles are removed and the feature becomes visible to users.  
  
_Development team responsibilities_  
- Unit tests are required, especially on the storage layer.
- Any MR that adds or updates queries must include tests.
- ClickHouse tests use testcontainers; fixtures stored separately.
- QA reviews test coverage; fixtures become part of staging setup.
- Self-check on RC and after production deployment is expected.

_QA responsibilities_  
- E2E coverage for validation, limits, authorization, and sanity checks.
- QA maintains dependency mocks.
- QA owns frontend test coverage.