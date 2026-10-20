---
name: impeccable
description: Load with Odin by default. Apply Impeccable to interface design and development, and support manually requested Impeccable commands.
---

# Impeccable for Odin

This entry point connects Odin to the bundled Impeccable instructions. Keep this adapter and the upstream repository together when copying Odin.

## Activation and scope

Load this skill when Odin is activated, then read the full [upstream SKILL.md](../impeccable-main/.agents/skills/impeccable/SKILL.md). Keep Impeccable enabled throughout the conversation unless the user explicitly disables it. Its behavior applies to interface design, implementation, copy, and review, including web and native app interfaces. Unrelated work continues under the other applicable Odin guidelines.

Loading the instructions makes Impeccable available; it does not itself invoke a command, display a menu, initialize a project, or run its launcher. Defer upstream Setup until the first applicable design task or requested command in the session. Questions about the skill and maintenance of Odin do not run that setup merely because these instructions were read.

For an applicable task, follow upstream Setup and routing. Ordinary design requests use its default design workflow without requiring a command. Load only the supporting playbooks needed for that task, and read the upstream craft floor before editing UI. Preserve the distinction between a refinement and a redesign.

## Paths and execution

Resolve the upstream skill base directory from Odin's retained absolute root:

`skills/impeccable-main/.agents/skills/impeccable/`

Resolve upstream `reference/`, `scripts/`, and `agents/` paths against that directory. Replace provider-specific relative launcher paths such as `.agents/skills/impeccable/scripts/impeccable` with the absolute path to this bundled launcher. Keep the working directory at the user's target project, not Odin or the upstream repository. On Windows without `sh`, use the bundled `scripts/impeccable.cmd`.

Inspect the launcher before first execution. It can download the pinned engine when no installed binary is available. If it cannot run, follow upstream's launcher-unavailable fallback and state which automated checks remain unavailable. Reading Odin does not install native hooks or register platform commands.

## Manual commands

Accept `/impeccable <command> [target]`, `$impeccable <command> [target]`, or a plain-language request such as "run impeccable audit on the settings page". These are chat instructions routed through this skill, even when the platform has no native slash-command registration.

Use the Commands table and routing in the loaded upstream SKILL.md as the command authority. Read the selected command's reference and follow it with the resolved paths above. A bare Impeccable invocation presents the upstream context-aware menu; it does not choose and run a command for the user. Preserve upstream's additional `hooks`, `doctor`, and pin/unpin routes when explicitly requested.

## Odin preferences and recovery

The user's instructions, platform requirements, and existing project instructions retain their priority. Apply Odin's [design preferences](../../guidelines/design.md) to interface work; those specific preferences take precedence over general upstream design advice. Keep communication-mode settings independent: `normal mode` or `stop adhd mode` disables the ADHD skill, not Impeccable.

Preserve the Impeccable enabled state, upstream skill base directory, relevant loaded references, and whether context setup ran for the target project in summaries and handoffs. Recover the instructions from these paths when needed; do not claim a previous setup ran if that state is unknown.

Upstream content remains under its [Apache-2.0 license](../impeccable-main/LICENSE) and [third-party notices](../impeccable-main/NOTICE.md).
