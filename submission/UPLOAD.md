# Latest Kaggle upload

## 2026-09-28 (user, ~21:25Z): vrp20_pfsoff 56652418 — FINAL PAIR vrp19w_k2wide 56649892 + vrp20_pfsoff 56652418

| | vrp20_pfsoff (master config) | vrp19w_k2wide (the other live slot) |
|---|---|---|
| Kaggle submission | **56652418** | **56649892** (unchanged) |
| Tarball | dist/vrp20_pfsoff.tar.gz md5 e5d84f03f330997539d76eda6b7baf1a (1,162,044 B, 31 files) | dist/vrp19w_k2wide.tar.gz md5 e490347d2f4db64ee8ca68cf3aec74cc (1,162,159 B, 31 files) |
| Recipe | vrp18_k2hb2046 with `KERNEL2_FIRE_CASH = "99999"`: no live rival h1 value is listed, so the step-1 latch never fires and every seat plays PFS (FIRELIVE1's OFF arm, FINALPLAN1's last upload); KERNEL2_ON and HANDBACK at day 18 stay (vacuous). Differs from vrp18_k2hb2046 and from vrp19w_k2wide only in kagg3/core/plan.py (one line) | vrp18_k2hb2046 + the WIDE 36-value KERNEL2 fire list |
| Source commit | **eeea2793** (ship_vrp20_pfsoff: b940d667 config, eeea2793 pins/tests on 0735ea4c), merged into master 5f289d05 (SHIPSYNC5); tests/_pin.SHIPPED = b940d667 | 72570ca8 (config 81090f6a) |
| Theta / head / eswork | theta7659 94a8ffd2, head_940 769ff15e, eswork_theta 6928257a (unchanged) | same |
| Evidence | docs/strategy/2026-09-28-pack20.md, -finalplan1.md, -firelive1.md | docs/strategy/2026-09-28-packwide1.md, -boldslot1.md |

Gene block (S/actionrl/live_expert.py SWITCHES, == plan defaults):
`OPEN_PUMP_ON=True,TAIL_FILL_ON=True,BANK_BEFORE_LOT_ON=True,HIRE_ROW_ON=True,brain.MELON_GENE_ON=True,brain.CROP_DAY_ON=True,ENDROUTE_ON=True,ENDROUTE2_ON=True,ENDROUTE2_SPLIT_ON=True,ENDROUTE_ROW2_ON=True,CLIP_CAP_ON=False,WIDE_PICK_ON=True,CARE_FILL_ON=True,OVERFLOW_GUARD_ON=True,OVERFLOW_GUARD_V2=True,OVERFLOW_GUARD_V3=True,LATE_EXEC_ON=True,ROUTE_VRP_ON=True,ROUTE_VRP_FIX_FROZEN=True,ROUTE_VRP_VERIFY=True,ROUTE_VRP_NEEDS_FIX_ON=True,ROUTE_VRP_REPAIR_ON=True,PLACEFEED_ON=True,PF_PUMPSAFE_ON=True,KERNEL2_ON=True,KERNEL2_NOOP_H0=False,KERNEL2_INHERIT=True,KERNEL2_FIRE_CASH=99999,KERNEL2_PRELOAD=False,KERNEL2_HANDBACK_DAY=18`

vrp18_k2hb2046 56646827 RETIRED (FIFO). Final pair (RULES1: Bradley-Terry over Oct 1-15 games of the last 2 uploads before
09-30 23:59Z) = vrp19w_k2wide 56649892 + vrp20_pfsoff 56652418. A further upload would retire vrp19w_k2wide.
Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ = the vrp20_pfsoff tarball
(31 files, cmp-identical); submission/vrp19w_k2wide/ = the vrp19w_k2wide tarball tree (31 files, cmp-identical); both
tarballs alongside (submission/vrp20_pfsoff.tar.gz, submission/vrp19w_k2wide.tar.gz); submission/vrp18_k2hb2046/ and its
tarball removed. SHIPSYNC5: all 27 kagg3/ files of the tarball are byte-identical to master src/kagg3; plan.py
KERNEL2_FIRE_CASH = "99999", KERNEL2_HANDBACK_DAY = 18; main.py == scripts/package_submission.main_source(
residual=True, kernel2=True); engine.lock.json == vendor/engine.lock.json. Doc docs/strategy/2026-09-28-shipsync5.md.

