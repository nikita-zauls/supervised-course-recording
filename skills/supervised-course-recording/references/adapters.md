# Recorder and audio adapters

Choose by **observable capabilities**, not brand. OBS is the first choice where available; Streamlabs Desktop or another local recorder is acceptable only after a short non-sensitive test proves the same contract. Instructions for OBS are based on supervised use; other recorders are supported by this contract, **not claimed live-tested by this skill**.

## Minimum recorder contract

An adapter must establish, before real playback: (1) the selected isolated visual source and excluded private sources; (2) the exact audio source and excluded mic/desktop audio; (3) an output directory and interruption-tolerant format; (4) whether recording is currently active; (5) the new file's identity and byte growth; and (6) a reliable stop/finalize action whose result can be checked. Test a short permitted sample, inspect its picture and audio, and restore the test state. If any required observation is unavailable, keep the lesson pending rather than running blind.

Do not install drivers, enable remote-control servers, change the default output device, or change another scene/profile merely to satisfy this contract. Preserve the owner's existing setup. A recorder launch may be attempted once using its supported local mechanism, then checked for process, control endpoint and output state; if it fails, diagnose the observed error or request the specific user action. Do not loop on invisible launches. Elevated changes require explicit administrator approval.

## OBS Studio

Use a dedicated scene/profile, with Window Capture plus its application audio where supported, or a separate application-audio source. OBS WebSocket is a useful **optional** status/control interface when already enabled and authorized; keep its password private and do not enable or expose it without permission. Verify that global Desktop Audio and microphone do not enter the recording track. Prefer an interruption-resilient source container such as MKV or a verified recoverable alternative, then export a separate final file. Check the OBS status and actual output, not just a red button or a moving meter.

## Streamlabs Desktop and other recorders

Streamlabs Desktop provides recording, output-path selection and application-audio capture; its recording/stream source selection and audio tracks must be inspected separately. Disable or exclude general desktop audio and mic **for this recording** so a private conversation or notification cannot enter the final file. If the recorder has no dependable status interface, a monitored UI may satisfy the contract only while the agent can confirm recording, file growth and stop; never assume OBS WebSocket commands work with another product. Do not claim support for an arbitrary recorder until its adapter test passes.

## Audio isolation while the owner uses the PC

Prefer capturing the designated browser/application audio directly. On Windows, an owner-approved **per-app** output route (for example a spare Realtek endpoint) can keep course audio away from the owner's headphones; use it only after checking that the recorder actually captures that endpoint or app. The owner listening through a headset proves the lesson has sound, **not** that the isolated recording has sound. A quiet opening can last minutes: check a known speech position or a short test that reaches the first voice. Do not record a full lesson on faith.

If per-app audio capture fails, test a separate device/source or a supported virtual route without changing system-wide defaults. Installing a virtual cable or driver may require administrator consent and must not be automatic. Check for double capture, echo, muted output, track assignment and the actual saved file. Restore a changed per-app route after the session if it was temporary and its prior value is known; otherwise disclose the remaining change rather than guessing.

Official capabilities (verify the installed version before relying on them): [OBS application audio](https://obsproject.com/kb/application-audio-capture-guide), [OBS remote control](https://obsproject.com/kb/remote-control-guide), [OBS formats](https://obsproject.com/kb/audio-video-formats-guide), [Streamlabs recording](https://streamlabs.com/content-hub/post/how-to-record-on-streamlabs-desktop-best-settings), [Streamlabs audio separation](https://support.streamlabs.com/hc/en-us/articles/360043744394-Advanced-Audio-Control-Setups).
