# Run

The `fenn run` command allows you run a Fenn project on the Fenn remote service

## Usage

```bash
fenn run [script] [--api-key] [--profile] [--max-runtime] [--detach] [--no-download] [--include] [--exclude]
```

### Arguments

- `[script]` (optional): Path to the entrypoint script (default: main.py).
- `[--api-key]` (optional): API key (overrides env, credentials file, and .env).
- `[--detach]` (optional): Submit the job and exit without streaming logs.
- `[--exclude]` (optional): Extra shell-glob pattern to exclude from the upload tarball.
- `[--include]` (optional): Extra path (relative to CWD) to include in the upload tarball.
- `[--max-runtime]` (optional): Maximum allowed wall-time in minutes (server enforces; default: 10).
- `[--no-download]` (optional): Do not download artifacts on completion.
- `[--profile]` (optional): Credentials profile name (default: 'default' or $FENN_PROFILE).



## Examples

### Basic Usage

Execute on the Fenn remote service; uploads the project, streams logs, downloads artifacts

```bash
fenn run
```

### Specify path to entrypoint script

Specify path to entrypoint script (default `main.py`):

```bash
fenn run /my_dir/custom_main.py
```

### Specify API key

Specify API key (overrides env, credentials file, and .env):

```bash
fenn run --api-key sk-proj-xK9mP2vL8nQrT5wY1jB6cD4eF7gH0iJ3kMnOpQrStUv
```

### Specify logs policy

Submit the job and exit without streaming logs:

```bash
fenn run --detach
```

### Exclude shell-glob pattern 

Extra shell-glob pattern to exclude from the upload tarball:

```bash
fenn run --exclude file*
```

### Include shell-glob pattern 

Extra path (relative to CWD) to include in the upload tarball.

```bash
fenn run --include file*
```

### Set maximum allowed wall-time in minutes

Maximum allowed wall-time in minutes (server enforces; default: 10).

```bash
fenn run --max-runtime 20
```

### Exclude artifacts

Do not download artifacts on completion

```bash
fenn run --no-download
```

### Set profile

Credentials profile name (default: 'default' or $FENN_PROFILE).

```bash
fenn run --profile test_profile
```