# Utror iterative improvement loop

## Current published versions
- v1: `https://utror.app.apnd.no` / Coolify app `rgt9frltczl5ejpmb57085qm` / Git branch `main`.
- v2: `https://utror2.app.apnd.no` / Coolify app `llh957f1lcuos3jb3uv0kn2a` / Git branch `utror2` / commit `63bc212`.
- v3: `https://utror3.app.apnd.no` / Coolify app `zkea2tf19wmu98aud2f6uc60` / Git branch `utror3` / incorporates Daniel feedback 2026-05-25: removed meta-solution wording, forecast horizons update actual data, more granular charting across dashboard/prognosis.
- v4: `https://utror4.app.apnd.no` / Coolify app `inc7a8d8imeepn36sya5xba1` / Git branch `utror4` / commit `84755fe` / added critical-now prioritisation, clickable merd drill-down, clearer map data panel, richer simulated fish-pen camera overlays, and stricter mobile header/overflow handling.
- v5: `https://utror5.app.apnd.no` / Coolify app `jwq6h3t94367px6qx9lzljit` / Git branch `utror5` / commit `91c46cf` / moved map/camera ahead of generic KPIs, added operational state strip, stronger critical alert hierarchy, KPI drill-down affordance, and selected-merd camera/data coupling.
- v6: `https://utror6.app.apnd.no` / Coolify app `mhbjdrok1sigrigafs1fw3ev` / Git branch `utror6` / commit `0256ceb` / added incident-focus anleggskart, clearer A2/B2 cause chain, ROV-route mode, deduplicated action sequence, and tighter mobile nav with sticky critical CTA.
- v7: `https://utror7.app.apnd.no` / Coolify app `r129qh46ibc51plw5mkmlj7h` / Git branch `utror7` / commit `c95b267` (UI code `23a588c`) / added leader-summary reporting, reduced desktop/tablet chrome, improved first-screen map+camera composition, and made fish-camera rendering react visually to selected merd.
- v8: `https://utror8.app.apnd.no` / Coolify app `lh1cq3wqk00jpx4d9bmwx0zc` / Git branch `utror8` / commit `73ed4fe` / fixed mobile rail overflow, made narrow map panel less obstructive, improved fish-camera net/depth/parallax realism, and added one-click leader-summary copy.
- v9: `https://utror9.app.apnd.no` / Coolify app `ggtn7s7uo1r02y1serrruaml` / Git branch `utror9` / commit `fd652ab` / brought map and live fish-camera higher on desktop, compressed mobile first screen, turned mobile map detail into a collapsible bottom sheet, and added visible action/copy receipts.
- v10: `https://utror10.app.apnd.no` / Coolify app `gzmo0p8vwsbyyglhaox7n46l` / Git branch `utror10` / commit `b7391cd` / densified leader summary, added more nautical/operational map context, strengthened A2/B2 fish-camera visual behavior, and fixed desktop aside overflow.
- v11: `https://utror11.app.apnd.no` / Coolify app `re8trwl7pv4flpcqzu3remm7` / Git branch `utror11` / commit `a9ba519` / moved mobile live camera directly after alert/progress, added compact mobile tiltaksstepper, clarified clickable map/camera controls, and preserved desktop first-screen density.
- v12: `https://utror12.app.apnd.no` / Coolify app `zun2qpnrhjfleixyew61anmt` / Git branch `utror12` / commit `384b67d` / tightened mobile chrome, brought live camera into the first viewport, added explicit next-manual-verification timing, and refined the camera card hierarchy.

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
- Deploy: Coolify app `r129qh46ibc51plw5mkmlj7h`, final verified deployment `qy2vsk70anncwo7x3nbqng00` reached `finished` at `2026-05-26T01:19:32Z` on commit `e0cd9c9` (UI code commit `23a588c`).
- QA: verified live HTML contains `Utror ControlRoom v7`, `leader-summary`, `cameraBadge`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop/mobile dimensions and no horizontal overflow; browser-evaluated `B2` selection updates camera HUD, camera badge, panel and simulated camera context.
- Next round should focus on: making the live fish-camera even more credible visually (net geometry/depth/parallax), improving the map at very narrow widths so the panel does not cover too much of the cage field, and considering a one-click copy/export for the leader summary without adding clutter.

