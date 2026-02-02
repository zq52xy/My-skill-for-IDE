# Shadcn UI Design System Integration

## 1. Initialize shadcn/ui
```bash
npx shadcn@latest init
```

**Configuration Options:**
- **Style**: Default
- **Base color**: Select as needed
- **CSS variables**: Yes
- **Path Aliases**: Automatically read from `jsconfig.json` / `tsconfig.json`

## 2. Install Theme
```bash
npx shadcn@latest add https://tweakcn.com/r/themes/amethyst-haze.json
```

## 3. Batch Component Installation (Avoid Timeouts)

⚠️ **CRITICAL**: Installing too many components at once causes timeouts. YOU MUST INSTALL IN BATCHES.

**Batch 1: Core Interaction**
```bash
npx shadcn@latest add button input label card dialog sheet
```

**Batch 2: Form Components**
```bash
npx shadcn@latest add form select checkbox radio-group switch textarea
```

**Batch 3: Feedback**
```bash
npx shadcn@latest add alert sonner badge skeleton progress
```

**Batch 4: Navigation**
```bash
npx shadcn@latest add tabs accordion dropdown-menu navigation-menu
```

**Batch 5: Display**
```bash
npx shadcn@latest add avatar table popover tooltip hover-card
```

**Batch 6: Utilities**
```bash
npx shadcn@latest add scroll-area separator command collapsible
```

**On Demand** (Install only if used):
```bash
npx shadcn@latest add slider toggle toggle-group menubar context-menu aspect-ratio
```

## 4. Design System Convention (`src/index.css`)
Ensure this is the only import:
```css
@import "tailwindcss";
```

## 5. Recommended Directory Structure
```
src/
├── components/
│   └── ui/          # shadcn components (auto-generated)
├── lib/
│   └── utils.ts     # cn() function (auto-generated)
├── index.css
└── App.jsx
```

## 6. Troubleshooting

| Issue | Solution |
|-------|----------|
| Installation Timeout | Batch installation (max 6 components per batch) |
| npm warn Unknown user config | Ignore, does not affect installation |
| Path Alias Error | Check `@/*` config in `jsconfig.json` |
| Styles Not Applied | Confirm `index.css` imports `tailwindcss` |

---

## Execution Directives
1. Use Design System components to build **Header**, **Hero**, **Footer**.
2. Include a `react-router` driven "DesignSystem" showcase page entry in the Header.
3. **Mandate**: In L1 & L2 documentation, emphasize that **ALL design must originate from the Design System's colors and components**.

**Status**: Await next instruction.