---

## 2026-09-28 (user, ~19:10Z): vrp19w_k2wide 56649892 — THE OTHER LIVE SLOT of the final pair (vrp18_k2hb2046 56646827 RETIRED 09-28 ~21:25Z)

| | vrp19w_k2wide (master config) | vrp18_k2hb2046 (the other live slot) |
|---|---|---|
| Kaggle submission | **56649892** | **56646827** (unchanged) |
| Tarball | dist/vrp19w_k2wide.tar.gz md5 e490347d2f4db64ee8ca68cf3aec74cc (1,162,159 B, 31 files) | dist/vrp18_k2hb2046.tar.gz md5 d6ed14d6449d0fa2593f3f785b8e686c (1,162,013 B, 31 files) |
| Recipe | vrp18_k2hb2046 + the WIDE KERNEL2 fire list: `KERNEL2_FIRE_CASH` = 36 values = vrp18's 5 + 31 MELON rival h1 values (BOLDSLOT1 wide list minus 20/2464 KEEP-OUT and 2015/2885 V-collision); HANDBACK at day 18 unchanged. Differs from vrp18_k2hb2046 only in kagg3/core/plan.py (one line) | vrp17_k2hb + 2046 in `KERNEL2_FIRE_CASH` |
| Source commit | **72570ca8** (ship_vrp19w_k2wide: 81090f6a config, 72570ca8 pins/tests on 0735ea4c), merged into master 84cc3122 (SHIPSYNC4); tests/_pin.SHIPPED = 81090f6a | 0735ea4c (config 599f8881) |
| Theta / head / eswork | theta7659 94a8ffd2, head_940 769ff15e, eswork_theta 6928257a (unchanged) | same |
| Evidence | docs/strategy/2026-09-28-packwide1.md, -boldslot1.md | docs/strategy/2026-09-28-pack18.md, -liveval1.md |

Gene block (S/actionrl/live_expert.py SWITCHES, == plan defaults):
`OPEN_PUMP_ON=True,TAIL_FILL_ON=True,BANK_BEFORE_LOT_ON=True,HIRE_ROW_ON=True,brain.MELON_GENE_ON=True,brain.CROP_DAY_ON=True,ENDROUTE_ON=True,ENDROUTE2_ON=True,ENDROUTE2_SPLIT_ON=True,ENDROUTE_ROW2_ON=True,CLIP_CAP_ON=False,WIDE_PICK_ON=True,CARE_FILL_ON=True,OVERFLOW_GUARD_ON=True,OVERFLOW_GUARD_V2=True,OVERFLOW_GUARD_V3=True,LATE_EXEC_ON=True,ROUTE_VRP_ON=True,ROUTE_VRP_FIX_FROZEN=True,ROUTE_VRP_VERIFY=True,ROUTE_VRP_NEEDS_FIX_ON=True,ROUTE_VRP_REPAIR_ON=True,PLACEFEED_ON=True,PF_PUMPSAFE_ON=True,KERNEL2_ON=True,KERNEL2_NOOP_H0=False,KERNEL2_INHERIT=True,KERNEL2_FIRE_CASH=1|4|8|17|19|23|26|29|34|73|76|117|160|163|182|190|444|456|553|564|620|638|661|938|1616|2046|2322|2338|2438|2477|2485|2492|2511|2593|2600|2904,KERNEL2_PRELOAD=False,KERNEL2_HANDBACK_DAY=18`

