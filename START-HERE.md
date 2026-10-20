# Odin

Odin is a personal guideline and skill bundle used with an existing coding agent. Merely inspecting it for a review does not activate it.

## Activation

1. Resolve and retain the absolute Odin root from the entry-point path the user supplied. Resolve bundle references against that root, not the project directory. Do not assume Odin is installed or copied into the project.
2. Read `INDEX.md` and `guidelines/core.md`. Keep the routing map and always-active rules available. Load the default skills as directed by the index: the communication skill unless normal mode was requested, and Impeccable unless explicitly disabled. Follow the Impeccable entry point to read its upstream instructions; defer its runtime setup until an applicable design task or requested command.
3. Read guideline files and skills whose index triggers match the current task, then give the activation response below and continue. Do not read the entire bundle by default.

The user's current instructions and the platform's higher-priority requirements take precedence. Existing project instructions still apply; identify material conflicts instead of silently replacing them. Reading this bundle does not authorize external actions. Inspect bundled scripts before executing them.

## Activation response

After loading the required guidance, send the entire predefined intro below together in one reply and one fenced `text` block. Keep the ODIN wordmark unboxed. Preserve the wording, textured lettering, table layout, and order. Do not split the banner, status, or guide across messages or code blocks, or print parts as separate progress updates.

Substitute `{odin_status}` with `ACTIVE` after successful loading or `PARTIALLY LOADED` if required guidance could not be loaded. Replace `{adhd}` and `{design}` with each skill's actual state: `on`, `off`, or `unavailable`, respecting explicit opt-outs. Pad the state cells with spaces to keep their columns aligned. If loading failed, add one brief `Loading:` explanation inside the same block immediately after the status line.

The commands are reference text, not requests to execute them during activation. This template is the authoritative intro; reproduce it instead of composing a new summary.

```text
    .:oOo:.      .:oO88Oo:.       .:oO88Oo:.    .:oO:.     .:Oo:.
  .x8@WW@8x.     x8@W##MW@8:      x8@W##W@8x    x8W@Bx.    xB@W8x
 :B@M##MM@B:     B@MWW##MM@Bx     '7BW@@WB7'    B@M#W8x.   B8W#M@
 7@MWx::xW@M7    M@W8x::x8W@M.      :W@M#:      M@W8B@W7   W@M##W
 M@W8:  :8W@M    W@M#:  :#M@W:      :M@W8:      W@M#xW@Br  M@W88M
 W@M#:  :#M@W    M@W8:  :8W@M:      :W@M#:      M@W8:B@MW: W@M##W
 M@W8:  :8W@M    W@M#:  :#M@W:      :M@W8:      W@M#: xW@B8M@W88M
 7M@Wx::xW@M7    M@W8x::x8W@M'      :W@M#:      M@W8:  7B@WMM@##W
 :B@MM##M@B:     B@MM##WWM@B7     .xBW@@WBx.    B@M#x   :W@M#W@8B
  'x8@WW@8x'     x8@WM##W@8'      x8@W##W@8x    x8W@r    'B@W@M8x
    ':oOo:'      ':oO88Oo:'       ':oO88Oo:'    ':oO:     ':O8o:'

STATUS / {odin_status}

MODES
+--------------+-------------+----------------------------------------+
| MODE         | STATE       | INCLUDES                               |
+--------------+-------------+----------------------------------------+
| ADHD         | {adhd}      | Clear steps and visible progress       |
| Impeccable   | {design}    | Interface design, building, and review |
+--------------+-------------+----------------------------------------+

QUICK COMMANDS
+-----------------------------------+---------------------------------+
| SAY / TYPE                        | ACTION                          |
+-----------------------------------+---------------------------------+
| normal mode                       | Turn ADHD mode off              |
| enable ADHD mode                  | Turn ADHD mode on               |
| disable Impeccable                | Turn design guidance off        |
| enable Impeccable                 | Turn design guidance on         |
| /impeccable                       | Browse design commands          |
| /impeccable shape [feature]       | Plan UX/UI before coding        |
| /impeccable audit [target]        | Accessibility, speed, resizing  |
| /impeccable polish [target]       | Give the interface a final pass |
+-----------------------------------+---------------------------------+

Use chat instructions or ask in plain language.
Project guidelines load as needed.
```

Then continue the user's task in the same reply. If no task was supplied, briefly invite the user to give one. Show this greeting once per explicit activation, not during routine task changes or context recovery. Honor requests to skip or change the greeting.

## During work

Use the retained index at the start of a task and when the work enters a different area, such as moving from planning to coding or interface design. Read newly applicable guidance before that work. Multiple areas may apply. Do not reopen the whole bundle before every decision, and do not reread a loaded file while its relevant contents remain available unless it changes or needs clarification.

File reads add content to the conversation; they do not provide automatic unloading or guaranteed memory. Keep relevant guidance in summaries rather than copying every loaded file. If a needed instruction is no longer available or remembered reliably, reread its source. Refresh `INDEX.md` when routing is uncertain or the bundle changes.

## Context recovery and handoffs

Preserve the absolute Odin root, entry-point and index paths, always-active rules, current communication mode (including an explicit opt-out), Impeccable's enabled state and runtime setup state, and relevant loaded file paths in summaries and handoffs. Preserve enough of the routing map to find task-specific guidance again. After context loss, use the retained path to reread the entry point, index, and necessary guidance before continuing. Do not reactivate a disabled default skill.

These instructions cannot guarantee retention across platform context resets. If the root path is lost, ask for Odin's location. If the folder is inaccessible, state that limitation rather than claiming to follow unread guidance.
