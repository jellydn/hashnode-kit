---
title: "Looking for a Grok Bot Alternative"
datePublished: 2026-11-02T04:59:32.931Z
cuid: cmvyshtd0000002ns05wwawo3
slug: looking-for-a-grok-bot-alternative
cover: https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/4339bad0-323c-4a32-825a-9a203dcd0db9.jpg
tags: ai, bot, grok-bot

---

I use Grok Bot every day. It drafts my posts, watches my Slack, and has its own cloud computer. It's good. But it's a paid, managed service, and I wanted to answer one question for myself:

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/17750e4b-4802-4673-a21a-d3214babdd1e.png align="center")

**Can I run something similar on my own Mac, with my own models, and still keep a human yes before every write?**

So I started [awesome-bot](https://github.com/jellydn/awesome-bot), a small research repo. Not a ranking. Just notes from actually installing things. This post is the snapshot as of **1 Nov 2026**.

## 1\. What I actually need

My daily work is Slack, Gmail, GitHub, and Sentry. So the bar is:

- Read Slack threads, Gmail, GitHub repos/PRs, and Sentry incidents.
- Run on a schedule and remember useful context.
- Bring my own model (BYOK), ideally self-hosted and always on.
- Least-privilege OAuth, auditable tool calls, and **approval before any write**.

That last one is non-negotiable. An agent that can post to Slack or send email without asking is not an assistant, it's a liability.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/17750e4b-4802-4673-a21a-d3214babdd1e.png align="center")

## 2\. The shortlist

| Platform | How it runs | License | Status |
| --- | --- | --- | --- |
| [Grok Bot](https://x.ai/news/introducing-grok-bot) | Managed | Paid service | Baseline |
| [Rakazo](https://rakazo.com/) | Hosted from $10/mo, desktop app | Apache-2.0 | Tried, not selected |
| [OpenMausBot](https://mausbot.com/) | Desktop / VPS / Docker | Apache-2.0 core | **Current trial** |
| [OpenBot](https://www.copilotkit.ai/openbot) (CopilotKit) | Self-host template | MIT | Watching |
| [OpenHuman](https://tinyhumans.ai/openhuman) | Local core, hosted memory from $20/mo | GPL-3.0 | Tried, Free plan dropped |
| [OpenBot.run](https://openbot.run/) | Desktop, local-first | PolyForm Noncommercial | Tried, fails approval rule |

## 3\. Rakazo: nice pitch, broke on install

Hosted plan is **$10/month** if you bring your ChatGPT or Claude plan, or credits from $20/month. Bots, browser automation, routines, web + desktop + mobile. On paper it's very close to what I want.

In practice, desktop v0.3.5 "This computer" mode failed because the `v0.3.5` container images return 404 (only `edge` exists). Connecting Twitter returned a raw Composio JSON error. I filed both: [#2414](https://github.com/elie222/rakazo/issues/2414) and [#2415](https://github.com/elie222/rakazo/issues/2415).

Keeping it on the list. Not installing it next.

## 4\. OpenBot.run: works with my ChatGPT plan, but no brakes

This one surprised me. It picked up my existing Codex CLI login (ChatGPT plan) and the provider just became available. Supports a long list of agents: Codex, Claude Code, Gemini, Grok, OpenCode, Ollama...

But the agents run with `danger-full-access` and `approvalPolicy: never`. They can change files, run commands, and drive the browser without asking. Also the license is now PolyForm Noncommercial, so not for work use without a separate license.

Fun to try. Fails my approval rule.

## 5\. OpenHuman: the "free" plan isn't really free

I ran the headless core plus web UI from release `v0.64.20` (main didn't compile for me). The local setup is fine.

The catch is memory. On the Free account, the memory API returns `MEMORY_PLAN_REQUIRED` (403). Hosted memory starts at **$20/month** (Basic) or **$200/month** (Pro), and the page says payments and credits are non-refundable.

So the Free plan is out. If I come back, it's with a paid plan or not at all.

## 6\. OpenMausBot: my current trial

[OpenMausBot](https://github.com/milind-soni/OpenMausBot) (formerly OpenGrokBot) is the one I'm still running. Apache-2.0 core, works with Codex/Claude/Grok CLIs, has schedules, webhooks, phone pairing, MCP, and approval cards for risky actions.

My setup:

- Harness on `127.0.0.1:8799`, Vite UI on `5199`, Electron off.
- One `just up` starts both and opens a Cloudflare tunnel to `bot.itman.fyi`.
- A remote browser must **pair** with a code before it can call the API.

One gotcha that cost me time: don't rewrite the Host header in the tunnel. If you do, the same-origin check fails with `forbidden: cross-origin request`.

Two things to watch: API keys sit in local config as plaintext (file mode 0600), and Slack/Gmail/GitHub go through Composio, which may cost extra. Sentry is still unverified.

## 7\. OpenBot (CopilotKit): the one I'm watching

Different project, same name. It's an MIT template you clone and run. What I like: every tool call goes through a gateway that **writes an audit row before the call**. That's the right shape. I haven't put it through the same hands-on run yet.

## 8\. Honest status

None of them has passed the real test yet. Slack, Gmail, GitHub, and Sentry were not fully connected in any run. Sentry support is unverified everywhere.

And a reminder to myself: **an advertised integration is not proof** of real OAuth scopes, two-way actions, or unattended runs.

The real test is one workflow:

1. Pull a Sentry issue and stack trace.
2. Find related GitHub commits and PRs, with citations.
3. Search Slack for the incident discussion.
4. Prepare a Gmail draft with a summary and links.
5. **Wait for my yes** before sending or posting anything.

## 9\. The shape I want

```text
Web / mobile UI
      |
Agent orchestrator --- Model gateway (BYOK / local LLM)
      |
Tool permission gateway
  |       |       |       |
Slack   Gmail   GitHub  Sentry
      |
Audit logs + approval + scheduler + state
```

Start read-only. Add writes later, behind approval.

## Wrap up

For now Grok Bot stays my baseline, and OpenMausBot is the self-hosted one I keep running. The repo is open, so if you've tested one of these (or one I missed), PRs are welcome. Please bring a version, a date, and whether you **tested** it or just **read** about it.

Cheap agents are easy. Agents you can trust with your inbox are not.

Repo: <https://github.com/jellydn/awesome-bot>

#ITMan #AI #SelfHosted #OpenSource