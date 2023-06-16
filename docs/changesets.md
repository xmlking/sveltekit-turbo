# changesets

## Install

```shell
pnpm add -Dw @changesets/cli
# Then changesets' init command:
pnpm changeset init
```

Other Commands

```shell
# Add a new changeset
pnpm changeset

# Create new versions of packages
pnpm changeset version

# Publish all changed packages to npm
pnpm changeset publish -r
```

Our recommendation is to add a publish-packages script into your root `package.json`:

```json
{
  "scripts": {
    // Include build, lint, test - all the things you need to run
    // before publishing
    "publish-packages": "turbo run build lint test && changeset version && changeset publish"
  }
}
```

> We recommend `publish-packages` so that it doesn't conflict with npm's built-in publish script.

## Reference

- [pnpm changesets](https://pnpm.io/using-changesets)
