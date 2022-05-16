# Buildkite Asdf Plugin

[![Build status](https://badge.buildkite.com/e3e424ff25712d5d1f1566ed06aac73af688f695ada6f8472f.svg)](https://buildkite.com/riskalyze/plugins-buildkite-asdf-plugin)

Use asdf .tool-versions to manage your pipeline's tools

## Example

Add the following to your `pipeline.yml`:

```yaml
steps:
  - plugins:
      - ssh://git@github.com/riskalyze/buildkite-asdf-plugin.git#v1: ~
```

## Configuration

This plugin doesn't take any configuration parameters currently.

## Contributing

1. Fork the repo
2. Make the changes
3. Commit and push your changes
4. Send a pull request
