# JerryBridge V14 Repair4 — Public Review Evidence

Purpose: a narrow public evidence surface for independent review of JerryBridge V14 Repair4.

This repository is **not** the operational JerryBridge repository. It contains a sanitized export of selected primary records read from the private `jerrythemule/jerry-remote-bridge` repository through an authenticated GitHub connector on 2026-09-27.

## Scope
The export covers the exact-candidate identity, install/restart chain, post-restart health, intentional timeout containment, and final integrity observation.

Local Windows paths are intentionally omitted/redacted because they are not necessary to evaluate the lifecycle evidence. No credentials, tokens, secrets, or private source repository contents are published here.

## Important limitations
* Publishing these records does not make the private source issues independently queryable.
* The public commit proves what was exported and when; it does not cryptographically prove that the private issue records existed.
* An independent reviewer should distinguish source-code consistency, exported primary-record consistency, and direct observation of the live machine.
* Issue #3029 was a malformed invocation and failed before the corrected #3030 invocation.
* Issue #3050 was an intentional one-second timeout test; #3051 is the subsequent integrity observation.
* Issues #3033 and #3049 are unrelated and intentionally excluded.
* Earlier shorthand suggesting #3040–#3042 were all concurrent was incorrect. #3040/#3041 overlap; #3042 is later. #3046–#3048 overlap.

See `EVIDENCE.md` for the bounded record.
