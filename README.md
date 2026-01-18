# aaa-actions

## Purpose / Scope
Reusable GitHub Actions workflows for the ai-asset-architecture (aaa) org. This repo provides organization-wide CI building blocks that other repos can call via `workflow_call`.

## Ownership / CODEOWNERS
Owned by the platform/infra maintainers. See `CODEOWNERS` (to be added).

## Versioning / Release
Workflows are versioned by git tags. Use `vX.Y.Z` tags in consuming repos. Do not pin to `main` for production usage.

## How to Consume / Use
Reference workflows by tag from `.github/workflows/*` in a consuming repo.

## Contribution / Promotion Rules
Changes must be backwards compatible or released as a new major tag. Validate changes against at least one downstream repo before tagging.

## Available Workflows
- `lint.yml` (TBD)
- `test.yml` (TBD)
- `eval.yml` (TBD)
- `release.yml` (TBD)

## Usage (with tag)
```yaml
jobs:
  lint:
    uses: ai-asset-architecture/aaa-actions/.github/workflows/lint.yml@v0.1.0
```

## Release Gate & Tag Policy
- Tags use SemVer: `vMAJOR.MINOR.PATCH`.
- `main` is for development only; consumers should pin tags.
- Breaking changes require a major bump and a migration note in the release.
