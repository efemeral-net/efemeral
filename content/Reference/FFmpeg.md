---
publish: true
title: ⌨️ Ffmpeg
tags:
  - shell
---

#### `ffmpeg` to convert .mkv to .mp4
```markdown
ffmpeg -i input.mkv -c copy output.mp4
```
- Copies the contents of the input file (`input.mkv`) directly into a new output file (`output.mp4`) without re-encoding.
- This is often used for quick conversions where quality preservation is not necessary.