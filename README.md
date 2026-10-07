# Supervised course recording

A portable, evidence-led procedure for capturing legitimately accessible course videos, reviewing the result and tracking what remains. OBS is preferred; another local recorder can be used only after it passes the same observable capture and stop checks. This repository contains **instructions and synthetic examples only**. It does not contain courses, credentials, browser sessions, recordings, transcripts or a running recorder.

Start with [the skill](skills/supervised-course-recording/SKILL.md). A future agent should adapt it to the actual player, recorder and audio route, and obtain the owner's current authorization before operating a browser, recorder or external account. The private state for a specific learner belongs in a separate private store. The [adapter reference](skills/supervised-course-recording/references/adapters.md) explains application-audio isolation and why a saved audio sample matters more than a mixer animation.

The procedure was distilled from repeated supervised Windows/Brave/OBS captures. Streamlabs and other recorders are capability-based adaptation paths, **not live-tested claims**. Its gates are safeguards, not a claim that it works unattended on every site. No DRM bypass or recording without permission is supported. Some sites may forbid recording under their terms; check before use.

No software license has been granted yet. Public visibility alone does not grant rights to redistribute, modify or reuse the repository outside applicable default law. The owner can add a license later after deciding its terms.
