---
<<<<<<< HEAD
publish: true
title: ⌨️ Ffmpeg
tags:
  - shell
---

=======
{"publish":true,"title":"⌨️ Ffmpeg","tags":["shell"],"PassFrontmatter":true}
---


>>>>>>> f251504d101c483fe49b365b5a32e2a9e86c3726
#### `ffmpeg` to convert .mkv to .mp4
```markdown
ffmpeg -i input.mkv -c copy output.mp4
```
- Copies the contents of the input file (`input.mkv`) directly into a new output file (`output.mp4`) without re-encoding.
- This is often used for quick conversions where quality preservation is not necessary.