# Auth

The `fenn auth` command allows you to manage credentials for the Fenn remote service.
## Usage

```bash
fenn auth [login] [--profile] [--api-key] [status] [--profile] [logout] [--profile]
```

### Arguments
One of subcomand (login, status or logout) is required for `auth` command
- `[login]`: Save an API key for a profile
- `[--api-key]` (optional): API key (if omitted, will prompt or read from stdin)
- `[--profile]` (optional): Profile name (default: 'default')
- `[status]`: Show the currently configured profile and credit balance
- `[--profile]` (optional): Show the currently configured profile and credit balance
- `[logout]`: Save an API key for a profile
- `[--profile]` (optional): Save an API key for a profile

## Examples

### Basic Usage

Execute fenn app with cartesian product, specified in grid:

```bash
fenn auth login
```

### Login
Save an API key for a profile

```bash
fenn auth login
```

### Specify API key

Specify API key:

```bash
fenn auth login --api-key sk-proj-xK9mP2vL8nQrT5wY1jB6cD4eF7gH0iJ3kMnOpQrStUv
```

### Set profile

Credentials profile name (default: 'default' or $FENN_PROFILE).

```bash
fenn run login --profile test_profile
```

### Show status
Show the currently configured profile and credit balance

```bash
fenn auth status
```

### Set profile

Credentials profile name (default: 'default' or $FENN_PROFILE).

```bash
fenn run status --profile test_profile
```

### Logout
Remove a profile from the credentials file

```bash
fenn auth logout
```

### Set profile

Credentials profile name (default: 'default' or $FENN_PROFILE).

```bash
fenn run logout --profile test_profile
```
