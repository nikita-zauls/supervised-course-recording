---
name: supervised-course-recording
description: Audit, capture and validate legitimately accessible course lessons with a supervised browser and a verifiable recorder (OBS preferred); use for authorized course recording or catch-up, not protected-stream extraction or unattended PC takeover.
---

# Supervised course recording

Use this only with the owner's current authority for the **specific course, account/session, output location and recording operation**. A provided browser and recorder do not themselves grant access, capture or publication permission. Check applicable platform terms; do not bypass technical protection. Keep course-specific state in a private manifest, never in this skill or public logs. Ask only for a decision that cannot be safely inferred or verified (for example access, capture scope, administrator approval, or an incompatible audio route), one focused question at a time. Do not promise universal unattended operation.

## Choose the mode

- **Audit only:** compare the platform lesson list with the private manifest and local files. Do not start OBS or playback merely to inspect a list. New, failed and ambiguous lessons remain distinct.
- **Capture:** record only lessons that are playable, not already validated or proven duplicates, with an isolated capture window and enough free storage. OBS is preferred, not mandatory: use another recorder only if its start, active, output, audio and stop states can be observed. Defer if the user's activity or private windows could enter the capture.
- **Validate/recover:** inspect raw capture and export, preserve evidence and mark validated only after objective checks. Never turn a partial or silent take into a completed lesson.

Read [capture and recovery](references/capture.md) for the live sequence, [recorder and audio adapters](references/adapters.md) when selecting or troubleshooting a recorder/audio route, [quality checks](references/quality.md) for export validation, and [state](references/state.md) when updating a private manifest. Read only the references needed for the chosen mode.

## Invariants

1. Identify lessons by course + module + stable page identity, not a mutable list number or similar title. Check the final output does not already exist. Do not infer a duplicate from a title/date alone.
2. Preserve unrelated browser tabs, recorder profiles/scenes, camera, microphone, default audio devices and user activity. Verify the dedicated capture contains only authorized video and audio. Never log signed player URLs, authentication material or private browser chrome.
3. Before capture, disable autoplay, pause, seek to zero, confirm it stays at zero, wait for the player to be ready, check normal speed, unmuted audio and the intended viewing mode. Start the verified recorder immediately before Play, then verify active status, the **expected** output file, growing bytes, advancing video time **at the same rate** and captured audio during an actually audible section. A silent introduction alone is not a failed audio route.
4. Monitor until the player reports a genuine end; stop and verify the recorder stopped. Use bounded checks and retries. On stall, pause, disconnect, unexpected recorder closure, unknown output, privacy leak or elapsed-time drift, stop the affected take and label it partial. Preserve it; retry from zero only after the cause is resolved. Never leave a recorder running between turns.
5. Preserve the raw capture. Remove only verified technical wait/silence/tail from the final copy. Do not delete speech because the image is static, and do not apply a fixed crop until the visible frame has been inspected.
6. Validate output duration against **audible content**, complete video/audio decoding, audio presence and representative start/middle/end frames. Only then update the private manifest with evidence, status and source location.
7. End each operating session with the recorder stopped and release temporary computer control; merely closing an agent control session must not close the user's browser or recorder. If periodic checks are requested, update one existing automation rather than creating duplicates; respect the requested capture day and stay quiet when nothing actionable changed.

A supervised recording is not automatically reproducible across providers. Adapt the player and recorder to their observed capabilities; if a required state cannot be checked, do not silently substitute guesses.