vrp17_k2hb 56643352 RETIRED (FIFO). Final pair (RULES1: Bradley-Terry over Oct 1-15 games of the last 2 uploads before
09-30 23:59Z) = vrp18_k2hb2046 56646827 + vrp19w_k2wide 56649892. A further upload would retire vrp18_k2hb2046.
Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ = the vrp19w_k2wide tarball
(31 files, cmp-identical); submission/vrp18_k2hb2046/ = the vrp18_k2hb2046 tarball tree (31 files, cmp-identical); both
tarballs alongside (submission/vrp19w_k2wide.tar.gz, submission/vrp18_k2hb2046.tar.gz); submission/vrp17_k2hb/ and its
tarball removed. SHIPSYNC4: all 27 kagg3/ files of the tarball are byte-identical to master src/kagg3; plan.py
KERNEL2_FIRE_CASH = the 36-value list, KERNEL2_HANDBACK_DAY = 18; main.py == scripts/package_submission.main_source(
residual=True, kernel2=True); engine.lock.json == vendor/engine.lock.json. Doc docs/strategy/2026-09-28-shipsync4.md.

---

## 2026-09-28 (user, ~16:35Z): vrp18_k2hb2046 56646827 — RETIRED (FIFO) by vrp20_pfsoff 56652418 09-28 ~21:25Z (tree + tarball removed from submission/ at SHIPSYNC5)

| | vrp18_k2hb2046 (master config) | vrp17_k2hb (the other live slot) |
|---|---|---|
| Kaggle submission | **56646827** | **56643352** (unchanged) |
| Tarball | dist/vrp18_k2hb2046.tar.gz md5 d6ed14d6449d0fa2593f3f785b8e686c (1,162,013 B, 31 files) | dist/vrp17_k2hb.tar.gz md5 11fd0f57e33acac6a53a78a2e85491a4 (1,161,963 B, 31 files) |
| Recipe | vrp17_k2hb + rival h1 cash 2,046 added to the KERNEL2 fire whitelist (`KERNEL2_FIRE_CASH = "26\|29\|2046\|2338\|2438"`, LIVEVAL1 CANDIDATE); HANDBACK at day 18 unchanged. Differs from vrp17_k2hb only in kagg3/core/plan.py | vrp15_k2fire + `KERNEL2_HANDBACK_DAY = 18` |
| Source commit | **0735ea4c** (ship_vrp18_k2hb2046: 599f8881 config, 0735ea4c pins/tests on a7fcad46), merged into master e08beb65 (SHIPSYNC3); tests/_pin.SHIPPED = 599f8881 | a7fcad46 (config ec2a6042) |
| Theta / head / eswork | theta7659 94a8ffd2, head_940 769ff15e, eswork_theta 6928257a (unchanged) | same |
| Evidence | docs/strategy/2026-09-28-pack18.md, -liveval1.md | docs/strategy/2026-09-28-handback2.md, -packhb1.md |

Gene block (S/actionrl/live_expert.py SWITCHES, == plan defaults):
`OPEN_PUMP_ON=True,TAIL_FILL_ON=True,BANK_BEFORE_LOT_ON=True,HIRE_ROW_ON=True,brain.MELON_GENE_ON=True,brain.CROP_DAY_ON=True,ENDROUTE_ON=True,ENDROUTE2_ON=True,ENDROUTE2_SPLIT_ON=True,ENDROUTE_ROW2_ON=True,CLIP_CAP_ON=False,WIDE_PICK_ON=True,CARE_FILL_ON=True,OVERFLOW_GUARD_ON=True,OVERFLOW_GUARD_V2=True,OVERFLOW_GUARD_V3=True,LATE_EXEC_ON=True,ROUTE_VRP_ON=True,ROUTE_VRP_FIX_FROZEN=True,ROUTE_VRP_VERIFY=True,ROUTE_VRP_NEEDS_FIX_ON=True,ROUTE_VRP_REPAIR_ON=True,PLACEFEED_ON=True,PF_PUMPSAFE_ON=True,KERNEL2_ON=True,KERNEL2_NOOP_H0=False,KERNEL2_INHERIT=True,KERNEL2_FIRE_CASH=26|29|2046|2338|2438,KERNEL2_PRELOAD=False,KERNEL2_HANDBACK_DAY=18`

