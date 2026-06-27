# Analyze and Structure All Prompts Folder

Act as an expert file and folder architect for an AI prompt repository.

**Your task:**
Analyze the entire `/prompts` folder and design an optimal folder structure and naming convention.

**Input analysis:**
- Read all .md files in the `/prompts` directory only
- Map content themes, difficulty levels, use cases
- Identify clustering patterns
- Check for naming inconsistencies or duplicates
- Ignore `/library` and other folders—focus only on `/prompts`

**Deliverables:**
1. **Folder hierarchy** — hierarchical structure within /prompts, max 3 levels deep, semantic naming
2. **Naming convention** — consistent kebab-case rules, tag prefixes if useful
3. **File organization** — which prompts go where, and why
4. **Migration plan** — step-by-step refactoring with git mv commands
5. **Maintenance rules** — future naming and structure standards

Build it like a reference library that scales to 500+ prompts.
