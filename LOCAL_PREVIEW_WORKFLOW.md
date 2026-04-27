# Local Preview Workflow

This file records the branch-preview workflow for this website so it can be reused later or reproduced on another machine.

## Purpose

This repo is a Hugo + Hugo Blox site.

- `main` is the production branch used by GitHub Pages.
- feature branches are where changes should be made and reviewed first
- local preview is the primary way to inspect branch changes before merging to `main`

At the time of writing, the active working branch is:

```bash
codex-content-refresh
```

## What is required

This repo needs all of the following available in Terminal:

- `node`
- `corepack`
- `pnpm` via `corepack`
- `hugo`
- `go`

Why `go` is required:

- this repo uses Hugo Modules from `config/_default/module.yaml`
- Hugo needs Go in order to download and load those modules

## One-time setup on a new machine

### 1. Install Homebrew if needed

Check whether Homebrew is installed:

```bash
brew --version
```

If it is not installed, install it from:

- [https://brew.sh](https://brew.sh)

### 2. Install Node.js

Check:

```bash
node -v
npm -v
corepack --version
```

If missing, install Node:

```bash
brew install node
```

### 3. Activate pnpm through Corepack

This repo expects `pnpm@10.14.0`.

Run:

```bash
corepack prepare pnpm@10.14.0 --activate
corepack pnpm --version
```

Note:

- `corepack enable` may fail with a permission error when trying to write to `/usr/local/bin`
- if that happens, it is okay to use `corepack pnpm ...` directly instead of plain `pnpm`

### 4. Install Hugo

Check:

```bash
hugo version
```

If missing:

```bash
brew install hugo
```

### 5. Install Go

Check:

```bash
go version
```

If missing:

```bash
brew install go
```

If Go was just installed and Terminal still says `go: command not found`, close Terminal, open a new one, and check again.

## First-time repo setup

From Terminal:

```bash
cd "/Users/ernestocriadohidalgo/Library/CloudStorage/Dropbox/Git/ernestocriado.github.io"
corepack pnpm install
```

This may generate or update a few local/build files such as:

- `node_modules/`
- `public/`
- `resources/`
- `go.sum`
- `pnpm-lock.yaml`

Before committing, always check what changed:

```bash
git status --short --branch
```

## Start the local preview server

From the repo root:

```bash
corepack pnpm run dev
```

Then open:

- [http://localhost:1313](http://localhost:1313)

Notes:

- keep the Terminal window open while previewing
- Hugo usually reloads automatically after file saves
- if the browser looks stale, refresh once manually
- stop the server with `Ctrl + C`

## Normal branch workflow

### Preview an existing branch

```bash
cd "/Users/ernestocriadohidalgo/Library/CloudStorage/Dropbox/Git/ernestocriado.github.io"
git fetch origin
git switch branch-name
corepack pnpm run dev
```

Replace `branch-name` with the branch you want to inspect.

### Create a fresh branch from the latest `main`

```bash
cd "/Users/ernestocriadohidalgo/Library/CloudStorage/Dropbox/Git/ernestocriado.github.io"
git fetch origin
git switch main
git merge --ff-only origin/main
git switch -c new-branch-name
corepack pnpm run dev
```

### Resume work on a branch another day

```bash
cd "/Users/ernestocriadohidalgo/Library/CloudStorage/Dropbox/Git/ernestocriado.github.io"
git status --short --branch
git branch --show-current
git fetch origin
corepack pnpm run dev
```

If you want to continue on a specific branch:

```bash
git switch branch-name
corepack pnpm run dev
```

## If changes were made directly on GitHub

If a file was edited in the GitHub web UI, sync local state before continuing.

### Update `main`

```bash
git fetch origin
git switch main
git merge --ff-only origin/main
```

### Bring those updates into your working branch

```bash
git switch your-branch-name
git merge --ff-only origin/main
```

If `git merge --ff-only origin/main` fails, stop and inspect the branch state before doing anything more invasive.

## Useful review commands

### See current branch and changed files

```bash
git status --short --branch
```

### See all branches

```bash
git branch -vv
```

### Compare current branch with `main`

```bash
git diff main...HEAD
```

### See which files differ from `main`

```bash
git diff --name-only main...HEAD
```

### Inspect recent history

```bash
git log --graph --oneline --decorate --all -n 20
```

## Deploy/preview notes

- GitHub Pages in this repo deploys from `main`, not from feature branches
- local preview is the main way to inspect branch work before merge
- Netlify is configured in `netlify.toml` for branch/deploy previews if needed

## Troubleshooting

### `pnpm: command not found`

Use:

```bash
corepack prepare pnpm@10.14.0 --activate
corepack pnpm --version
```

Then run all pnpm commands as:

```bash
corepack pnpm install
corepack pnpm run dev
```

### `hugo: command not found`

Install Hugo:

```bash
brew install hugo
hugo version
```

### `failed to load modules: binary with name "go" not found in PATH`

Install Go:

```bash
brew install go
go version
```

### Browser tab icon or CSS looks stale

Do a hard refresh:

- `Cmd + Shift + R`

### Preview server is already running or locked

Stop the existing server with:

- `Ctrl + C`

If needed, start a fresh Terminal window and run the preview command again.

## Recommended session checklist

At the start of a session:

```bash
cd "/Users/ernestocriadohidalgo/Library/CloudStorage/Dropbox/Git/ernestocriado.github.io"
git status --short --branch
git fetch origin
git switch your-branch-name
corepack pnpm run dev
```

At the end of a session:

```bash
git status --short --branch
```

Then decide whether to:

- keep working later without committing
- commit to the branch
- push the branch
- merge to `main` only after review
