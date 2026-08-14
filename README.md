# DashClaw Agent Skills

Reusable [Agent Skills](https://skills.sh) for working with **[DashClaw](https://dashclaw.io)** — the governance runtime for AI agents (policy enforcement, decision recording, human approvals, and risk signals).

These skills teach any skill-aware agent (Claude Code, Cursor, Codex, Copilot, Gemini, OpenClaw, and others) how to set up DashClaw, instrument an agent with the governance loop, author policies, run approvals, and troubleshoot.

## Install

Install all skills with one command:

```bash
npx skills add ucsandman/dashclaw-skills
```

Preview without installing, or pick a subset:

```bash
npx skills add ucsandman/dashclaw-skills --list
npx skills add ucsandman/dashclaw-skills --skill setup-dashclaw
```

Install globally (available in every project) and target specific agents:

```bash
npx skills add ucsandman/dashclaw-skills -g -a claude-code -a cursor
```

## Skills

| Skill | What it does |
|-------|--------------|
| **setup-dashclaw** | Stand up a DashClaw instance, install the CLI, and configure Claude Code hooks. |
| **instrument-agent** | Integrate the DashClaw SDK into any agent using the 4-step governance loop. |
| **register-on-dashclaw** | Register an agent as a governed agent on a DashClaw instance. |
| **create-policies** | Create and test guard policies for agent governance. |
| **manage-approvals** | Human-in-the-loop approval workflows for governed actions. |
| **dashclaw-governance** | Runtime governance behavior: when to call `guard`, how to interpret `allow`/`warn`/`block`/`require_approval`, recording actions, waiting for approvals, session lifecycle. Use with `@dashclaw/mcp-server`. |
| **compliance-drift-evals** | Compliance exports, drift detection, evaluations, scoring, and learning analytics. |
| **troubleshoot** | Debug DashClaw errors, signal issues, and misconfigurations. |
| **dashclaw-platform-intelligence** | Platform expert for integration, troubleshooting, and governance. Prefers live queries against a running instance. |
| **build-dashclaw** | Contribute to the DashClaw codebase — architecture, scaffolding, tests, and CI. For OSS contributors. |

## What is DashClaw?

DashClaw is a minimal **governance runtime, not an agent platform**: it doesn't give agents tools to achieve goals — it provides the infrastructure to *govern* those goals. The core loop is **guard → act → record → (optionally) wait for approval**.

- Product & docs: <https://dashclaw.io/docs>
- Source & the full Claude Code plugin (MCP server + hooks): <https://github.com/ucsandman/DashClaw>

The plugin (MCP server, hooks, and the same governance/platform-intelligence skills) is also installable directly from the main repo's Claude Code marketplace.

## License

MIT © DashClaw. See [LICENSE](./LICENSE).

## Support

If my tools save you time, you can support my work here:

[![Sponsor on GitHub](https://img.shields.io/badge/GitHub%20Sponsors-%E2%9D%A4-db61a2?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/ucsandman)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-%E2%98%95-ffdd00?logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/wes_sander)
