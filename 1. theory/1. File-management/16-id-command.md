## `id` Command in Linux — Summary

The `id` command in Linux displays user identity information, including:
- UID (User ID)
- GID (Group ID)
- Supplementary groups
- Usernames and group names
- Security context (on SELinux systems)  
It’s mainly used for permission troubleshooting, user verification, and system administration tasks.

### What `id` Shows by Default

Running `id` with no options prints:
- Your UID
- Your primary GID
- All groups you belong to
- SELinux context (if enabled)
Example:
`id`

```bash
id
```

### Useful Options

| Option    | Description |
|-----------|-------------|
| -u        | Print only the user ID (UID). |
| -g        | Print only the primary group ID (GID). |
| -G        | Print all supplementary group IDs. |
| -n        | With -u, -g, or -G, print names instead of numeric IDs. |
| -r        |  Print real IDs instead of effective IDs. |
| --help    | Show usage information and exit. |
| --version | Show version information and exit. |

### Examples

### 1. Show your own identity
`id`


### 2. Show UID of a specific user
`id -u master`

### 3. Show GID of a specific user
`id -g master`

### 4. Show UID + all groups of a user
`id master`

### 5. Show all group IDs only
`id -G master`

### 6. Show names instead of numbers
```bash
id -ng master
id -nu master
id -nG master
```

### 7. Show real IDs instead of effective IDs
```bash
id -r -u master
id -r -g master
id -r -G master
```







