# Build Workflow Validation

This short note exists to trigger and document validation of the GitHub Actions `Build` workflow after workflow hardening.

## Validation target

The `Build` workflow should pass on pull requests to `main` and confirm:

- backend dependency restore succeeds
- API build succeeds
- Identity Server build succeeds
- Angular dependency install succeeds
- API client generation succeeds
- shared library, TMS, Admin, Customer, and Website builds succeed

## Operational note

This file can remain as a lightweight validation note, or be removed in a follow-up once the workflow is proven stable.
