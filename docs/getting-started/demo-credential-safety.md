# Demo Credential Safety Review

This document records the safety expectations for the public LogisticsX demo credentials and seeded demo tenant.

## Purpose

The public demo exists so evaluators can explore role-based workflows without using production accounts or real payment details.

## Current state

- The live demo is publicly linked from the README.
- Seeded demo users are documented in `docs/getting-started/test-credentials.md`.
- Demo payment flows use Stripe test keys.
- Demo users can exercise role-specific workflows across admin, office, dispatch, driver, and customer-facing experiences.

## Required warnings

Every public demo entry point should make these rules clear:

- Do not enter real payment information.
- Do not enter real customer, driver, shipment, carrier, billing, or company data.
- Demo data may be shared with other users.
- Demo data may be reset without notice.
- Demo credentials are for evaluation only, not production use.

## Recommended controls

Use the lowest-friction control that still protects the demo environment:

1. Keep demo credentials documented only if they are intentionally public and non-sensitive.
2. Reset seeded demo data on a predictable cadence.
3. Prefer disposable seeded users or rotating demo passwords if abuse appears.
4. Restrict destructive actions in the public demo where practical.
5. Keep Stripe test-mode warnings visible near any billing or payment screen.
6. Keep README and `docs/getting-started/test-credentials.md` consistent.

## Documentation consistency checklist

- [ ] README links the current live demo.
- [ ] README and detailed credential docs list the same demo roles.
- [ ] Payment warning is visible before users reach payment flows.
- [ ] Shared-data warning is visible before users log in.
- [ ] Reset behavior is documented.
- [ ] Test credentials are rotated or intentionally accepted as public.

## Operational review cadence

Review this setup whenever any of the following change:

- authentication or role permissions
- billing or payment flows
- tenant seeding/reset logic
- public demo URL
- mobile app demo access
- production-like integrations enabled in demo

## Decision log

Record future demo-access decisions here:

| Date | Decision | Owner | Notes |
|------|----------|-------|-------|
| TBD | Confirm fixed public demo credentials vs rotating/disposable users | Project owner | Pending review |
