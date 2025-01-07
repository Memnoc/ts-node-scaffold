## Scaffold for node packages written in TypeScript

Easy scaffold to start developing node packages to publish in the registry.

### Dependencies

**Create project**

mkdir gig
cd gig
pnpm init

**Add TypeScript and core dependencies**

pnpm add -D typescript @types/node tsup
pnpm add clipanion enquirer better-cli-alerts

**Dev tools and best practices**

pnpm add -D prettier eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin
pnpm add -D vitest
pnpm add -D @changesets/cli # For version management

**Create basic structure**

mkdir src
mkdir src/commands
mkdir src/utils
mkdir src/types
mkdir tests

**Initialize TypeScript**

pnpm tsc --init
OR
npx tsc --init

**Initialize ESLint**

pnpm eslint --init
OR
npx eslint --init

**Initialize Prettier**

echo {} > .prettierrc.json

### Sample structure// Project structure

src/
├── commands/
│ ├── generate.ts // Main command to generate gitignore
│ └── list.ts // List available templates
├── utils/
│ ├── templates.ts // Store/load gitignore templates
│ └── writer.ts // Write gitignore file
├── types.ts // Shared types
└── cli.ts // CLI entry point
