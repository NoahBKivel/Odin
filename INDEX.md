# Odin index

Keep this routing map and the resolved absolute path of the Odin root available throughout the conversation. All paths below are relative to that root. This is a file-based bundle; no skill installation or platform registration is required.

## Guidelines

| Area | Read when | Path |
| --- | --- | --- |
| Always active | At activation; retain throughout the conversation | `guidelines/core.md` |
| Coding | Before code exploration, implementation, debugging, or review | `guidelines/coding.md` |
| Design | Before website or interface design, implementation, copywriting, or review | `guidelines/design.md` |
| Odin maintenance | Before changing this bundle or its organization | `guidelines/maintenance.md` |

Planning uses the always-active rules plus guidance for the work being planned. There is no separate planning file yet; add one when distinct planning preferences justify it. Tasks can match multiple areas.

## Skills

Skills are procedures or specialized behavior, while guidelines express standing preferences. Store skills separately and use task-area tags here to route to them. Read the full `SKILL.md` before applying a skill; open its supporting references only as needed.

| Skill | Area | Trigger and duration | Path |
| --- | --- | --- | --- |
| i-have-adhd | Communication | Load at activation unless normal mode was requested. Remains active until the user says stop adhd mode or normal mode; reactivate only on request. | `skills/i-have-adhd/SKILL.md` |
