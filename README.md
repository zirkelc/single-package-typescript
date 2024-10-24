# TypeScript Single Package Project Template

This template provides an opinionated setup for a single package TypeScript project.

## 🚀 Features

- 📦 [PNPM](https://pnpm.io/) for efficient package management
- 🧹 [Biome](https://biomejs.dev/) for linting and formatting
- 🧪 [Vitest](https://vitest.dev/) for fast, modern testing
- 🏗️ [tsup](https://tsup.egoist.dev/) for TypeScript building and bundling
- 🏃‍♂️ [tsx](https://tsx.is/) for running TypeScript files
- 🐶 [Husky](https://github.com/typicode/husky) for Git hooks
- 🔄 [GitHub Actions](.github/workflows/ci.yml) for continuous integration
- 🐞 [VSCode](.vscode/) debug configuration and editor settings
- 🔧 [@total-typescript/tsconfig](https://github.com/total-typescript/tsconfig) for TypeScript configuration

## 📋 Details

### Package

The [`package.json`](package.json) is configured as ESM (`"type": "module"`), but supports dual publishing with both ESM and CJS module formats.

### Biome

[`biome.jsonc`](biome.jsonc) contains the default [Biome configuration](https://biomejs.dev/reference/configuration/) with minimal formatting adjustments. It uses the formatter settings from the [`.editorconfig`](.editorconfig) file.

### Vitest

An empty Vitest config is provided in [`vitest.config.ts`](vitest.config.ts).

### Build and Run

- `tsup` builds `./src/index.ts`, outputting both ESM and CJS formats to the `dist` folder.
- `tsx` compiles and runs TypeScript files on-the-fly.

### Git Hooks

[Husky](https://github.com/typicode/husky) runs the [.husky/pre-commit](.husky/pre-commit) hook to lint staged files.

### Continuous Integration

[`.github/workflows/ci.yml`](.github/workflows/ci.yml) defines a GitHub Actions workflow to run linting and tests on commits and pull requests.

### VSCode Integration

#### Debugging

[`.vscode/launch.json`](.vscode/launch.json) provides VSCode launch configurations:
- `Debug (tsx)`: Run and debug TypeScript files
- `Test (vitest)`: Debug tests

It uses the [JavaScript Debug Terminal](https://code.visualstudio.com/docs/nodejs/nodejs-debugging) to run and debug.

#### Editor Settings

[`.vscode/settings.json`](.vscode/settings.json) configures Biome as the formatter and enables format-on-save.

### EditorConfig

[`.editorconfig`](.editorconfig) ensures consistent coding styles across different editors and IDEs:

- Uses spaces for indentation (2 spaces)
- Sets UTF-8 charset
- Ensures LF line endings
- Trims trailing whitespace (except in Markdown files)
- Inserts a final newline in files

This configuration complements Biome and helps maintain a consistent code style throughout the project.

## 🚀 Getting Started

1. Create a new repository [using this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
2. Run `pnpm install` to install dependencies
3. Start coding in the `src` directory
4. Run tests with `pnpm test`
5. Build your project with `pnpm build`

Happy coding! 🎉
