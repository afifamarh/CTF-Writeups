# Basic Linux Medium Challenge

## Challenge Information

| Field | Value |
|---------|---------|
| CTF | LICTF 2022 |
| Category | Linux |
| Difficulty | Medium |
| Points | 40 |

## Objective

Navigate to the specified directory and execute the provided file to obtain the flag.

### Challenge Description

> Run the file in `/root/CTF/Basic_Linux/Medium`. What is printed?

---

## Reconnaissance

The first step was navigating to the target directory:

```bash
cd /root/CTF/Basic_Linux/Medium
```

After arriving at the location, I listed the directory contents:

```bash
ls
```

The command revealed a file named:

```text
output
```

---

## Obstacle Encountered

Following the challenge instructions, I attempted to execute the file:

```bash
./output
```

However, the system returned:

```text
Permission denied
```

This indicated that the file lacked execute permissions.

---

## Solution

To make the file executable, I used:

```bash
chmod +x output
```

After updating the permissions, I executed the file again:

```bash
./output
```

This time the program executed successfully and displayed the flag.

---

## Flag

```text
Now you see me!
```

---

## Reflection

This challenge was straightforward but highlighted the importance of checking file permissions before attempting execution.

A better approach would have been:

```bash
ls -l
```

instead of:

```bash
ls
```

because it immediately displays file permissions and would have helped identify the issue faster.

### Key Learning Points

- Using `chmod` to modify file permissions.
- Understanding Linux execute permissions.
- Using `ls -l` to inspect file attributes.
- Troubleshooting "Permission denied" errors.
