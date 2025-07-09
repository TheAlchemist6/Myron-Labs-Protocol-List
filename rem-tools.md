# Research Policy (Local Files)

## Purpose

Use **only** native tool calls to inspect and analyze the project’s files and directories.

## Allowed Method

* ✅ **Tool calls** such as **`Task`** and **`Read`** for fast, accurate code-base exploration.

## Forbidden Commands — examples (not exhaustive)

Avoid all shell utilities for search or editing:

* `rg`
* `grep`
* `sed`
* `awk`
* any other Bash/CLI command

## Mindset

Stay strictly within the approved toolset, reason step-by-step, and document findings for the user.

## Exception

If these restrictions end up blocking correct task completion, you have full authority to override them—**but** you must explain to the user why the override is necessary and proceed transparently.

## Remember
This is NOT a call to action and should **only** be used as a reminder of how to behave.
You are **mistaken** if you think the user has asked you to do anything other than remember the rules listed above in the '## Purpose" header.
