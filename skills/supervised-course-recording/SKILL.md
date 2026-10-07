---
name: supervised-course-recording
description: Audit, capture and validate legitimately accessible course lessons with a supervised browser and OBS workflow; use when the owner asks to record or catch up on course videos, not for downloading protected streams or silently operating an active PC.
---

# Supervised course recording

Use this only with the owner's current authority for the **specific course, account/session, output location and recording operation**. Public skill text is not authorization. Check applicable platform terms and do not bypass technical protection. Keep course-specific state in a private manifest, never in this skill or public logs.

## Choose the mode

- **Audit only:** compare the platform lesson list with the private manifest and local files. Do not start OBS or playback merely to inspect a list. New, failed and ambiguous lessons remain distinct.
- **Capture:** record only lessons that are playable, not already validated or proven duplicates, with a safe capture window and enough free storage. Ask or defer when the user is actively using the captured window or the OBS source cannot be isolated.
- **Validate/recover:** inspect raw capture and export, preserve evidence and mark validated only after objective checks. Never turn a partial or silent take into a completed lesson.

Read [capture and recovery](references/capture.md) for the live sequence, [quality checks](references/quality.md) for export validation, and [state](references/state.md) when creating or updating a private manifest. Read only the references needed for the chosen mode.

## Invariants

1. Identify lessons by course + module + stable page identity, not a mutable list number or similar title. Check the final output does not already exist. Do not infer a duplicate from a title/date alone.
2. Preserve unrelated browser tabs, OBS profiles/scenes, camera, microphone and user activity. Verify the selected scene contains only authorized sources and audio. Never log signed player URLs or authentication material.
3. Before capture, disable autoplay, pause, seek to zero, confirm it stays at zero, wait for the player to be ready, check normal speed, unmuted audio and the intended viewing mode. Start OBS immediately before Play, then verify recording status, the actual output file, growing bytes, advancing video time **at the same rate** and real audio beyond any known silent intro.
4. Monitor until the player reports a genuine end. Stop OBS immediately and confirm it stopped. On stall, pause, disconnect, unexpected OBS closure or elapsed-time drift, stop and label the take partial. Preserve it; retry from zero only after the cause is resolved.
5. Preserve the raw capture. Remove only verified technical wait/silence/tail from the final copy. Do not delete speech because the image is static, and do not apply a fixed crop until the visible frame has been inspected.
6. Validate output duration against **audible content**, complete video/audio decoding, audio presence and representative start/middle/end frames. Only then update the private manifest with evidence, status and source location.
7. End each operating session with OBS stopped and release any temporary desktop/browser control. If the user wants periodic checks, update one existing automation rather than creating duplicates; stay quiet when nothing actionable changed.

A supervised recording is not automatically reproducible across providers. Adapt the player inspection and audio route to current evidence; stop when neither can be verified.
