# Sync CLI Assets

Sync source data and scripts to CLI bundle before publishing.

## Usage

```
/project:sync-cli
```

## Instructions

Run the sync per CLAUDE.md rules:

```bash
cp -r src/ui-ux-pro-max/data/* cli/assets/data/
cp -r src/ui-ux-pro-max/scripts/* cli/assets/scripts/
cp -r src/ui-ux-pro-max/templates/* cli/assets/templates/
```

Then verify the CLI still works:

```bash
node cli/src/commands/init.ts --help 2>/dev/null || echo "TypeScript — run via npx"
```

Check sizes to confirm sync:
```bash
du -sh src/ui-ux-pro-max/data/ cli/assets/data/
du -sh src/ui-ux-pro-max/scripts/ cli/assets/scripts/
```

Report any size discrepancies. If mismatch found, re-run sync.
