# stellarui

Beautiful, accessible UI components for Astro with a dark-themed design system.

## Installation

### 1. Install Tailwind CSS v4

First, install Tailwind CSS v4 in your Astro project:

```bash
npm install tailwindcss@next @tailwindcss/vite@next
# or
pnpm add tailwindcss@next @tailwindcss/vite@next
# or
yarn add tailwindcss@next @tailwindcss/vite@next
```

### 2. Configure Tailwind in your Astro config

Update your `astro.config.mjs`:

```javascript
import { defineConfig } from 'astro/config';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  vite: {
    plugins: [tailwindcss()]
  }
});
```

### 3. Add the design tokens to your global CSS

Create or update your global CSS file (e.g., `src/styles/global.css`) with the StellarUI design tokens:

```css
@import "tailwindcss";

@layer base {
  :root {
    /* Neutrals */
    --background: hsl(220, 15%, 8%);
    --content: hsl(220, 14%, 11%);
    --elevated: hsl(220, 13%, 16%);
    --border: hsl(220, 12%, 22%);
    --text-default: hsl(220, 13%, 93%);
    --text-subtle: hsl(220, 9%, 70%);
    --text-faint: hsl(220, 8%, 50%);

    /* Accents & Statuses */
    --red: hsl(0, 65%, 62%);
    --orange: hsl(30, 70%, 60%);
    --yellow: hsl(45, 75%, 65%);
    --green: hsl(130, 40%, 55%);
    --teal: hsl(165, 45%, 53%);
    --cyan: hsl(185, 50%, 60%);
    --blue: hsl(210, 70%, 63%);
    --purple: hsl(270, 60%, 65%);
    --pink: hsl(330, 65%, 67%);

    --accent: var(--blue);
    --radius: 0.5rem;

    --astro-code-background: var(--content);
    --astro-code-foreground: var(--text-default);
    --astro-code-token-constant: var(--pink);
    --astro-code-token-string: var(--green);
    --astro-code-token-comment: var(--text-faint);
    --astro-code-token-keyword: var(--pink);
    --astro-code-token-parameter: var(--red);
    --astro-code-token-function: var(--blue);
    --astro-code-token-string-expression: var(--green);
    --astro-code-token-punctuation: var(--red);
    --astro-code-token-link: var(--green);
  }
}

@theme {
  --color-*: initial;
  --color-background: var(--background);
  --color-content: var(--content);
  --color-elevated: var(--elevated);
  --color-border: var(--border);
  --color-text-default: var(--text-default);
  --color-text-subtle: var(--text-subtle);
  --color-text-faint: var(--text-faint);
  --color-red: var(--red);
  --color-orange: var(--orange);
  --color-yellow: var(--yellow);
  --color-green: var(--green);
  --color-cyan: var(--cyan);
  --color-blue: var(--blue);
  --color-purple: var(--purple);
  --color-pink: var(--pink);
  --color-accent: var(--accent);
  --radius-radius: var(--radius);
  --radius-lg: calc(var(--radius) + 3px);
  --radius-sm: calc(var(--radius) - 3px);
}
```

### 4. Install StellarUI

```bash
npm install stellarui
# or
pnpm add stellarui
# or
yarn add stellarui
```

### 5. Import the global CSS in your layout

In your Astro layout or page:

```astro
---
import '../styles/global.css';
---
```

## Usage

Import components in your Astro files:

```astro
---
import { Button } from 'stellarui';
---

<Button variant="primary" size="md">
  Click me
</Button>
```

## Components

### Button

A versatile button component with multiple variants and sizes.

**Props:**
- `variant?: 'primary' | 'secondary' | 'outline'` - Button style variant (default: 'primary')
- `size?: 'sm' | 'md' | 'lg'` - Button size (default: 'md')
- `class?: string` - Additional CSS classes

**Example:**

```astro
<Button variant="primary" size="lg">
  Primary Button
</Button>

<Button variant="outline" size="sm">
  Small Outline
</Button>
```

## Requirements

- Astro ^5.0.0
- Tailwind CSS (for styling)

## License

MIT