vrp15_k2fire 56634350 RETIRED (FIFO). Final pair (RULES1: Bradley-Terry over Oct 1-15 games of the last 2 uploads before
09-30 23:59Z) = vrp17_k2hb 56643352 + vrp18_k2hb2046 56646827. A further upload would retire vrp17_k2hb.
Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ = the vrp18_k2hb2046 tarball
(31 files, cmp-identical); submission/vrp17_k2hb/ = the vrp17_k2hb tarball tree (31 files, cmp-identical); both tarballs
alongside (submission/vrp18_k2hb2046.tar.gz, submission/vrp17_k2hb.tar.gz); submission/vrp15_k2fire/ and its tarball removed.
SHIPSYNC3: all 27 kagg3/ files of the tarball are byte-identical to master src/kagg3; plan.py KERNEL2_FIRE_CASH =
"26|29|2046|2338|2438", KERNEL2_HANDBACK_DAY = 18; main.py == scripts/package_submission.main_source(residual=True,
kernel2=True); engine.lock.json == vendor/engine.lock.json. Doc docs/strategy/2026-09-28-shipsync3.md.

---

## 2026-09-28 (user, ~14:15Z): vrp17_k2hb 56643352 — RETIRED (FIFO) by vrp19w_k2wide 56649892 09-28 ~19:10Z (tree + tarball removed from submission/ at SHIPSYNC4)

| | vrp17_k2hb (master config) | vrp15_k2fire |
|---|---|---|
| Kaggle submission | **56643352** | **56634350** (unchanged) |
| Tarball | dist/vrp17_k2hb.tar.gz md5 11fd0f57e33acac6a53a78a2e85491a4 (1,161,963 B, 31 files) | dist/vrp15_k2fire.tar.gz md5 1929f224b19f24b16e1d85f1a6740b26 (1,161,399 B, 31 files) |
| Recipe | vrp15_k2fire + HANDBACK at day 18: on KERNEL2-fired seats (rival h1 cash 26/29/2,338/2,438) the V56 kernel runs the farm until the dawn of day 18, then PFS's planner takes it back (`KERNEL2_HANDBACK_DAY = 18`). Unfired seats = vrp15_k2fire = vrp12_pfs byte-identical. Differs from vrp15_k2fire only in kagg3/agent/runtime.py + kagg3/core/plan.py | vrp12_pfs + KERNEL2 v3 (FIRE_CASH whitelist, lazy V56) |
| Source commit | **a7fcad46** (ship_vrp17_k2hb: 5f29b272 handback1, ec2a6042 config, a7fcad46 pins/tests), fast-forwarded into master 19819373 -> a7fcad46; tests/_pin.SHIPPED = ec2a6042 | 796c979d (config b78bf1e4) |
| Theta / head / eswork | theta7659 94a8ffd2, head_940 769ff15e, eswork_theta 6928257a (unchanged from vrp15_k2fire) | same |
| Evidence | docs/strategy/2026-09-28-handback2.md, -judge17b.md, -freshb1.md, -packhb1.md | docs/strategy/2026-09-28-judgemh4v2.md, -packv3.md |

