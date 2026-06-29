# Analyze and Structure All Prompts Folder

Act as an expert file and folder architect for an AI prompt repository.

**Your task:**
Analyze the entire `/prompts` folder and design an optimal folder structure and naming convention.

**Input analysis:**
- Read all .md files in the `/prompts` directory only
- Map content themes, difficulty levels, use cases
- Identify clustering patterns
- Check for naming inconsistencies or duplicates
- Detect media prompts by checking for `![image]`, `![video]`, or `![audio]` lines
- Ignore `/library` and other folders—focus only on `/prompts`

**Folder structure rules:**
- Regular prompts → flat `.md` file inside their category folder
- Media prompts → dedicated subfolder under `/media/[category]/[folder-for-files]/`, where category is the media type (e.g. `image`, `video`, `audio`)

**Example structure:**
```
/prompts
  /engineering/
    turn-claude-into-a-senior-frontend-engineer.md
    make-claude-audit-your-entire-codebase.md
  /business/
    immediate-competitive-advantage.md
  /media/
    /image/
      /celebrity-floatie/
        celebrity-floatie.md
        image.png
    /video/
      /vip-fifa-spectator/
        vip-fifa-spectator.md
        video.mp4
    /audio/
      /some-audio-prompt/
        some-audio-prompt.md
        audio.mp3
```

**Deliverables:**
1. **Folder hierarchy** — hierarchical structure within /prompts, max 3 levels deep, semantic naming
2. **Naming convention** — consistent kebab-case rules for both files and subfolders
3. **File organization** — which prompts go where, and why
4. **Migration plan** — step-by-step refactoring with git mv commands
5. **Maintenance rules** — future naming and structure standards, including media subfolder convention

Build it like a reference library that scales to 500+ prompts.