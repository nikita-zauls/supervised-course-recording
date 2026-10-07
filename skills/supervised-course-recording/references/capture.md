# Capture and recovery

## Preflight

Confirm the exact course and lesson from the page, the owner's access/retention authority, the intended destination and a unique local filename. Check free space and that the recorder is stopped. Inspect its profile/scene/source and output path without changing unrelated configuration. The capture must exclude camera/microphone and general desktop audio unless explicitly requested. A source following the user's active browser may capture unrelated activity: isolate a dedicated window/profile or defer. If a preview shows account details, messages, browser chrome with signed URLs, or any other private surface, correct the source before recording; never publish a diagnostic frame containing it.

Inspect the player through supported browser UI/DOM, never by copying a signed media URL into logs. Video duration and readiness can change after load. Disable autoplay; pause and seek to zero; wait long enough to catch resume jumps. Confirm speed 1, sound enabled, target output audio route and the intended fullscreen or player-maximized mode. A player icon or live recorder meter alone does not prove captured audio. If a separate browser/audio endpoint is used so the owner can keep working, verify both the per-app route and the actual recorded track; do not change system-wide defaults.

## Capture

Start the verified recorder just before Play. Confirm its active state, expected **new** file and byte growth, then start playback. Sample captured audio at a known audible point after any plausible silent introduction; if a short meter sample is zero, verify a raw audio sample rather than calling the lesson silent. Compare monotonic wall-clock/recording elapsed with player progress repeatedly; `paused=false`, file growth and `readyState=4` do not prove real-time playback when buffering or playback lags. Poll more frequently near the end so technical tails stay short. Do not leave a live take awaiting a future scheduled turn.

## Bounded recovery

Use explicit states: `idle → prepared → recording → stopped → validated`, with `partial` or `blocked` on failure. Give preparation, initial file creation, audio proof and progress checks finite time budgets chosen for the lesson/player; record the observed reason if one expires. A known long silent introduction changes the audio-proof checkpoint, **not** the requirement to monitor playback/bytes in the meantime. Use a short retry only after a specific transient problem has cleared; repeated identical failures need a different remedy or a user action, not an endless loop.

On player stall, unexpected pause, disconnected browser control, privacy leak, wrong output file or recorder failure, stop the recorder as soon as the state is known and preserve the raw as partial. If control is lost, independently verify/stop the recorder through its own available interface before ending the run; if that cannot be done, flag urgent user action instead of pretending it stopped. Never export a partial take as a whole lesson. Rewind and begin a fresh take only when safe. If two takes must be joined, require overlapping audio or visual evidence of alignment, inspect the splice and document the derivation. Do not guess an offset from wall time alone.

## End and handoff

Wait for a genuine end state, then stop the recorder immediately and verify stopped status and finalized file size. Preserve the source. Record lesson identity, duration, raw filename, any interruption and checks in the private manifest. If blocked by platform processing, protection, absent audio or insufficient evidence, mark **blocked/pending** with the observed reason and recheck later; do not call it omitted or complete. Release temporary computer control after use without closing the owner's apps.
