---
"openfilm": patch
---

Exact frames (render, look, Studio's exports): a video's frame on screen is told by how long its frames last, which the host reads with ffprobe. A video woken ahead while hidden, then shown, no longer leaves its old frame in the picture: shown again after the seek, it was taken for the sought one, and an export could hold a frame from the clip's start. Footage whose next frame is the same source frame (24 fps footage in a 30 fps export) no longer waits seconds for a frame that never comes: such a film exports several times as fast.
