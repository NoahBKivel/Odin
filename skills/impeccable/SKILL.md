---
name: impeccable
description: Load for UI/UX work or explicit Impeccable invocation. Apply interface guidance; reserve onboarding and runtime setup for explicit requests.
---

# Impeccable for Odin

This entry point connects Odin to the bundled Impeccable instructions. Keep this adapter and the upstream repository together when copying Odin.

## Activation and scope

Load this skill when UI/UX work begins or the user explicitly invokes Impeccable, then read the full [upstream SKILL.md](../impeccable-main/.agents/skills/impeccable/SKILL.md). Do not load it solely because Odin was activated. Respect explicit opt-outs. Its behavior applies to interface design, implementation, copy, and review, including web and native app interfaces. Stop applying it when work moves outside that scope; mixed tasks use it only for their interface portion. Already-read text may remain in context.

Loading the instructions makes Impeccable available; it does not itself invoke a command, display a menu, initialize a project, or run its launcher. Questions about the skill and maintenance of Odin do not run setup merely because these instructions were read.

For ordinary UI work, read existing project context directly and apply the relevant design guidance without running the launcher. Load only the supporting playbooks needed for that task, and read the upstream craft floor before editing UI. Preserve the distinction between a refinement and a redesign.

### Explicit setup boundary

These Odin-specific limits take precedence over upstream automatic setup and onboarding routes:

- Run the context launcher for an explicitly requested Impeccable command or explicit setup request, following its execution requirements. Ordinary UI work does not trigger it.
- Run the full product interview and create or onboard `PRODUCT.md` only when the user requests `/impeccable init` or explicitly asks for equivalent product onboarding. A missing file alone does not trigger init. If another command routes into init, use existing confirmed context and mark unknowns; ask for needed task facts without starting full onboarding. If the command genuinely requires a product record, explain that dependency and offer init.
- Reserve saved build-path preferences and live-mode configuration for explicit init or a specific request for that setup. Hook installation and enablement remain separately invoked.

The lightweight project-understanding default lives in Odin's core guidelines and applies without Impeccable.

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
