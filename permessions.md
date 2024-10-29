### Permission Format in `chmod`

In Unix/Linux, permissions are usually represented in three groups: **Owner**, **Group**, and **Others**. Each group has three possible permissions:
- **Read (r)**: Value `4`
- **Write (w)**: Value `2`
- **Execute (x)**: Value `1`

Permissions are represented as a three-digit number where each digit is the sum of permissions for each group.

### Common Permission Combinations

| Permission | Command (`chmod`) | Description                                | Symbolic Representation |
|------------|--------------------|--------------------------------------------|--------------------------|
| `777`      | `chmod 777 file`  | Full access to everyone                    | `rwxrwxrwx`              |
| `755`      | `chmod 755 file`  | Owner can read/write/execute, others read/execute | `rwxr-xr-x`      |
| `700`      | `chmod 700 file`  | Only the owner has full access             | `rwx------`              |
| `644`      | `chmod 644 file`  | Owner can read/write, others read-only     | `rw-r--r--`              |
| `600`      | `chmod 600 file`  | Owner can read/write, no permissions for others | `rw-------`        |
| `555`      | `chmod 555 file`  | Read/execute for everyone, no write access | `r-xr-xr-x`              |
| `444`      | `chmod 444 file`  | Read-only for everyone                     | `r--r--r--`              |
| `400`      | `chmod 400 file`  | Owner read-only, no permissions for others | `r--------`              |
| `750`      | `chmod 750 file`  | Owner full access, group read/execute, others no access | `rwxr-x---`  |
| `640`      | `chmod 640 file`  | Owner read/write, group read-only, others no access | `rw-r-----`    |
| `711`      | `chmod 711 file`  | Owner full access, others execute-only     | `rwx--x--x`              |
| `666`      | `chmod 666 file`  | Read/write for everyone, no execute access | `rw-rw-rw-`              |
| `331`      | `chmod 331 file`  | Owner write/execute, group write-only, others execute-only | `-wx-w---x` |
| `222`      | `chmod 222 file`  | Write-only for everyone                    | `-w--w--w-`              |
| `111`      | `chmod 111 file`  | Execute-only for everyone                  | `--x--x--x`              |

### Understanding the Symbolic Representation

Each group of permissions is three characters:
1. **First Group (Owner)**: Represents the owner’s permissions.
2. **Second Group (Group)**: Represents the group’s permissions.
3. **Third Group (Others)**: Represents everyone else's permissions.

For example:
- `755` → `rwxr-xr-x`: The owner has full permissions, while group and others can read and execute but not write.
- `644` → `rw-r--r--`: The owner can read and write, while group and others can only read. 


