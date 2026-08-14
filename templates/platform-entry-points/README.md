# Platform entry-point templates

These files connect one vendor-neutral `PROJECT_CONSTITUTION.md` to a particular agent environment.
They are carriers, not separate constitutions.

1. Create and approve `PROJECT_CONSTITUTION.md` using the
   [`constitutional document skeleton`](../constitutional-document-skeleton.md).
2. Copy the entry-point template for your environment into the location named below.
3. Replace every bracketed placeholder.
4. Keep the approved Operating Card in the entry point so the load-bearing mission is present even
   before the agent opens the full constitution. Record the constitution's version, date, or digest
   beside it and update both when the constitution changes.
5. Start a clean session and run the loading check in the
   [`implementation guide`](../../docs/implementation-guide.md).

| Environment | Copy | Destination |
|---|---|---|
| Codex | [`codex-AGENTS.md`](codex-AGENTS.md) | Repository root as `AGENTS.md` |
| Claude Code | [`claude-CLAUDE.md`](claude-CLAUDE.md) | Repository root as `CLAUDE.md` |
| ChatGPT Project | [`chatgpt-project-instructions.md`](chatgpt-project-instructions.md) | Project Instructions; upload `PROJECT_CONSTITUTION.md` as a project source |
| API or custom runtime | [`generic-system-instructions.md`](generic-system-instructions.md) | The runtime's system/developer configuration or explicit loader |

When a repository supports multiple environments, keep multiple small entry points that reference
the same canonical constitution. Do not create a different mission for each vendor.
