# Godot setup action

Moves Godot support files from the root user to the local user. For use with environments where Godot support files are owned by the root user.

## Usage

```yaml
name: my-workflow

on: push

jobs:
  export:
    runs-on: ubuntu-latest
    container: lfdev/godot-headless:latest
    steps:
      - uses: LF/godot-setup-action@v1
```

While the image [lfdev/godot-headless](https://hub.docker.com/r/lfdev/godot-headless) from Docker Hub is used in this example, this action should work in environments where Godot support files are in the expected locations within root user's home folder.
