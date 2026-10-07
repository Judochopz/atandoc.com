# Deployment Guidelines

## One-Line Deployment Command

To build the Hugo site and deploy to Firebase in one command:

```bash
hugo && firebase deploy
```

## What This Does

1. **`hugo`** - Builds the static site from your Hugo source files into the `public/` directory
2. **`firebase deploy`** - Deploys the contents of the `public/` directory to Firebase Hosting

## Prerequisites

- Hugo CLI installed (`hugo version` should work)
- Firebase CLI installed and authenticated (`firebase --version` should work)
- Firebase project configured (`.firebaserc` exists with project ID)

## Current Configuration

- **Hugo config**: `config.yml` with PaperMod theme
- **Firebase project**: `personal-website-398402`
- **Public directory**: `public/` (Hugo builds here, Firebase serves from here)

## Manual Steps (if needed)

If the one-liner fails, run these separately:

```bash
# Build the Hugo site
hugo

# Deploy to Firebase
firebase deploy
```