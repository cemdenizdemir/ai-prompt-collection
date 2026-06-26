# ai-prompt-collection

A curated collection of prompts for AI tools — organized by category, ready to copy and use.

---

## Structure

Prompts are organized in a `[category]/[sub-category]` structure.

```
prompts/
├── media/
│   ├── image/
│   ├── video/
│   └── audio/
├── coding/
│   ├── frontend/
│   ├── backend/
│   ├── devops/
│   ├── debugging/
│   ├── review/
│   └── docs/
├── writing/
│   ├── creative/
│   ├── copywriting/
│   ├── email/
│   ├── social/
│   └── essay/
├── research/
│   ├── analysis/
│   ├── fact-check/
│   └── learning/
├── data/
│   ├── sql/
│   ├── transform/
│   └── viz/
├── roleplay/
│   ├── persona/
│   └── simulation/
├── productivity/
│   ├── planning/
│   ├── summarize/
│   └── template/
└── system/
    ├── agent/
    └── meta/
```

---

## Each Prompt File

Every prompt is a `.md` file named in `kebab-case`.

```
prompt-title
![image](/image.png)   ← only present for media generation prompts
prompt text...
```

---

## Contributing

1. Fork the repo
2. Add your prompt as a `.md` file under the correct `category/sub-category` folder
3. Name the file in `kebab-case` matching the prompt title
4. Open a pull request

If you have an image of a prompt, use the [media-prompt-extractor](prompts/system/meta/media-prompt-extractor.md) to generate the file automatically.

---

## License

[MIT](LICENSE)