# CLAUDE.md

## Project Overview

**message-dispatcher-test** is an early-stage TypeScript project built on the Bun runtime. The project is structured as an ES module and currently contains a minimal scaffold with a single entry point.

## Tech Stack

- **Runtime**: Bun 1.3.10 (pinned via `mise.toml`)
- **Language**: TypeScript (strict mode)
- **Node version**: 25.7.0 (pinned via `mise.toml`)
- **Module system**: ES modules (`"type": "module"`)
- **Dependencies**: `chat` (4.15.0)

## Project Structure

```
src/
  index.ts          # Main entry point
package.json        # Project manifest (Bun)
tsconfig.json       # TypeScript configuration
mise.toml           # Tool version pinning (Bun, Node)
bun.lockb           # Bun lock file (binary)
```

## Development

### Setup

```sh
bun install
```

### Run

```sh
bun run src/index.ts
```

### Type Checking

```sh
bun x tsc --noEmit
```

No test framework, linter, or CI/CD pipeline is configured yet.

## Code Conventions

- **Strict TypeScript**: `strict: true` in tsconfig — all code must pass strict type checking.
- **ESNext target**: Use modern JS/TS syntax freely (top-level await, etc.).
- **Bundler module resolution**: Imports use bundler-style resolution (`allowImportingTsExtensions` is enabled).
- **No emit**: TypeScript is only used for type checking; Bun handles execution directly.
- **ES modules only**: Use `import`/`export`, not `require`/`module.exports`.

## Git Workflow

- **Default branch**: `main` (remote) / `master` (local)
- Keep commits focused and descriptive.
- Do not commit `.env` files, `node_modules/`, or build artifacts (see `.gitignore`).
