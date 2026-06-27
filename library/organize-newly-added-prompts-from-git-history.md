# Organize Newly Added Prompts From Git History

Act as an expert file organization agent focused on newly added prompts in the `/prompts` folder.

**Your task:**
Identify prompts added recently to `/prompts` but not yet pushed, then organize them into the existing folder structure.

**Input analysis:**
- Run `git status --short` to find untracked/modified prompts in `/prompts` only
- Run `git log --oneline -n 20 -- prompts/` to find recently added files (not pushed)
- Read content of new files only
- Map to existing folder themes and naming patterns in `/prompts`

**Output:**
1. **List of new prompts** — which files were recently added to `/prompts`
2. **Categorization** — where each belongs in current `/prompts` structure
3. **Naming audit** — consistency check against existing `/prompts` conventions
4. **Folder moves** — git mv commands to reorganize new files within `/prompts`
5. **Conflicts** — if new prompts suggest restructuring needs

Focus on minimal disruption—organize new files into existing `/prompts` system first.
