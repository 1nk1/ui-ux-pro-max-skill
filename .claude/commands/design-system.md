# Generate Design System

Generate a complete design system for a product using the ui-ux-pro-max skill.

## Usage

```
/project:design-system <product description> [-p "Project Name"] [--persist]
```

## Instructions

Run the design system generator with the provided description:

```bash
python3 src/ui-ux-pro-max/scripts/search.py "$ARGUMENTS" --design-system -p "${PROJECT_NAME:-Project}"
```

If `--persist` is requested by the user, add it to save `design-system/MASTER.md`:

```bash
python3 src/ui-ux-pro-max/scripts/search.py "$ARGUMENTS" --design-system --persist -p "${PROJECT_NAME:-Project}"
```

After running, synthesize the output into:
1. Chosen style + reasoning
2. Color palette (primary, secondary, accent, surface, text tokens)
3. Typography pair (heading + body fonts with scale)
4. Key UX rules to follow for this product type
5. Anti-patterns to avoid

Then ask: "Shall I persist this as design-system/MASTER.md for hierarchical retrieval?"
