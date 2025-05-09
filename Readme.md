# CLI Starter Template

A modern template for building command-line interfaces with TypeScript.

## Features

- **Strong TypeScript Support**: 100% type-safe CLI construction
- **Modern Development Experience**: Fast builds and clean code
- **Easy to Use**: Simple API to create complex command-line tools

## Tech Stack

- [**stricli**](https://github.com/bloomberg/stricli): Type-safe CLI framework
- [**Biome**](https://biomejs.dev/): Fast linting and formatting
- [**Bun**](https://bun.sh/): Efficient package management and runtime (node works too)
- [**tsup**](https://github.com/egoist/tsup): TypeScript bundler
- [**pkg-pr-new**](https://github.com/stackblitz-labs/pkg.pr.new): publishes a preview release on each commit (needs [minimal setup](https://github.com/stackblitz-labs/pkg.pr.new?tab=readme-ov-file#setup))
- [**release-please**](https://github.com/googleapis/release-please): automates versioning and changelog generation
- [**lefthook**](https://github.com/evilmartians/lefthook): formatting and linting pre-commit hooks

## Getting Started

### Prerequisites

- Bun installed on your system

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/cli-starter.git
cd cli-starter

# Install dependencies
bun install
```

- [**pkg-pr-new**](https://github.com/stackblitz-labs/pkg.pr.new) (creates preview builds):
  - [Install GitHub App](https://github.com/stackblitz-labs/pkg.pr.new?tab=readme-ov-file#setup) 
- [**release-please**](https://github.com/googleapis/release-please) (automates versioning and changelogs):
  - create personal access token with write access to PRs and Code [Guide](https://github.com/googleapis/release-please-action?tab=readme-ov-file#basic-configuration)
  - Save token as `RELEASE_PLEASE_GH_TOKEN` secret
  - It Creates a release PR on every push to `main`. Merge to release.


### Development

```bash
# Run development build with watching
bun run build:dev

# Lint code
bun run lint

# Type check
bun run typecheck
```

### Building for Production

```bash
# Build the project
bun run build
```

## Usage

After building, you can run your CLI with:

```bash
# bun
bun ./src/cli/bin/cli.ts

# Or with node (needs to be built)
npm run build:dev
node ./dist/cli/bin/cli.ts
```
