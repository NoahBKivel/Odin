# Odin

Odin is a personal guideline and skill bundle used with an existing coding agent. Merely inspecting it for a review does not activate it.

## Activation

1. Resolve and retain the absolute Odin root from the entry-point path the user supplied. Resolve bundle references against that root, not the project directory. Do not assume Odin is installed or copied into the project.
2. Read `INDEX.md` and `guidelines/core.md`. Keep the routing map and always-active rules available. Load the default skills as directed by the index: the communication skill unless normal mode was requested, and Impeccable unless explicitly disabled. Follow the Impeccable entry point to read its upstream instructions; defer its runtime setup until an applicable design task or requested command.
3. Read guideline files and skills whose index triggers match the current task, then briefly confirm Odin activation and the enabled default skills and continue. Do not read the entire bundle by default.

The user's current instructions and the platform's higher-priority requirements take precedence. Existing project instructions still apply; identify material conflicts instead of silently replacing them. Reading this bundle does not authorize external actions. Inspect bundled scripts before executing them.

## During work

Use the retained index at the start of a task and when the work enters a different area, such as moving from planning to coding or interface design. Read newly applicable guidance before that work. Multiple areas may apply. Do not reopen the whole bundle before every decision, and do not reread a loaded file while its relevant contents remain available unless it changes or needs clarification.

File reads add content to the conversation; they do not provide automatic unloading or guaranteed memory. Keep relevant guidance in summaries rather than copying every loaded file. If a needed instruction is no longer available or remembered reliably, reread its source. Refresh `INDEX.md` when routing is uncertain or the bundle changes.

## Context recovery and handoffs

Preserve the absolute Odin root, entry-point and index paths, always-active rules, current communication mode (including an explicit opt-out), Impeccable's enabled state and runtime setup state, and relevant loaded file paths in summaries and handoffs. Preserve enough of the routing map to find task-specific guidance again. After context loss, use the retained path to reread the entry point, index, and necessary guidance before continuing. Do not reactivate a disabled default skill.

These instructions cannot guarantee retention across platform context resets. If the root path is lost, ask for Odin's location. If the folder is inaccessible, state that limitation rather than claiming to follow unread guidance.
