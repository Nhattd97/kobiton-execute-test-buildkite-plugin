# Kobiton Execute Test Buildkite Plugin

A Buildkite Plugin to (synchronously) execute an automated test script on Kobiton service.

## Example

Add the following to your `pipeline.yml`:

```yml
steps:
  - command: ls
    plugins:
      - Nhattd97/kobiton-execute-test#v1.0.0:
          pattern: '*.md'
```

## Configuration

### `pattern` (Required, string)

The file name pattern, for example `*.ts`. Supports any pattern supported by [find -name](http://man7.org/linux/man-pages/man1/find.1.html).

## Developing

To run the tests:

```shell
docker-compose run --rm tests
```

To validate the `plugin.yml`:
```shell
docker-compose run --rm lint
```

## Contributing

1. Fork the repo
2. Make the changes
3. Run the tests
4. Commit and push your changes
5. Send a pull request