Gene block (S/actionrl/live_expert.py SWITCHES, == plan defaults):
`OPEN_PUMP_ON=True,TAIL_FILL_ON=True,BANK_BEFORE_LOT_ON=True,HIRE_ROW_ON=True,brain.MELON_GENE_ON=True,brain.CROP_DAY_ON=True,ENDROUTE_ON=True,ENDROUTE2_ON=True,ENDROUTE2_SPLIT_ON=True,ENDROUTE_ROW2_ON=True,CLIP_CAP_ON=False,WIDE_PICK_ON=True,CARE_FILL_ON=True,OVERFLOW_GUARD_ON=True,OVERFLOW_GUARD_V2=True,OVERFLOW_GUARD_V3=True,LATE_EXEC_ON=True,ROUTE_VRP_ON=True,ROUTE_VRP_FIX_FROZEN=True,ROUTE_VRP_VERIFY=True,ROUTE_VRP_NEEDS_FIX_ON=True,ROUTE_VRP_REPAIR_ON=True,PLACEFEED_ON=True,PF_PUMPSAFE_ON=True,KERNEL2_ON=True,KERNEL2_NOOP_H0=False,KERNEL2_INHERIT=True,KERNEL2_FIRE_CASH=26|29|2338|2438,KERNEL2_PRELOAD=False,KERNEL2_HANDBACK_DAY=18`

vrp12_pfs 56612145 RETIRED (FIFO). Final pair (RULES1: Bradley-Terry over Oct 1-15 games of the last 2 uploads before
09-30 23:59Z) = vrp15_k2fire 56634350 + vrp17_k2hb 56643352. Package B (vrp17b_k2hbsafe, f4cfb272/b1ededbb) was NOT uploaded
and is not on master.
Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ = the vrp17_k2hb tarball
(31 files, cmp-identical); submission/vrp15_k2fire/ = the vrp15_k2fire tarball tree (31 files, cmp-identical); both tarballs
alongside (submission/vrp17_k2hb.tar.gz, submission/vrp15_k2fire.tar.gz); submission/vrp12_pfs/ and its tarball removed.
SHIPSYNC2: all 27 kagg3/ files of the tarball are byte-identical to master src/kagg3 (incl. v56kernel.py, route_vrp_c.so,
eswork_theta.npy); plan.py KERNEL2_HANDBACK_DAY = 18, KERNEL2_FIRE_CASH = "26|29|2338|2438"; main.py ==
scripts/package_submission.main_source(residual=True, kernel2=True); engine.lock.json == vendor/engine.lock.json.
Doc docs/strategy/2026-09-28-shipsync2.md.

---

## 2026-09-28 (user, ~08:20Z): vrp15_k2fire 56634350 — RETIRED (FIFO) by vrp18_k2hb2046 56646827 09-28 ~16:35Z (pair vrp12_pfs + vrp15_k2fire superseded 09-28 ~14:15Z)

| | vrp15_k2fire (master config) | vrp12_pfs |
|---|---|---|
| Kaggle submission | **56634350** | **56612145** (unchanged) |
| Tarball | dist/vrp15_k2fire.tar.gz md5 1929f224b19f24b16e1d85f1a6740b26 (1,161,399 B, 31 files) | dist/submission_res940_vrp12_pfs.tar.gz md5 2532e456d049577c30cad256ad1a2e07 (531,777 B, 30 files) |
| Recipe | vrp12_pfs + KERNEL2 v3: the V56 kernel takes the farm at step 1 only if the rival's h1 cash is exactly 26, 29, 2,338 or 2,438 (fires on ~9 % of our live games; unfired = vrp12_pfs byte-identical). Differs from vrp12_pfs in main.py (kernel2 act splice), kagg3/agent/runtime.py, kagg3/core/plan.py, + kagg3/agent/v56kernel.py | vrp10_esw + PLACEFEED_ON, PF_PUMPSAFE_ON |
| Source commit | **796c979d** (ship_vrp15_k2fire: 2d959515 k2lazy, b78bf1e4 config, 796c979d pins/tests), fast-forwarded into master 942b46cb -> 796c979d; tests/_pin.SHIPPED = b78bf1e4 | dcacbd33 |
| Theta / head / eswork | theta7659 94a8ffd2, head_940 769ff15e, eswork_theta 6928257a (unchanged from vrp12_pfs) | same |
| Evidence | docs/strategy/2026-09-28-judgemh4v2.md (incl. V3BRANCH1 §3c, bea5f30c), -packv3.md, -pkgpool1.md, -decision-brief.md | docs/strategy/2026-09-27-placefeed3.md |