### v8 — 2026-05-26 02:12 UTC
- Latest version found before work: v7 (`utror7.app.apnd.no`, Coolify `r129qh46ibc51plw5mkmlj7h`, branch `utror7`). Coolify apps/domains and Git branches showed v1–v7, so next version was v8.
- Reviewed v7 desktop/mobile via browser plus memory and ledermøte notes. Strict v7 weaknesses: mobile nav still clipped on narrow width, the mobile map panel covered too much cage field, the simulated fish camera needed stronger net/depth/parallax cues to feel like a real merd, and the leader summary was readable but not easy to export/copy.
- Built v8 on branch `utror8`: mobile rail is single-column with all nav items visible and no horizontal overflow, mobile map panel is compact and shifted out of the cage center, fish camera now has curved net geometry/depth rings/current shimmer, and leader report/summary can be copied as a 3-point status.
- Deploy: Coolify app `lh1cq3wqk00jpx4d9bmwx0zc`, deployment `g5ep9mbvc1d0hrdhejnb4d1b` reached `finished` at `2026-05-26T02:09:34Z` on commit `73ed4fe`.
- QA: verified live HTML contains `Utror ControlRoom v8`, `copyLeaderSummary`, `net-depth`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop/mobile views, no horizontal overflow, `B2` selection updates camera HUD/panel, and copy action runs.
- Next round should focus on: making the map panel even smarter on narrow screens (collapsible or bottom sheet), reducing first-screen height before map/camera, and adding richer operational feedback after copying or executing leader-summary actions without adding clutter.

### v9 — 2026-05-26 03:12 UTC
- Latest version found before work: v8 (`utror8.app.apnd.no`, Coolify `lh1cq3wqk00jpx4d9bmwx0zc`, branch `utror8`). Coolify apps/domains and Git branches showed v1–v8, so next version was v9.
- Reviewed v8 desktop/mobile via browser metrics plus memory and ledermøte notes. Relevant context remains Emilsen Fisk/simple reporting and havbruk/maritim leads.
- Strict v8 weaknesses: desktop still pushed the live fish-camera too low and gave the map a narrow field; mobile still spent ~705 px before the map, the critical card was too tall, and the mobile map panel still covered operational cage context. Copy/execute interactions were acknowledged only by transient toast, not persistent enough for operator confidence.
- Built v9 on branch `utror9`: widened the desktop operational surface, reordered live fish-camera above oxygen details, compressed mobile rail/top/ops/critical blocks so map appears around 399 px, converted the mobile map panel to a tap-to-expand bottom sheet, and added persistent action receipts after fôr/ROV/storm/resolve/copy actions.
- Deploy: Coolify app `ggtn7s7uo1r02y1serrruaml`, deployment `nmbq3kfipo318juikruq6ntz` reached `finished` at `2026-05-26T03:12:11Z` on code commit `fd652ab`; iteration log commit `cb31e21`.
- QA: verified live HTML contains `Utror ControlRoom v9`, `actionReceipt`, `togglePanel`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop/mobile dimensions, no horizontal overflow in mobile, B2 selection updates camera/panel, collapsible panel expands, and `Start tiltak` produces persistent receipt + updated prognosis tag.
- Next round should focus on: reducing desktop leader-summary height or turning it into a denser status strip so map/camera start even closer to the top, improving visual differentiation in the simulated fish camera beyond labels/tint, and making the anleggskart more geographically credible without clutter.

### v10 — 2026-05-26 04:15 UTC
- Latest version found before work: v9 (`utror9.app.apnd.no`, Coolify `ggtn7s7uo1r02y1serrruaml`, branch `utror9`). Coolify apps/domains and Git branches showed v1–v9, so next version was v10.
- Reviewed v9 desktop/mobile screenshots, memory, UTROR iteration log and ledermøte notes. Relevant context remains Emilsen Fisk/simple reporting plus maritime/havbruk leads.
- Strict v9 weaknesses: leader-summary still consumed too much first-screen height; map felt polished but not geographically/nautically credible enough; live fish-camera differentiated A2/B2 mostly by labels/tint rather than behavior; desktop right-side action column could overflow/clutter; mobile still needs tighter action/camera prioritisation after map.
- Built v10 on branch `utror10`: compact leader status strip, bathymetry/coordinates/compass/mooring cues in anleggskart, clearer simulated merdkamera disclosure, stronger canvas behavior differences (A2 dense stressed/pellet-heavy cluster, B2 slower low-current band), and desktop aside overflow fix.
- Deploy: Coolify app `gzmo0p8vwsbyyglhaox7n46l`, deployment `wcnaljjkghdtzcgo081st1di` reached `finished` at `2026-05-26T04:14:23Z` on commit `b7391cd`.
- QA: verified live HTML contains `Utror ControlRoom v10`, `leader-summary compact`, `BATYMETRI`, `simulert merdkamera`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop/mobile dimensions with no horizontal overflow; browser-evaluated `B2` selection + ROV focus updates panel and camera HUD; captured final desktop/mobile screenshots.
- Next round should focus on: pulling the live camera even closer to the primary alert/action on mobile, making clickable map/camera controls more visually distinct from informational chips, and showing progress/consequence after `Start tiltaksekvens` as a compact stepper rather than only receipt/toast.

