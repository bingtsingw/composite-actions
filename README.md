# composite-actions

## `setup-node`

Sets up Bun, Node.js, and pnpm, then installs dependencies by default.

```yaml
- uses: bingtsingw/composite-actions/setup-node@main
  with:
    pnpm-version: '11'
```

pnpm caching is enabled automatically when `cache-dependency-path` (default:
`**/pnpm-lock.yaml`) matches a lockfile. If there is no lockfile, Node.js is
still set up and the cache is skipped; this is useful for repositories that
only test the action itself. To disable installation as well, set
`run-install: 'false'`.
