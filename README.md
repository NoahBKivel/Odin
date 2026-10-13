# Odin

A portable instruction bundle for coding agents. Drop this folder into a project, then send:

```text
Read Odin/START-HERE.md and follow its guidelines for this conversation. Read and apply relevant skills from the bundle when instructed. Then continue my task.
```

Adjust the path if you rename or move the folder. Activating Odin automatically enables the bundled ADHD skill. To disable it, say:

```text
normal mode
```

## What plug and play means here

The files can be read directly; no package installation or global configuration is required. Any agent assistant with access to the folder can use the same explicit reading prompt and shared instructions.

This does not automatically register the skills in platform menus, override higher-priority instructions, or make every new chat read the bundle. Activate it in each new chat. For automatic loading, add a reference from the platform's recognized project instruction mechanism; configure that separately and preserve any existing instructions.

## Edit the bundle

- `START-HERE.md`: entry point and skill index.
- `guidelines/core.md`: shared requirements and things to avoid.
- `skills/<skill-name>/SKILL.md`: each focused workflow, with supporting files alongside it.

Update the skill index when adding a skill. Keep file references relative so the whole folder remains movable.

Odin is licensed under MIT; see [LICENSE.txt](LICENSE.txt).

The included ADHD skill is adapted from https://github.com/ayghri/i-have-adhd under MIT. Its original copyright notice and license are preserved in [skills/i-have-adhd/LICENSE](skills/i-have-adhd/LICENSE). Assistant-specific command files and invocation metadata have been removed so the bundle uses one shared, file-based workflow.
