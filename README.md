# Linux `uniq` Challenge

## Investigate Repeated Failed SSH Login Sources

**Difficulty:** Beginner
**Target audience:** Graduate IT Operations consultants

## Scenario

The Security Operations team has exported the source IP address from each failed SSH login event.

Each line in the input file represents one failed SSH login attempt. The same IP address may therefore appear multiple times.

The input file is intentionally unsorted.

## Input File

The data is stored at:

```text
data/failed_ssh_source_ips.txt
```

Do not edit or overwrite this file.

## Environment

Use a Bash-compatible terminal:

- Linux terminal on Linux
- Git Bash or WSL in VS Code on Windows

Run all commands from the root of the downloaded challenge folder.

Native PowerShell commands are outside the scope of this challenge.

---
## Getting Started

1. Select **Code → Download ZIP** on this GitHub page.
2. Extract the downloaded ZIP file.
3. Open the extracted folder in Visual Studio Code.
4. Open a Bash-compatible terminal:
   - Git Bash or WSL on Windows
   - A standard terminal on Linux
5. Run all commands from the root of the challenge folder.
---

## Task 1 — Investigate Repeated Sources

Write **one command pipeline** that:

1. Uses the `uniq` command.
2. Shows only IP addresses that appear more than once.
3. Shows how many times each repeated IP address appears.
4. Displays the highest count first.
5. Does not modify the original input file.

### Expected Output

```text
4 203.0.113.17
3 198.51.100.42
2 192.0.2.55
```

Additional spaces before the counts are acceptable.

---

## Task 2 — Create a Deduplicated File

Create a new file in the challenge folder called:

```text
unique_failed_ssh_sources.txt
```

The new file must:

- Contain every source IP address exactly once
- Be sorted in ascending order
- Leave the original input file unchanged

### Expected File Contents

```text
10.20.30.5
192.0.2.55
192.0.2.99
198.51.100.42
198.51.100.8
203.0.113.17
```

---

## Submission

Provide:

1. The command pipeline used for Task 1
2. The command used for Task 2
3. The generated `unique_failed_ssh_sources.txt` file
4. A brief explanation of why `sort` is needed before `uniq`

## Constraints

- You must use `uniq`.
- Do not manually edit the input data.
- Do not overwrite `data/failed_ssh_source_ips.txt`.
- Your solution should work in a Bash-compatible terminal on Windows or Linux.