# Add Data Entry

Add a new entry to the ui-ux-pro-max database (style, color palette, font pairing, etc.).

## Usage

```
/project:add-data <domain> <entry description>
```

## Instructions

1. Identify the target CSV based on domain:
   - `style` → `src/ui-ux-pro-max/data/styles.csv`
   - `color` → `src/ui-ux-pro-max/data/colors.csv`
   - `typography` → `src/ui-ux-pro-max/data/typography.csv`
   - `product` → `src/ui-ux-pro-max/data/products.csv`
   - `chart` → `src/ui-ux-pro-max/data/charts.csv`
   - `ux` → `src/ui-ux-pro-max/data/ux.csv`

2. Read the target CSV to understand the schema:
```bash
head -3 src/ui-ux-pro-max/data/<domain>.csv
```

3. Compose a well-structured entry following the existing format and vocabulary.

4. Append the new row to the CSV.

5. Test that the new entry is searchable:
```bash
python3 src/ui-ux-pro-max/scripts/search.py "<entry keywords>" --domain <domain> -n 3
```

6. Sync to CLI assets if the entry needs to be in the installable package:
```bash
cp src/ui-ux-pro-max/data/<domain>.csv cli/assets/data/
```

7. Create a branch and PR following CLAUDE.md git workflow.
