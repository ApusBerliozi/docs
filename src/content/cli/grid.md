# Grid

The `fenn grid` command allows you to run fenn app with different seeds, epoch counts, or learning rates. In order to do it, you need to specify grid/train param in yaml template, like this:
```yaml
grid:
    train:
        seed: [42,41,40]
        batch: [16,15]
        epochs: 30
        lr: 1e-3
```
## Usage

```bash
fenn grid [path]
```

### Arguments

- `[path]` (optional): The path to entrypoint file. The file can have a custom name (e.g. `my_dir/custom_main.py`). Defaults are current directory (`.`) and `main.py` file.

## Examples

### Basic Usage

Execute fenn app with cartesian product, specified in grid:

```bash
fenn grid
```

### Specify path to entrypoint script

Specify path to entrypoint script (default `main.py`):

```bash
fenn grid empty /my_dir/custom_main.py
```
