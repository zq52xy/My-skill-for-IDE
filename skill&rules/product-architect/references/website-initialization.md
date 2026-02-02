# Website Initialization Protocol (Vite + React + Tailwind v4)

## 0. Check Node.js Environment

First, check if Node.js is installed:
```bash
node -v
```

**If version is shown (e.g., v20.x.x)**: Skip to Step 1.

**If prompt says "command not found"**: Install as follows:

### macOS Installation (Recommended: nvm)
```bash
# Install nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

# Install Node LTS version after restarting terminal
nvm install --lts
nvm use --lts

# Verify installation
node -v && npm -v
```

### Windows Installation
1. Visit https://nodejs.org
2. Download LTS version (Recommended)
3. Run installer, click Next through steps
4. Restart terminal, run `node -v` to verify

### Or using Homebrew (macOS)
```bash
brew install node
```

---

## 1. Create Project & Install Dependencies
```bash
npm create vite@latest . -- --template react && npm install
```

## 2. Install TailwindCSS v4 (Vite Plugin)
```bash
npm install tailwindcss @tailwindcss/vite
```

## 3. Configure `vite.config.js`
```javascript
import tailwindcss from '@tailwindcss/vite'
import react from '@vitejs/plugin-react'
import { defineConfig } from 'vite'

export default defineConfig({
  plugins: [react(), tailwindcss()],
})
```

## 4. Configure `src/index.css`
Keep only one line:
```css
@import "tailwindcss";
```
(Tailwind v4 deprecates `@tailwind base/components/utilities` syntax)

## 5. Add `jsconfig.json` Path Aliases (Optional)
Ensure correct path mapping for imports (e.g., `@/*` to `src/*`).

## 6. Install UI Enhancements
```bash
npm install framer-motion lucide-react clsx tailwind-variants react-icons
```

## 7. Icon & Animation Conventions
- **framer-motion**: Slide-in/Transition animations
- **lucide-react**: System icons
- **react-icons/si**: Social media icons (Si prefix)

**Post-Action**: Immediately build L1/L2/L3 documentation to implement fractal initialization.
**Status**: Await next instruction.
