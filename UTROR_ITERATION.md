# Utror iterative improvement loop

## Current published versions
- v1: `https://utror.app.apnd.no` / Coolify app `rgt9frltczl5ejpmb57085qm` / Git branch `main`.
- v2: `https://utror2.app.apnd.no` / Coolify app `llh957f1lcuos3jb3uv0kn2a` / Git branch `utror2` / commit `63bc212`.
- v3: `https://utror3.app.apnd.no` / Coolify app `zkea2tf19wmu98aud2f6uc60` / Git branch `utror3` / incorporates Daniel feedback 2026-05-25: removed meta-solution wording, forecast horizons update actual data, more granular charting across dashboard/prognosis.
- v4: `https://utror4.app.apnd.no` / Coolify app `inc7a8d8imeepn36sya5xba1` / Git branch `utror4` / commit `84755fe` / added critical-now prioritisation, clickable merd drill-down, clearer map data panel, richer simulated fish-pen camera overlays, and stricter mobile header/overflow handling.

## Standing quality bar
- Use `frontend-design` skill every run.
- Review requirements and prior critique before coding.
- Take screenshots of latest live version before deciding changes.
- Be stricter than last run: remove clutter, fix overlaps, test mobile and desktop.
- Use a real-looking/simulated fish-pen live view; never embed an unrelated video.
- Keep the facility map clean and operationally readable.
- Preserve `noindex, nofollow, noarchive` and `robots.txt`.
- Each hourly iteration publishes to the next unused domain: `utror3.app.apnd.no`, `utror4.app.apnd.no`, etc.

## Original explicit critique from Daniel, 2026-05-25
- Previous live video was not a fish pen and sat behind numbers; unacceptable.
- Facility map was ugly and cluttered.
- Dashboard overall was too cluttered and poor; it needs to be polished, clear, informative, interactive and close to perfect.

## Iteration log

### v4 — 2026-05-25 22:15 UTC
- Latest version found before work: v3 (`utror3.app.apnd.no`, Coolify `zkea2tf19wmu98aud2f6uc60`, branch `utror3`). Coolify also had v1/v2; Git branches had `utror2` and `utror3`.
- Reviewed v3 with desktop and mobile screenshots. Weak points: all KPI cards had nearly equal priority; map was still more illustrative than operational; merds did not clearly expose drill-down; mobile spent too much first-screen space before critical status; fish-camera needed more concrete instrumentation.
- Built v4 on branch `utror4`: critical-now strip above generic KPIs, clickable merds with selected-merd panel, stronger direct connection between A2/B2 risk and actions, richer canvas fish-pen simulation with depth scale/bubbles/pellets overlay, and mobile overflow/header fixes.
- Deploy: Coolify deployment `l22m69dwpvix0mglzux9pll4` reached `finished` at `2026-05-25T22:14:54Z`.
- QA: verified live HTML contains `Utror ControlRoom v4`, `critical-strip`, `selectMerd`, `Pelletsretur 7,4 %`, and `noindex, nofollow, noarchive`; verified `robots.txt` still blocks all crawlers; captured live desktop/mobile screenshots. Mobile is materially better, but the next round should still reduce the first viewport height and make the nav/action row feel less cramped.
- Next round should focus on: making the fish-pen camera respond to selected merd, adding visible hover/active affordance for KPI drill-down, and improving mobile hierarchy so “critical now + next action” is visible even earlier.
