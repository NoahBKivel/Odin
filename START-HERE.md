# Odin

Read `guidelines/core.md` and `skills/i-have-adhd/SKILL.md` before working. Activate ADHD mode automatically whenever Odin is activated, unless the user has explicitly requested normal mode. This default is configured in Odin itself, so project instruction files only need to reference this entry point. Paths in this bundle are relative to this folder, regardless of its name or location.

Apply these guidelines throughout the current conversation. Preserve them when summarizing context or handing off work. If the bundle is no longer available after a context reset, say so and request its location rather than claiming to follow unread instructions.

The user's current instructions and the platform's higher-priority requirements take precedence. Existing project instructions still apply; identify material conflicts instead of silently replacing them.

## Skills

Read a skill's full `SKILL.md` before using it. Treat bundled scripts as executable code: inspect them before running them. Installing or reading this bundle does not authorize external actions.

| Skill | When to use | Location |
| --- | --- | --- |
| i-have-adhd | Automatically when Odin is activated, unless the user has requested normal mode; also when explicitly invoked. | `skills/i-have-adhd/SKILL.md` |

ADHD mode persists in the current conversation until the user says `stop adhd mode` or `normal mode`. Activating Odin also activates this skill by default. Merely inspecting these files for a review does not activate either. After the user disables ADHD mode, do not reactivate it during the same conversation unless the user asks.

Confirm activation of Odin and ADHD mode briefly (or Odin alone if ADHD mode is disabled), then continue the user's task. Do not read every skill and reference by default.
