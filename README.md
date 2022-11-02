# Buildkite Asdf Plugin

Use [asdf](https://asdf-vm.com/) .tool-versions files to manage your pipeline's tools.

## Example

Add the following to your `pipeline.yml`:

```yaml
steps:
  - command: yarn && yarn test
    plugins:
      - byerobot/asdf#v1.2.2: ~
```

`asdf` will look for a `.tool-versions` in your repo's root and install the plugins and tool versions listed there.

## Configuration

### `path` (Optional, string)

Allows specifying the project path. Useful for repos that do not conform to the standard folder structure.

Defaults to the repository root.

### `tool` (Optional, string)

Allows a specific tool to be specified for installation by asdf.

This can be useful if multiple tools are specified in the repository but you only need one for this particular task.

```yaml
steps:
  - command: terraform init && terraform plan
    plugins:
      - byerobot/asdf#v1.2.2:
          tool: terraform
```

## Contributing

1. Fork the repo
2. Make the changes
3. Commit and push your changes
4. Send a pull request
