# Buildkite Asdf Plugin

[![Build status](https://badge.buildkite.com/e3e424ff25712d5d1f1566ed06aac73af688f695ada6f8472f.svg)](https://buildkite.com/riskalyze/plugins-buildkite-asdf-plugin)

Use asdf .tool-versions to manage your pipeline's tools

## Example

Add the following to your `pipeline.yml`:

```yaml
steps:
  - command: yarn && yarn test
    plugins:
      - ssh://git@github.com/riskalyze/buildkite-asdf-plugin.git#v1: ~
```

`asdf` will look for a `.tool-versions` in your repo's root and install the plugins and tool versions listed there.

## Configuration

### `path` (Optional, string)

Allows specifying the project path. Useful for repos that do not conform to the standard folder structure.

Defaults to the repository root.

## Contributing

1. Fork the repo
2. Make the changes
3. Commit and push your changes
4. Send a pull request
