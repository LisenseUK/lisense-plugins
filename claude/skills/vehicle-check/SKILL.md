---
name: vehicle-check
description: Check a UK vehicle by registration with Lisense. Use when the user gives a UK number plate and asks about its tax, MOT, mileage, history or whether it is worth buying.
---

# Vehicle check

1. Call `vehicle-lookup` with the registration, without spaces.
2. Summarise make, model, colour, fuel and engine size; tax status and expiry; MOT expiry; latest recorded mileage and date; and MOT pass/fail totals.
3. Flag gaps or drops in recorded mileage between MOT tests, and repeated advisories.
4. For an unfamiliar advisory or defect, call `mot-advisory-search` with its wording or manual reference. Keep the recorded severity.
5. If the user wants more, offer `enhanced-specification`, `vehicle-insights` or `motability-status`. These may need add-ons or credits; when a tool reports a missing entitlement, say so rather than guessing.

Present data as Lisense records, not a mechanical inspection. Predictions from `vehicle-insights` are estimates, not a diagnosis.
