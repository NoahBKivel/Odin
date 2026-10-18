# Odin

### Your preferences. Your workflows. Across projects.

Odin gives your coding agent a shared set of instructions: how to work, how to communicate, and which focused skills to use. Keep them in one readable folder, bring it into a project, and tell your agent where to start.

**Plain Markdown · No package installation · Portable · MIT licensed**

[Get started](#get-started) · [What's inside](#whats-inside) · [Make it yours](#make-it-yours) · [How it loads](#how-it-loads)

---

## At a glance

| Part | What it does |
| --- | --- |
| **Routing index** | Lists when to load each guideline file or skill. |
| **Shared guidelines** | Keep essential rules active and load task-specific preferences when relevant. |
| **Focused skills** | Add instructions for specific workflows or needs. |
| **One entry point** | Give the agent a single file to read first. |

Odin currently includes shared guidelines and an ADHD communication skill. You can edit both or add your own skills as the bundle grows.

## Get started

1. Keep the `Odin` folder anywhere your coding agent can read it. It does not need to be installed or copied into each project.
2. Send this prompt in your agent's chat:

   ```text
   Read <absolute-path-to-Odin>/START-HERE.md and activate Odin for this conversation. Remember that Odin folder path and use its index to load relevant guidelines and skills as needed. Then continue my task.
   ```

3. Continue with your task. The agent should briefly confirm that Odin and ADHD mode are active.

Replace the placeholder with your folder's actual absolute path. If you move or rename the folder, adjust the path in the prompt.

### ADHD mode

Enabled by default when Odin is activated, the bundled skill shapes responses around clear next actions, short steps, and visible progress.

To turn it off for the current conversation, send:

```text
normal mode
```

You can also say `stop adhd mode`. It stays off in that conversation unless you ask to enable it again.

## What's inside

```text
Odin/
├── START-HERE.md          Activation and context recovery
├── INDEX.md               Guideline and skill routing map
├── guidelines/
│   ├── core.md           Always-active rules
│   ├── coding.md         Code guidance loaded when relevant
│   ├── design.md         Website and interface guidance
│   └── maintenance.md    Guidance for changing Odin
├── skills/
│   └── i-have-adhd/      ADHD communication skill and its license
├── README.md
└── LICENSE.txt
```

## Make it yours

| Want to… | Edit |
| --- | --- |
| Change always-active behavior | [guidelines/core.md](guidelines/core.md) |
| Change coding or design preferences | [guidelines/coding.md](guidelines/coding.md) or [guidelines/design.md](guidelines/design.md) |
| Adjust the included ADHD skill | [skills/i-have-adhd/SKILL.md](skills/i-have-adhd/SKILL.md) |
| Add a focused workflow | Create `skills/<skill-name>/SKILL.md`, then add its trigger and area to [INDEX.md](INDEX.md) |
| Change routing or add a guideline category | [INDEX.md](INDEX.md), following [maintenance guidance](guidelines/maintenance.md) |
| Change what loads at startup | [START-HERE.md](START-HERE.md) |

Keep file references relative so the folder stays portable. Give each new skill a clear purpose and activation condition so the agent knows when to use it.

Guidelines are grouped by task area. Skills stay in their own folders, with task-area tags and triggers in the index so one skill can apply to several areas without duplication. Planning loads guidance for the work being planned; a separate planning file can be added when it has distinct rules.

## How it loads

Odin works through files your agent can read. No package installation or global configuration is required.

At activation, the agent reads the entry point, index, always-active rules, and default communication skill. It loads other guidance when the current task or a change in task area matches an index trigger. It uses already-loaded instructions during work rather than rereading the bundle before every decision.

The agent is instructed to preserve Odin's absolute folder path, routing information, and communication mode through summaries and handoffs, then reread needed files after context loss. This is instruction-based routing, not automatic retrieval or guaranteed memory. Reading a file adds it to conversation context; it does not automatically unload later. If the folder path is lost, the agent must ask for it again.

**Activate it in each new chat.** For automatic loading, reference `START-HERE.md` from your agent platform's recognized project instruction file. Configure that separately and preserve any existing project instructions.

Reading Odin does not register its skills in platform menus. Your instructions, the platform's higher-priority requirements, and existing project instructions still apply.

## License & credits

Odin is licensed under [MIT](LICENSE.txt).

The ADHD skill is adapted from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd), also under MIT. Its original copyright notice and license are preserved in [skills/i-have-adhd/LICENSE](skills/i-have-adhd/LICENSE). Assistant-specific command files and invocation metadata have been removed so the bundle uses one shared, file-based workflow.
