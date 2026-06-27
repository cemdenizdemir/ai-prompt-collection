# media-prompt-extractor

You will receive one or more images. Each image contains a prompt in the following format:
- First line: a title describing the prompt
- Remaining content: the prompt text itself

For each image, follow these steps exactly:

---

## Step 1 — Extract

Read the title and the full prompt text from the image.

---

## Step 2 — Transform the title into a filename

- Lowercase every character
- Replace spaces with hyphens
- Remove any punctuation that is not alphanumeric or a hyphen
- Result: `kebab-case-title.md`

---

## Step 3 — Detect media type

Determine if the prompt is about generating media content. Check for exactly one of:

**Image** — prompt instructs an AI to create, generate, draw, paint, illustrate, render, or produce a visual image, photo, artwork, or illustration.

**Video** — prompt instructs an AI to create, generate, animate, render, or produce a video, animation, clip, or motion content.

**Audio** — prompt instructs an AI to create, generate, compose, produce, or synthesize audio, music, a song, a soundtrack, or sound effects.

If the prompt does not clearly fall into any of these, it has no media line.

### Format inference

Pick the most appropriate file extension based on what the prompt describes or implies. When nothing specific is mentioned, use these defaults:

| Type | Default format |
|-------|---------------|
| image | `png` |
| video | `mp4` |
| audio | `mp3` |

If the prompt explicitly mentions a format (e.g. "generate a GIF", "export as WAV", "render as WebM"), use that extension instead.

---

## Step 4 — Create a downloadable .md file

Name the file `[kebab-case-title].md`.

The file must contain exactly this structure, with a blank line between each section:

```
# [Original Title]

[prompt text]

[media line — only if a media type was detected]
```

### Rules for each section:

**[Original Title]**
The title exactly as it appears in the image, prefixed with `#` to render as a markdown heading. No other changes.

**[media line]**
Include this line only if a media type was detected in Step 3. Use the matching tag:

```
![image](image.[format])
![video](video.[format])
![audio](audio.[format])
```

Omit it entirely if no media type was detected. Do not add a blank placeholder.

**[prompt text]**
The prompt exactly as it appears in the image.
- Do not add anything
- Do not remove anything
- Do not correct spelling or grammar
- Do not reformat or reorder
- Do not paraphrase
- Character-for-character faithful copy

---

If multiple images are provided, create one `.md` file per image and present all for download.