Gene block (S/actionrl/live_expert.py SWITCHES, == plan defaults):
`OPEN_PUMP_ON=True,TAIL_FILL_ON=True,BANK_BEFORE_LOT_ON=True,HIRE_ROW_ON=True,brain.MELON_GENE_ON=True,brain.CROP_DAY_ON=True,ENDROUTE_ON=True,ENDROUTE2_ON=True,ENDROUTE2_SPLIT_ON=True,ENDROUTE_ROW2_ON=True,CLIP_CAP_ON=False,WIDE_PICK_ON=True,CARE_FILL_ON=True,OVERFLOW_GUARD_ON=True,OVERFLOW_GUARD_V2=True,OVERFLOW_GUARD_V3=True,LATE_EXEC_ON=True,ROUTE_VRP_ON=True,ROUTE_VRP_FIX_FROZEN=True,ROUTE_VRP_VERIFY=True,ROUTE_VRP_NEEDS_FIX_ON=True,ROUTE_VRP_REPAIR_ON=True,PLACEFEED_ON=True,PF_PUMPSAFE_ON=True,KERNEL2_ON=True,KERNEL2_NOOP_H0=False,KERNEL2_INHERIT=True,KERNEL2_FIRE_CASH=26|29|2338|2438,KERNEL2_PRELOAD=False`

vrp10_esw 56600971 RETIRED (FIFO). Final pair (RULES1: Bradley-Terry over Oct 1-15 games of the last 2 uploads before
09-30 23:59Z) = vrp12_pfs 56612145 + vrp15_k2fire 56634350. **NO further uploads.**
Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ = the vrp15_k2fire tarball
(31 files, cmp-identical); submission/vrp12_pfs/ = the vrp12_pfs tarball tree (30 files, cmp-identical); both tarballs alongside.
SHIPSYNC1: all 27 kagg3/ files of the tarball are byte-identical to master src/kagg3 (incl. v56kernel.py, route_vrp_c.so,
eswork_theta.npy); main.py == scripts/package_submission.main_source(residual=True, kernel2=True); engine.lock.json ==
vendor/engine.lock.json. Doc docs/strategy/2026-09-28-shipsync1.md.

---

## 2026-09-27 (user, ~15:10Z): vrp12_pfs 56612145 replaces vrp9_cs 56600958 — pair vrp10_esw 56600971 + vrp12_pfs 56612145 (superseded 09-28 08:20Z)

| | vrp12_pfs (master config) | vrp10_esw |
|---|---|---|
| Kaggle submission | **56612145** | **56600971** (unchanged) |
| Tarball | dist/submission_res940_vrp12_pfs.tar.gz md5 2532e456d049577c30cad256ad1a2e07 | dist/submission_res940_vrp10_esw.tar.gz md5 73f4af9a2e6a2e2b2c4cd6e7a84747e1 |
| Recipe | vrp10_esw + plan.py `PLACEFEED_ON = True`, `PF_PUMPSAFE_ON = True` (only kagg3/core/plan.py differs) | see below |
| Source config commit | dcacbd33 (ship_vrp12_pfs, merged into master); tests/_pin.SHIPPED = dcacbd33 | a4c5cc9e |
| Evidence | docs/strategy/2026-09-27-placefeed3.md, -placefeed3-upload-plan.md, -bandleg1.md | docs/strategy/2026-09-27-esship1.md |

