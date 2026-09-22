# Cursor working rules

Reusable Cursor rules about **how to think and how to answer**.

These rules are not tied to one repo or one codebase. Copy them into another project so a new agent follows the same working style.

## What is in here

| File | Meaning |
| --- | --- |
| `how-to-answer.mdc` | Answer the question that was asked. Do deep work, then give a short high-level answer. Simple English. |
| `answers-from-evidence.mdc` | Base claims on real code or data. Mark anything inferred. Say when you are unsure. |
| `one-topic-at-a-time.mdc` | List all open issues. Work only the current one. Remind the user of the rest. |
| `register-solutions.mdc` | Write down a proposed fix. Do not implement until the user says start. |
| `delete-adhoc-scripts.mdc` | Delete one-off scripts after the job. |
| `do-not-commit-unless-asked.mdc` | Do not commit or push unless the user asks. |
| `assumption-loop.mdc` | Do not stop at an untested assumption. Gather evidence for and against it. Loop until the evidence supports the answer. Then propose fixes; do not implement unless asked. |

## What is not in here

Repo-specific limits (memory cap, proxy, experiment setup, paper task list) stay in that repo. They do not transfer.

## How to use in another repo

```bash
git clone git@github.com:fancui-cuhk/cursor-working-rules.git
mkdir -p /path/to/other-repo/.cursor
cp -r cursor-working-rules/.cursor/rules /path/to/other-repo/.cursor/
```

Cursor will pick up `.cursor/rules/*.mdc` in that repo.
