# Utror iterative improvement loop

## Current published versions
- v1: `https://utror.app.apnd.no` / Coolify app `rgt9frltczl5ejpmb57085qm` / Git branch `main`.
- v2: `https://utror2.app.apnd.no` / Coolify app `llh957f1lcuos3jb3uv0kn2a` / Git branch `utror2` / commit `63bc212`.
- v3: `https://utror3.app.apnd.no` / Coolify app `zkea2tf19wmu98aud2f6uc60` / Git branch `utror3` / incorporates Daniel feedback 2026-05-25: removed meta-solution wording, forecast horizons update actual data, more granular charting across dashboard/prognosis.
- v4: `https://utror4.app.apnd.no` / Coolify app `inc7a8d8imeepn36sya5xba1` / Git branch `utror4` / commit `84755fe` / added critical-now prioritisation, clickable merd drill-down, clearer map data panel, richer simulated fish-pen camera overlays, and stricter mobile header/overflow handling.
- v5: `https://utror5.app.apnd.no` / Coolify app `jwq6h3t94367px6qx9lzljit` / Git branch `utror5` / commit `91c46cf` / moved map/camera ahead of generic KPIs, added operational state strip, stronger critical alert hierarchy, KPI drill-down affordance, and selected-merd camera/data coupling.
- v6: `https://utror6.app.apnd.no` / Coolify app `mhbjdrok1sigrigafs1fw3ev` / Git branch `utror6` / commit `0256ceb` / added incident-focus anleggskart, clearer A2/B2 cause chain, ROV-route mode, deduplicated action sequence, and tighter mobile nav with sticky critical CTA.
- v7: `https://utror7.app.apnd.no` / Coolify app `r129qh46ibc51plw5mkmlj7h` / Git branch `utror7` / commit `c95b267` (UI code `23a588c`) / added leader-summary reporting, reduced desktop/tablet chrome, improved first-screen map+camera composition, and made fish-camera rendering react visually to selected merd.

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

### v5 — 2026-05-25 23:13 UTC
- Latest version found before work: v4 (`utror4.app.apnd.no`, Coolify `inc7a8d8imeepn36sya5xba1`, branch `utror4`). Coolify also had v1/v2/v3; Git branches had `utror2`, `utror3`, `utror4`.
- Reviewed v4 with desktop and mobile screenshots plus ledermøte notes. Relevant context: Append is exploring havbruk/fiskeri leads, including Emilsen Fisk needing simpler reporting and a maritime/havbruk event.
- Strict v4 weaknesses: the title/meta chrome still competed with the critical issue; map/camera arrived too late after generic KPI cards; operational mode was not persistent enough; KPI cards looked informational but not clearly drillable; selected merd did not update camera HUD/data.
- Built v5 on branch `utror5`: operational state strip, more severe critical-now treatment with threshold/time/trend, facility map + fish-camera moved before generic KPIs, clickable KPI affordance, and merd selection now updates camera label, visibility, pellet return, stress and density values.
- Deploy: Coolify app `jwq6h3t94367px6qx9lzljit`, deployment `yk6of5xf0tg0104ijldtay5m` reached `finished` at `2026-05-25T23:12:45Z`.
- QA: verified live HTML contains `Utror ControlRoom v5`, `ops-state`, `cameraMerd`, `Kritisk nå`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified selected merd `B2` updates camera HUD/panel/pellet note; captured live desktop/mobile screenshots.
- Next round should focus on: compressing mobile header/nav even further, removing duplicate CTAs between alert and “Neste beste handling”, simplifying map overlays into a clearer A2/B2 incident-focus mode, and possibly adding sticky mobile critical CTA.

### v6 — 2026-05-26 00:11 UTC
- Latest version found before work: v5 (`utror5.app.apnd.no`, Coolify `jwq6h3t94367px6qx9lzljit`, branch `utror5`). Coolify apps/domains and Git branches showed v1–v5, so next version is v6.
- Reviewed v5 with desktop and mobile screenshots plus ledermøte notes. Relevant context remains simple reporting for Emilsen Fisk and havbruk/maritim leads; the demo should prioritize operator clarity over decorative dashboard density.
- Strict v5 weaknesses: mobile nav still showed horizontal overflow/chrome before substance; map was improved but still not enough of an incident-focus operational view; duplicate CTAs competed between critical alert and next-best-action; A2/B2 cause chain was not explicit enough; critical action was not sticky on mobile once the user scrolled into map/camera.
- Built v6 on branch `utror6`: compact 4-item mobile nav, hidden mobile intro copy, incident-focus map default that de-emphasizes non-affected cages, explicit “lav strøm → oksygenfall → fôr ned” cause chain, ROV-route focus mode, deduplicated next-best-action into a 3-step sequence, and sticky mobile critical CTA.
- Deploy: Coolify app `mhbjdrok1sigrigafs1fw3ev`, deployment `y31ievq4s4z653t49y4cwyme` reached `finished` at `2026-05-26T00:10:44Z`.
- QA: verified live HTML contains `Utror ControlRoom v6`, `incident-focus`, `mobile-cta`, `Start tiltak`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop and mobile views; browser-evaluated ROV focus + `B2` selection updates focus state, panel, and camera HUD.
- Next round should focus on: improving the tablet breakpoint around 1024px (rail consumes too much height before content), reducing hero/header height on desktop, making the canvas fish camera visually reflect selected A2 vs B2 more clearly, and adding a small “leader summary” view that answers Emilsen-style simple reporting needs without making the control room busier.

### v7 — 2026-05-26 01:13 UTC
- Latest version found before work: v6 (`utror6.app.apnd.no`, Coolify `mhbjdrok1sigrigafs1fw3ev`, branch `utror6`). Coolify apps/domains and Git branches showed v1–v6, so next version was v7.
- Reviewed v6 desktop/mobile via browser. Strict v6 weaknesses: tablet/desktop chrome still consumed too much vertical attention; mobile rail was 129 px before useful content; map was strong but camera still arrived too late; selected A2/B2 changed labels but did not feel visually different enough in the simulated fish-pen feed; leader-reporting was hidden in a separate page rather than visible as a simple operational summary.
- Built v7 on branch `utror7`: shorter desktop/tablet header, compact tablet rail, mobile rail reduced to 78 px, desktop first-screen composition now shows map and fish-camera together, added “Lederrapport på 15 sek” summary tiles for Emilsen-style simple reporting, expanded the report page into four concise executive tiles, and made the canvas camera tint/cluster/annotation change for A2 vs B2 vs normal merder.
- Deploy: Coolify app `r129qh46ibc51plw5mkmlj7h`, final deployment `hd8se8f0rl4q6bka5ep42ea3` reached `finished` at `2026-05-26T01:18:41Z` on commit `c95b267` (UI code commit `23a588c`).
- QA: verified live HTML contains `Utror ControlRoom v7`, `leader-summary`, `cameraBadge`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop/mobile dimensions and no horizontal overflow; browser-evaluated `B2` selection updates camera HUD, camera badge, panel and simulated camera context.
- Next round should focus on: making the live fish-camera even more credible visually (net geometry/depth/parallax), improving the map at very narrow widths so the panel does not cover too much of the cage field, and considering a one-click copy/export for the leader summary without adding clutter.