vrp9_cs 56600958 RETIRED (FIFO). Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ =
the vrp12_pfs tarball (now submission/vrp12_pfs/); submission/vrp10_esw/ and its tarball removed at SHIPSYNC1 (retired).
SRCSYNC2: master src/kagg3 == vrp12_pfs tarball kagg3/ byte-for-byte (`diff -r`: 0 lines except src-only es/, sim/,
agent/opening.py).

---

## 2026-09-27 (user, ~07:45Z): the final pair (superseded 15:10Z) — vrp10_esw 56600971 + vrp9_cs 56600958

Rules (RULES1): the final rating = Bradley-Terry over the Oct 1-15 games of the LAST 2 uploads before 09-30 23:59Z. These
two are that pair (vrp7 56572961 and vrp8_jit 56580780 retire FIFO). Both beat live vrp8_jit on every leg, gift-free, and do
not combine (G30D: g30 + CARE_RIDE / + SLIVER lose own purse), so they ship as two packages.

| | vrp10_esw (master config) | vrp9_cs |
|---|---|---|
| Kaggle submission | **56600971** | **56600958** |
| Tarball | dist/submission_res940_vrp10_esw.tar.gz md5 73f4af9a2e6a2e2b2c4cd6e7a84747e1 (530,070 B) | dist/submission_res940_vrp9_cs.tar.gz md5 cd94b3342dce0f238046901a896d8040 (528,299 B) |
| Recipe | vrp8_jit tarball + `kagg3/core/eswork_theta.npy` (ESWORK1 run2 g30 candidate, md5 6928257a) loaded as `plan.ESWORK_THETA` | vrp8_jit tarball + plan.py `CARE_RIDE_ON = True`, `SLIVER_ON = True` (S/stackjit1/pkg.py) |
| Source config commit | selfplay1 a4c5cc9e (plan.ESWORK_THETA = shipped file; tests/_pin.SHIPPED = a4c5cc9e) | same tree with ESWORK_THETA None + the two switches True |
| Theta / head | theta7659 md5 94a8ffd2, head_940 md5 769ff15e (both) | same |
| Legs vs vrp8_jit | dev100 0 flips dours +638 t 5.1, held100 +3, FRESH300 +6 (+522 t 6.2), tapes +2, faithful +2, bed +2, banked live losses +12/-0 | bed +4, dev +1, held +2, FRESH600 +7 (t 6.2), tapes +6/-0, faithful +1 |
| Real-engine row (dev board 0 seat 0) | 80,321 / 74,385 | 79,477 / 74,767 |
| Evidence | docs/strategy/2026-09-27-esship1.md | docs/strategy/2026-09-27-stackjit2.md, -vrp9cs-upload-plan.md |

Payload here: submission/{main.py,theta.npy,engine.lock.json,residual_head.npz} + kagg3/ tree = the vrp10_esw tarball;
submission/vrp9_cs/ = the vrp9_cs tarball's plan.py-bearing tree; both tarballs alongside.
Known drift (SRCSYNC1, open): src/kagg3 on master is NOT byte-equal to the tarballs' kagg3/ (packages since vrp8 were
built by patching the previous tarball); the tarball trees in submission/ are the authoritative uploaded code.


---

# Earlier uploads (record kept)

## Re-upload 2026-09-17 (user, recorded 07:51Z) — same two packages, fresh first-20 draws

| | |
|---|---|
| lot4t17_slotprio_ft2 (SHIPPED package, unchanged) | **56298246** (replaces 56284867, which was 71W-8L 1,754 at the floor); tarball submission_flow193_g100_hr_lot4t17_slotprio_ft2.tar.gz md5 ab1acb76, ship-ft2 c5f68ac; feed 07:51Z 8W-0L 1,483 |
| lot4t17_slotprio (control, unchanged) | **56298238** (replaces 56277270, 105W-37L 1,900); tarball submission_flow193_g100_hr_lot4t17_slotprio.tar.gz md5 b3c33bbf, ship-slotprio d3716e6; feed 07:51Z 8W-0L 1,277 |

