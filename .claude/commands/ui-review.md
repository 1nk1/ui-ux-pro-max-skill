# UI/UX Code Review

Review UI code against ui-ux-pro-max quality standards.

## Usage

```
/project:ui-review [file or component name]
```

## Instructions

1. Read the specified file(s) or `git diff` if no file given:
```bash
git diff HEAD -- "*.tsx" "*.jsx" "*.css" "*.ts" | head -300
```

2. Run UX validation search:
```bash
python3 src/ui-ux-pro-max/scripts/search.py "animation accessibility z-index loading touch" --domain ux -n 10
```

3. Review against the Pre-Delivery Checklist from `.claude/skills/ui-ux-pro-max/SKILL.md`:
   - **Visual Quality**: No emoji icons, consistent icon family, semantic color tokens
   - **Interaction**: Touch targets ≥44px, pressed feedback, micro-interaction 150–300ms
   - **Light/Dark Mode**: Contrast ≥4.5:1 for body, ≥3:1 for secondary
   - **Layout**: Safe areas, 8dp spacing rhythm, mobile-first breakpoints
   - **Accessibility**: aria-labels, keyboard nav, focus order, reduced-motion support

4. Report issues grouped by severity: CRITICAL → HIGH → MEDIUM → LOW

5. For each issue: quote the offending code, state the rule violated, provide the fix.
