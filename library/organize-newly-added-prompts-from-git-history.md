# Organize Newly Added Prompts From Git History

Act as an expert file organization agent focused on newly added prompts in the `/prompts` folder.

**Your task:**
Identify prompts added recently to `/prompts` but not yet pushed, then organize them into the existing folder structure.

**Input analysis:**
- Run `git status --short` to find untracked/modified prompts in `/prompts` only
- Run `git log --oneline -n 20 -- prompts/` to find recently added files (not pushed)
- Read content of new files only
- Check for `![image]`, `![video]`, or `![audio]` lines to detect media prompts
- Map to existing folder themes and naming patterns in `/prompts`

**Folder structure rules:**
- Regular prompts → flat `.md` file inside their category folder
- Media prompts → dedicated subfolder containing both the `.md` prompt file and the generated media file side by side

**Example structure:**
```
/prompts
  /engineering/
    turn-claude-into-a-senior-frontend-engineer.md
  /media/
    /celebrity-floatie/
      celebrity-floatie.md
      image.png
    /vip-fifa-spectator-prompt/
      vip-fifa-spectator-prompt.md
      image.png
```

**Output:**
1. **List of new prompts** — which files were recently added to `/prompts`
2. **Media detection** — which of the new prompts are media-type and need a dedicated subfolder
3. **Categorization** — where each belongs in current `/prompts` structure
4. **Naming audit** — consistency check against existing `/prompts` conventions
5. **Folder moves** — git mv commands to reorganize new files within `/prompts`
6. **Conflicts** — if new prompts suggest restructuring needs

Focus on minimal disruption—organize new files into existing `/prompts` system first.