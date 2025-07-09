# Setup guide

1. Create this file: ~/.claude/commands/tree.md
2. Modify the tree command (also install the tree command with `sudo apt -y install tree`) so it matches and escapes the right things
3. Restart Claude code
4. Call with /tree command

This fast updates Claude code on your entire code base layout.
You can now easily give Claude the ENTIRE birds eye view of your project files fast and have him use this info to optimize and enhance the next tasks you are working on together.



# Project Structure Overview (`tree`)

Quickly visualize the source layout while ignoring generated artifacts.

## Purpose

* See every relevant source file at a glance.
* Exclude `node_modules/`, `dist/`, `.git/` so you focus only on maintained code.

## Command — run from the project root

```bash
tree -P "*.tsx" -P "*.ts" -P "*.css" -P "*.scss" -P "*.toml" -P "*.sql" -P "*.json" -P "*.sh" -P "*.py" -I "node_modules" -I "dist" -I ".git" .
```

## Workflow

1. **Verify location** – `pwd` should point to the project root.
2. **Execute** the command above.
3. **Review** the output; concentrate solely on files that appear.
4. **Map** the structure to all open TODOs and refine your action plan.
5. **Explain** to the user how these findings shape your next steps.
6. **Complete** every pending task with this newfound context.

## Mindset

Reason methodically, step by step, to produce world-class, maintainable code that matches the user’s intent.
