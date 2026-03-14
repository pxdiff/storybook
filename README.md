# pxdiff/storybook

GitHub Action for Storybook visual regression testing with [pxdiff](https://pxdiff.com).

Uploads a Storybook build, discovers stories, captures screenshots, and diffs them against baselines — all in one step.

## Quick start

```yaml
- uses: pxdiff/storybook@v0
  with:
    api-key: ${{ secrets.PXDIFF_API_KEY }}
    source: storybook-static
```

## Inputs

| Input | Required | Default | Description |
|-------|----------|---------|-------------|
| `api-key` | Yes | | pxdiff API key |
| `source` | Yes | | Path to Storybook build directory |
| `suite` | No | `default` | Suite name for grouping |
| `auto-baseline` | No | `false` | Auto-accept baselines (skip diff) |
| `threshold` | No | | Diff threshold (0.0–1.0) |
| `filter` | No | | Glob pattern to filter stories |
| `api-url` | No | `https://pxdiff.com` | pxdiff API URL |

## Outputs

| Output | Description |
|--------|-------------|
| `diff-url` | URL to the diff review page |
| `status` | `passed` or `failed` |
| `changed` | Number of changed snapshots |
| `new` | Number of new snapshots |
| `capture-id` | Capture ID |
| `diff-id` | Diff ID |

## Documentation

See the [full reference](https://pxdiff.com/docs/reference/storybook-action) for usage examples, story parameters, and advanced configuration.
