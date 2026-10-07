# Capture and recovery

## Preflight

Confirm the exact course and lesson from the page, the owner's access/retention authority, the intended destination and a unique local filename. Check free space and that OBS is stopped. Snapshot OBS profile/scene/source identity without changing unrelated scenes. The capture must exclude camera/microphone unless explicitly requested. A window source that follows the user's active browser may capture unrelated activity: isolate a dedicated window or defer.

Inspect the player through supported browser UI/DOM, never by copying a signed media URL into logs. Video duration and readiness can change after load. Disable autoplay; pause and seek to zero; wait long enough to catch resume jumps. Confirm speed 1, sound enabled, target output audio route and the intended fullscreen or player-maximized mode. A player icon or live OBS meter alone does not prove captured audio.

## Capture

Start OBS just before Play. Confirm OBS says recording, the expected new file exists and grows, and video time advances. Sample captured audio after any plausible silent introduction; if a short meter sample is zero, verify a longer raw audio sample before calling the lesson silent. Compare wall-clock/OBS elapsed with player progress repeatedly; a playing flag is insufficient when buffering or playback lags. Poll more frequently near the end so technical tails stay short.

Do not abandon a live recording between runs. On player stall, unexpected pause, disconnected browser control or OBS failure, stop OBS as soon as the state is known and preserve the raw as partial. Never export it as a whole lesson. Rewind and begin a fresh take when safe. If two takes must be joined, require overlapping audio or visual evidence of alignment, inspect the splice and document the derivation. Do not guess an offset from wall time alone.

## End and handoff

Wait for a genuine end state, then stop OBS immediately and verify stopped status and finalized file size. Preserve the source. Record lesson identity, duration, raw filename, any interruption and checks in the private manifest. If blocked by platform processing, DRM, absent audio or insufficient evidence, mark **blocked/pending** with the observed reason and recheck later; do not call it omitted or complete.
