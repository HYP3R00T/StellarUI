# StellarUI

A UI component library for Astro with beautiful, accessible components.

## Project Structure

This is a pnpm monorepo with the following structure:

```
StellarUI/
├── packages/
│   └── stellarui/          # Main component library package
│       ├── components/     # .astro components
│       ├── index.ts        # Main export file
│       └── package.json
├── apps/
│   └── docs/              # Documentation and demo site
└── package.json           # Root workspace configuration
```

## Getting Started

### Prerequisites

- Node.js 18+
- pnpm 9+

### Installation

```bash
# Install dependencies
pnpm install

# Start the development server
pnpm dev
```

The docs site will be available at `http://localhost:4321`.

## Development

### Available Scripts

- `pnpm dev` - Start the docs development server
- `pnpm build` - Build all packages
- `pnpm build:lib` - Build only the component library
- `pnpm build:docs` - Build only the docs site
- `pnpm preview` - Preview the built docs site
- `pnpm format` - Format code with Prettier
- `pnpm format:check` - Check code formatting
- `pnpm typecheck` - Run TypeScript type checking

### Adding New Components

1. Create a new `.astro` file in `packages/stellarui/components/`
2. Export it from `packages/stellarui/index.ts`
3. Add examples in `apps/docs/src/pages/index.astro`

Example component structure:

```astro
---
export interface Props {
  // Component props
}

const { prop1, prop2 } = Astro.props;
---

<div>
  <!-- Component markup -->
  <slot />
</div>
```

## Publishing

To publish the `stellarui` package to npm:

```bash
cd packages/stellarui
pnpm publish
```

## License

MIT
