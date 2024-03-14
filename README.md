# `@Schleifner/upload-artifact`

This aciton is forked from actions/upload-artifact

we changed it's behavior to only run in post step
and added a new input: second-path

## Usage

### Inputs

```yaml
- uses: Schleifner/upload-artifact@v1
  with:
    name: coredump
    path: /var/lib/apport/coredump
    # if no files found in path ,second-path will be ignored, otherwise combine path and second-path to search
    second-path: ${{ inputs.build_dir }}
```

please refer source [README](https://github.com/actions/upload-artifact) in actions/upload-artifact
