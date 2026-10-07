# Quality checks and export

Inspect raw boundaries before trimming. Use audio analysis **and** frame inspection: a quiet first slide can be real content, and a static image may carry speech. Seek the first verified voice/sound that belongs to the lesson; retain a small lead-in instead of cutting a consonant. Remove a tail only when frozen/silent and outside content. Never compensate for a long initial wait by cutting the end.

If source capture includes browser chrome, determine its bounds from actual frames before cropping. If chrome is inside the teacher's source video, it is part of the lesson and must not be blindly removed. Make cropping/rescaling optional and course-specific.

A Windows/OBS installation may support H.264/AAC and hardware encoding, but choose compatible export settings only after checking available encoders. Example with FFmpeg (replace paths and trim values after inspection):

```text
ffmpeg -ss <verified_start_seconds> -i <raw.mkv> -t <verified_content_seconds> -vf <optional_verified_filter> -c:v h264_nvenc -cq 25 -c:a aac -ar 48000 -ac 2 <candidate.mp4>
```

Keep the raw untouched; write a distinct candidate. `-ss`, `-t` and filter values are **not defaults**. For ordinary portability prefer settings supported by the target device, and test the actual result rather than relying on the command's exit code.

Minimum validation:

- Probe both streams and container duration; compare to observed playable/audible content, allowing documented small encoder rounding.
- Decode the **entire** candidate with errors surfaced, not only sampled frames.
- Measure audio after the technical lead-in and near the end; investigate unexpected silence, clipping or a route mismatch.
- Inspect representative first, middle and final frames and any splice/crop boundary.
- Verify the expected output name/location and retain the raw source and any failed takes.

Example checks (replace paths):

```text
ffprobe -v error -show_entries format=duration:stream=codec_name,codec_type,width,height,r_frame_rate,sample_rate,channels -of json <candidate.mp4>
ffmpeg -v error -i <candidate.mp4> -f null -
ffmpeg -hide_banner -i <candidate.mp4> -af volumedetect -vn -f null -
```

A passing probe is not proof of complete decode or meaningful audio. Report each observation separately. Never declare a lesson validated from filename presence alone.