Rationale: docs/strategy/2026-09-17-ratingpath.md + -earlyloss.md — landing rating = f(game of first loss), P(20-0) ≈ 0.08 per upload; no code change, tests/_pin.SHIPPED stays c5f68ac.

## Previous upload (2026-09-16)

| | |
|---|---|
| Kaggle submission | 56284867 (B + LOT4 ON at turn 17 + SELL_SLOT_PRIORITY ON + FERT_TIMING ON (2-day look-ahead), 'lot4t17_slotprio_ft2'), user upload recorded 2026-09-16T17:58Z |
| Tarball | submission_flow193_g100_hr_lot4t17_slotprio_ft2.tar.gz, md5 ab1acb765945a71207f4a0f917c419e3 |
| Source commit | ship-ft2 33ef484 (master 463ee05 + FERT_TIMING_ON=True 6a6119c + packager ships agent/tell.py 2482766), fast-forwarded into master: every kagg3/*.py in the tarball is byte-identical to src/kagg3 at that commit (plan.py diff -q verified) |
| Theta | flow193_g100_hr, 6,789 float32, unchanged (theta.npy md5 7fcf3948); layout 7,428 (sw block + g12 zero-padded, inert) |
| Switches | FERT_TIMING_ON=True, FERT_TIMING_DAYS=2 (new); SELL_SLOT_PRIORITY_ON=True; LOT4_ON=True, LOT4_TURN=17; OPEN_PUMP_ON=True, TAIL_FILL_ON, BANK_BEFORE_LOT_ON, HIRE_ROW_ON as before |
| Evidence | docs/strategy/2026-09-16-fertengine.md + docs/strategy/2026-09-16-upload-ft2.md: increment over the pair POOLED180 +2,770/game t 29.5 (15 flips for, 0 against), V45LEG +2,382 t 11.3, ENG22 +1,702 t 6.1; retention 9/9 ≥ 0.85; smoke coin-exact |

Rule (user, 2026-09-11): master is always identical to the latest agent code uploaded to Kaggle and
carries all production code we run. A new upload = fast-forward or merge master to the ship commit,
replace this directory with the new tarball payload, update this table.

## Other live submission

Kaggle keeps two active submissions. 56284867 replaced **lot4t17 56276165** (verified 18:57Z off the episode feed: no new completed game in 30 min while both others played), leaving **lot4t17_slotprio 56277270 as the control**. Feed 18:57Z: FT2 14W-2L 1336 climbing; control 63W-18L 1780.

| | |
|---|---|
| lot4t17_slotprio (control) | 56277270, submission_flow193_g100_hr_lot4t17_slotprio.tar.gz md5 b3c33bbf; ship-slotprio d3716e6; docs/strategy/2026-09-16-upload-slotprio.md |

Earlier (2026-09-16 11:52Z): Kaggle keeps two active submissions. VERIFIED 2026-09-16 11:52Z off the episode feed: 56277270 replaced
**pump-off 56273500** (its newest episode id 109648545 is below the others' 109653181+, so it stopped
receiving games at 41W-13L, rating 2007). **lot4t17 56276165 is the surviving control** (18W-4L, 1801.5
at 11:52Z; 56277270 itself 8W-0L, 1349.8).

| | |
|---|---|
| lot4t17 | 56276165, dist/submission_flow193_g100_hr_lot4t17.tar.gz md5 0ff30cea; ship-lot4 3fb406b; docs/strategy/2026-09-16-upload-lot4.md |
| pumpoff (REPLACED by 56277270) | 56273500, dist/submission_flow193_g100_hr_pumpoff_live56273500.tar.gz md5 890b489d; d0e469d; docs/strategy/2026-09-16-upload-pumpoff.md; OPEN_PUMP family closed at §115b (2026-09-16-pumpoff3.md) |
