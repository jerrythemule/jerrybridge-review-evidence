# JerryBridge V14 Repair4 — Sanitized Primary Evidence Export

## Provenance
Source surface: authenticated GitHub connector read of private repository `jerrythemule/jerry-remote-bridge` on 2026-09-27. This file is a sanitized transcription/export for public independent review. Local filesystem paths are omitted.

## Exact candidate identity
Private issue #3027, terminal result comment `5857578945`:
- UTC: `2026-09-27T16:15:56.913333+00:00`
- result schema: `JERRY-BRIDGE-RESULT-v3`
- `ok: true`, `returncode: 0`, `timed_out: false`
- ZIP bytes: `5392455`
- ZIP SHA-256: `ec259fb910d231b6797b027a705be5c2a0d6b1ecc857820297cf4bf52ff3aa59`

Private issue #3028, terminal result comment `5857581973`:
- UTC: `2026-09-27T16:16:21.761304+00:00`
- `ok: true`, `returncode: 0`, `timed_out: false`
- installer bytes: `15105`
- installer SHA-256: `dc130f92ef94970246603126ccaadb51c0fe5be335bf8ce535ea6d51945deafe`

## Install/restart chain
Private issue #3029:
- malformed invocation
- terminal `ok: false`, `returncode: 1`
- Python `NameError`
- this is not represented as successful installation evidence.

Private issue #3030:
- corrected installer invocation
- terminal `ok: true`, `returncode: 0`
- installer reported `APPLIED_PENDING_RESTART` with restart deferred
- transaction: `ec5d764058224c218441b00fe390cfd6`
- backup manifest SHA-256: `4fb44800d0e17828a88593ea69d0d6a615b87575ec1e615252d4ca6396138f33`

Private issue #3031:
- observed status `APPLIED_PENDING_RESTART`
- transaction remained `ec5d764058224c218441b00fe390cfd6`
- upgrade ID `jerrybridge-v14-20260926`
- pre-upgrade instance `b2f20b66c23e4c5da424a0b75426deb9`
- no restart request, restart processing, or maintenance lock at that observation
- runtime hashes listed below matched later #3035/#3051.

Private issue #3032:
- authorized continuation/restart handoff
- terminal `ok: true`, `returncode: 0`

Private issue #3034:
- observed status `APPLIED_PENDING_RESTART`
- restart intent `automatic`
- restart request ID `870a69a0ee254642b72f60be17d1f9b0`
- same transaction and upgrade ID
- restart processing present at that observation; request/result/maintenance-lock absent

## Post-restart health
Private issue #3035:
- terminal `ok: true`, `returncode: 0`
- upgrade ID: `jerrybridge-v14-20260926`
- status: `HEALTHY`
- `healthy_by: replacement-worker`
- healthy instance: `ab9aca6a391446089cc86d730fc966db`
- stopped/pre-upgrade instance: `b2f20b66c23e4c5da424a0b75426deb9`
- restart request ID: `870a69a0ee254642b72f60be17d1f9b0`
- transaction: `ec5d764058224c218441b00fe390cfd6`
- backup manifest SHA-256: `4fb44800d0e17828a88593ea69d0d6a615b87575ec1e615252d4ca6396138f33`
- heartbeat: last poll OK, no error, inflight 0, queued 0, preexec retry empty
- restart request/processing/result and maintenance lock absent at final observation

### Runtime hashes observed at #3031, #3035 and #3051
- `bridge.py`: `e29f2e49da560fe81089f1826bc66ff58d873a158a7e254496f7fd922d00281c`
- `jerry_transport.py`: `6f4b4182ccac24d25714ba2558dd04507c9aa0278834f4c1f4017743187e4d48`
- `phase4_ops.py`: `a0c9f046ed2d41d601246498f99ee9127536e43aa9423077c06c7734f851c81f`
- `Restart-Jerry-Remote-Bridge.ps1`: `6b239e87f7753f06cc6646638ef668d971909afc937a72c777acb52d61ad4fb7`
- `Watch-Jerry-Remote-Bridge.ps1`: `53c00e3c1bcb81a161b9fbb335c3820386d5d49be7f45092bcfae4f2c7a50d0c`
- `Run-Restart-Request.ps1`: `ca8e99656d61fe30c0f3b7aa044b7d1916d5b3a452ffd9dbbdc2e66604bc2a8b`

## Post-install execution observations
Terminal timestamps from private issue records:
- #3039: admitted `16:20:28.574418Z`; terminal `16:20:31.074954Z`; `ok:true`
- #3040: admitted `16:20:33.237158Z`; terminal `16:20:38.904754Z`; `ok:true`
- #3041: admitted `16:20:34.451789Z`; terminal `16:20:39.970641Z`; `ok:true`
- #3042: admitted `16:20:42.383618Z`; terminal `16:20:47.853854Z`; `ok:true`
- #3043: admitted `16:21:00.410519Z`; terminal `16:21:04.910755Z`; `ok:true`
- #3044: admitted `16:21:08.345342Z`; terminal `16:21:11.841604Z`; `ok:true`
- #3045: admitted `16:21:08.504182Z`; terminal `16:21:12.173106Z`; `ok:true`
- #3046: admitted `16:21:16.104762Z`; terminal `16:21:19.568112Z`; `ok:true`
- #3047: admitted `16:21:16.153995Z`; terminal `16:21:19.653295Z`; `ok:true`
- #3048: admitted `16:21:16.436284Z`; terminal `16:21:19.992486Z`; `ok:true`

The timestamps establish overlap for #3040/#3041, #3044/#3045, and #3046–#3048. They do not establish #3042 as concurrent with #3040/#3041.

## Intentional timeout containment
Private issue #3050, terminal result comment `5857621044`:
- command SHA-256: `04e27b8c2c7e173ba468e946e1cc03a37b53e268a229005ed445348fd299f4d2`
- terminal UTC: `2026-09-27T16:21:46.431877+00:00`
- `ok: false`
- `returncode: null`
- `timed_out: true`
- `timeout_seconds: 1`
- issue ended with `jerry-error`
This was an intentional command that slept longer than its one-second timeout.

## Final integrity after timeout
Private issue #3051:
- admission comment `5857624224`: UTC `2026-09-27T16:22:12.126646+00:00`, schema `JERRY-BRIDGE-ADMISSION-v1`, command SHA-256 `a2d59177cd037b95a2997a3f8131df9e4c055adb6f164c598d136832b4b90e11`
- terminal comment `5857624304`: UTC `2026-09-27T16:22:12.880073+00:00`, schema `JERRY-BRIDGE-RESULT-v3`, `ok:true`, `returncode:0`, `timed_out:false`
- stdout reported:
  - `LIFECYCLE jerrybridge-v14-20260926 HEALTHY ab9aca6a391446089cc86d730fc966db`
  - `HEARTBEAT True None 0 0 []`
  - restart request: absent
  - restart processing: absent
  - restart result: absent
  - maintenance lock: absent
  - all six runtime hashes identical to the #3031/#3035 observations above

## Evidence-bounded interpretation
These exported records support the proposition that the recorded JerryBridge workflow identified the exact Repair4 candidate, completed the corrected install/restart sequence, reported a replacement worker as HEALTHY, processed multiple subsequent commands including overlapping executions, contained an intentional timeout, and subsequently reported HEALTHY state with unchanged runtime hashes.

They do **not** give a public reviewer authenticated access to the private source issues or direct access to the live host. A reviewer should not convert this public export into a claim of independently witnessed machine execution.

No record in this bounded export demonstrates a post-Repair4 defect requiring a Repair5.
