---
{"publish":true,"title":"⌨️🐍 Videogrep","tags":["shell","python"],"PassFrontmatter":true}
---


=======
{"publish":true,"title":"⌨️🐍 Videogrep","tags":["shell","python"],"PassFrontmatter":true}
---


>>>>>>> f251504d101c483fe49b365b5a32e2a9e86c3726
[Videogrep](https://github.com/antiboredom/videogrep) makes automatic video supercuts with [Python].

#### `videogrep` with Search Parameters
```markdown
videogrep -i 'input_file.mkv' --search 'keyword' --search 'alternative_keyword' -r -o output_file.mp4
```
- Searches for videos containing both specified keywords (case-insensitive) in the input file (`input_file.mkv`) and outputs a new video file (`output_file.mp4`).
- The `-r` flag enables reverse search.
- The `[number]` placeholder can be used to specify a range of timestamps for each search result, but it is not used in this example.

#### `videogrep` with Multi-Search Parameters
```markdown
videogrep -i 'input_file.mkv' --search 'keyword1' --search 'keyword2' -r -o output.mp4
```
- Performs a search for videos containing both specified keywords (`keyword1` and `keyword2`) in the input file (`input_file.mkv`) and outputs a new video file (`output.mp4`).
- The `-r` flag enables reverse search.
```markdown
videogrep -i 'rw_raw_2.mp4' --search 'theater' --search 'spiritual' -r -o spiritualtheater.mp4
```
- This is identical to the previous example, searching for videos containing both "theater" and "spiritual" keywords in `rw_raw_2.mp4` and outputting a new file named `spiritualtheater.mp4`.
