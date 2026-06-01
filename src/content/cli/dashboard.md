# Dashboard

The `fenn dashboard` command launch the Fenn log-browser web UI.

## Usage

```bash
fenn dashboard
```
### Arguments

- `[--log-dir]` (optional): Extra directories to scan for .fn files
- `[--port]` (optional): Port to bind (default: 5000).
- `[--debug]` (optional): Run Flask in debug mode.

## Examples

### Basic Usage

Launch the Fenn log-browser web UI with default port:

```bash
fenn dashboard
```

### Specify extra log directory

Specify extra directories to scan for .fn files

```bash
fenn dashboard --log-dir log-dir/
```

### Specify custom port

Specify custom port to run fenn app on:

```bash
fenn dashboard --port 4000
```

### Run fenn app in debug mode

 Run Fenn in debug mode:

```bash
fenn dashboard --debug
```