### v11 — 2026-05-26 05:12 UTC
- Latest version found before work: v10 (`utror10.app.apnd.no`, Coolify `gzmo0p8vwsbyyglhaox7n46l`, branch `utror10`). Coolify apps/domains and Git branches showed v1–v10, so next version was v11.
- Reviewed v10 desktop/mobile via browser metrics plus memory, iteration log and ledermøte notes. Relevant context remains Emilsen Fisk/simple reporting, havbruk leads and maritime event context.
- Strict v10 weaknesses: mobile still put the live fish-camera too far below the primary alert/action; `Start tiltakssekvens` changed receipt/prognosis but did not show a compact step-by-step consequence near the decision; clickable map focus controls and risky merds looked too close to informational chips; desktop should not lose its map+camera first-screen density.
- Built v11 on branch `utror11`: mobile order now shows alert → tiltaksstepper → live fish-camera before the anleggskart, `Start tiltakssekvens` advances a compact 3-step progress indicator, A2/B2 risky merds have clearer click affordance/focus states, incident controls are visually distinct, and the desktop-only quick stepper is hidden so desktop map/camera remain high.
- Deploy: Coolify app `re8trwl7pv4flpcqzu3remm7`, final deployment `wqzo48btzw4iw0m1u2dhmyhn` reached `finished` at `2026-05-26T05:13:09Z` on deployed commit `2ac6d28` (UI code commit `a9ba519`; later commits may be log-only updates).
- QA: verified live HTML contains `Utror ControlRoom v11`, `quick-stepper`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified desktop map/camera start at y=448 with no horizontal overflow, mobile camera starts at y=499 before map and no horizontal overflow; browser-evaluated `B2` selection + ROV focus updates panel/camera HUD and `Start tiltakssekvens` advances the mobile stepper/receipt/prognosis.
- Next round should focus on: reducing mobile top chrome by another 40–70 px so the live camera starts even closer to the first viewport, adding an explicit “next manual verification due” timestamp after the stepper, and making the map geographically richer only if it can be done without pushing camera/action down.

### v12 — 2026-05-26 06:12 UTC
- Latest version found before work: v11 (`utror11.app.apnd.no`, Coolify `re8trwl7pv4flpcqzu3remm7`, branch `utror11`). Coolify apps/domains and Git branches showed v1–v11, so next version was v12.
- Reviewed v11 desktop/mobile via browser metrics plus memory, iteration log and ledermøte notes. Relevant context remains Emilsen Fisk/simple reporting, havbruk/fiskeri leads and maritime event context.
- Strict v11 weaknesses: mobile top chrome still consumed 95 px before content; the live fish camera started at y=613 on 390×844, leaving too little first-viewport operational confidence; the stepper lacked a concrete next manual verification timestamp; and the desktop camera card still read as secondary under oxygen details rather than as the live evidence surface.
- Built v12 on branch `utror12`: compressed mobile rail/top/critical blocks, added `verify-due` inside the mobile tiltaksstepper, dynamically updates verification time after fôr/ROV actions, gave the camera card a clearer live-evidence affordance, and preserved noindex/robots/no external video.
- Deploy: Coolify app `zun2qpnrhjfleixyew61anmt`, deployment `ctblx6fd7qix6ns8nf3640bo` reached `finished` at `2026-05-26T06:10:21Z` on commit `384b67d`.
- QA: verified live HTML contains `Utror ControlRoom v12`, `verify-due`, and `noindex, nofollow, noarchive`; verified `robots.txt` blocks all crawlers; browser-verified mobile no horizontal overflow with rail 76 px and live camera y=485; browser-evaluated `B2` selection + `Start tiltakssekvens` updates camera badge, panel, receipt, stepper and next-verification time. App status later reported `running:unknown` after successful deploy and live 200 response.
- Next round should focus on: desktop first-screen hierarchy after receipt appears (map/camera can be pushed down), making the manual verification cue visible on desktop without adding clutter, and making the anleggskart richer only if map/camera vertical priority is preserved.

### final / utrordata — 2026-05-26 06:54 UTC
- Hourly cron `Utror hourly design iteration` was cancelled on Daniel's request. Existing version apps v2–v12 were left untouched.
- Built final public version on branch `utrordata-final`: all SVG/heat/bar diagrams get point/cell tooltips on hover/tap, the front page now has two larger axis-labelled decision graphs (`frontOxygenChart`, `frontOpsChart`), and tooltip/mobile overflow was corrected so hidden UI does not create layout overlap.
- Published to `https://utrordata.app.apnd.no` as Coolify app `u654951s9z8ldklv1mok77fq`; final deployment `wksdgg0xlnfog947ifie9mv0` reached `finished` at `2026-05-26T06:55:19Z` on UI code commit `9e07f60`; latest iteration log commit `d18eb39`.
- QA: verified live HTML contains `Utror ControlRoom final`, `frontOxygenChart`, `diagram-tip`, `noindex, nofollow, noarchive`; verified `robots.txt` blocks crawlers; browser-verified desktop and 390px mobile have no horizontal overflow, front charts render with axes/points, and tapping a front chart point shows the correct tooltip.
