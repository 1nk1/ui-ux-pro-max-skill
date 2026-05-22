# Fix GitHub Issue

Read a GitHub issue, implement the fix, and create a PR.

## Usage

```
/project:fix-github-issue <issue_number>
```

## Instructions

1. Read the issue:
```bash
gh issue view $ARGUMENTS --json title,body,labels,comments
```

2. Understand the problem — is it a data fix (CSV), script fix (search.py), or skill/template fix?

3. Create a branch:
```bash
git checkout -b fix/issue-$ARGUMENTS
```

4. Implement the fix following the sync rules in CLAUDE.md:
   - Data changes → edit `src/ui-ux-pro-max/data/*.csv`
   - Script changes → edit `src/ui-ux-pro-max/scripts/*.py`
   - Template changes → edit `src/ui-ux-pro-max/templates/`
   - If CLI assets need sync → run the cp commands from CLAUDE.md

5. Test the fix:
```bash
python3 src/ui-ux-pro-max/scripts/search.py "test query" --domain style -n 3
```

6. Commit and push:
```bash
git add -A && git commit -m "fix: <description> (closes #$ARGUMENTS)" && git push -u origin HEAD
```

7. Create PR:
```bash
gh pr create --title "fix: <description>" --body "Closes #$ARGUMENTS\n\n## Changes\n\n- " --web
```
