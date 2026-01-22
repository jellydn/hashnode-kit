---
title: "Power-Up #3: OpenCode — Composable AI Agents for Real Coding Workflows"
datePublished: Thu Jan 22 2026 02:18:12 GMT+0000 (Coordinated Universal Time)
cuid: cmkotoe5e000802jv2q5s4sj2
slug: power-up-3-opencode-composable-ai-agents-for-real-coding-workflows
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1769048358793/b6ac629e-23fb-45da-b12f-672073702d15.png
tags: ai, opensource, ai-tools, opencode

---

After experimenting with [**Amp**](https://blog.productsway.com/power-up-1-amp-opinionated-ai-that-fits-real-developer-workflows) and [**Plannotator**](https://blog.productsway.com/power-up-2-plannotator-visual-plan-review-for-coding-agents), I’ve been spending more time with [**OpenCode**](https://opencode.ai/), and it’s quickly becoming one of the most thoughtfully designed AI coding agents I’ve used.

This post focuses on *why OpenCode feels different*, and when you might want to go even further with its experimental fork, [**Shuvcode**](https://github.com/Latitudes-Dev/shuvcode).

## **Surprisingly Good Free Models**

One detail that deserves more attention: **OpenCode ships with genuinely usable free models**.

At the time of writing, free options include:

* opencode/glm-4.7-free
    
* opencode/minimax-m2.1-free
    
* opencode/big-pickle
    

These aren’t toy demos. They’re good enough for:

* Exploration and planning
    
* Lightweight refactors
    
* Reviewing unfamiliar codebases
    

For many workflows, you can stay productive **without paying anything**, and only switch to premium models when needed. That’s a smart, developer-friendly default.

## **Provider-Agnostic by Design**

OpenCode doesn’t lock you into a single model provider.

You can:

* Use built-in free models
    
* Bring your own provider via OpenRouter
    
* Plug in OpenAI, Claude, Gemini, GLM, Qwen, and more
    
* Switch models based on task, cost, or latency
    

This flexibility keeps OpenCode future-proof and practical. You optimize for **your constraints**, not the tool’s.

### **Edge First? Use Shuvcode**

If you enjoy being close to the frontier, **Shuvcode** is worth your attention.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1769048189385/a4098997-2128-4bfa-a45a-95aadf3f0833.png align="center")

Shuvcode is a fork of OpenCode that serves as a proving ground for **new features before they are integrated into the main branch**. If you want to try ideas early, accept some instability, and give feedback upstream, this is the version to run.

Think of it as:

* OpenCode → stable, production-ready
    
* Shuvcode → experimental, fast-moving, opinionated
    

For developers who enjoy testing what’s next, Shuvcode feels like the right playground.

### **Plan vs Build: A Small Idea With Big Impact**

One thing I *really* love about OpenCode is its **two default agents**:

* **Plan** – read-only, safe, exploratory
    
* **Build** – full access, can modify files
    

This separation sounds simple, but it fundamentally changes how you work with AI.

When you’re in *Plan* mode, you can:

* Explore the codebase
    
* Ask “what if” questions
    
* Review ideas without fear of side effects
    

Once you switch to *Build*, changes are intentional and explicit. No accidental edits. No surprise diffs.

It encourages a mindset that mirrors how senior engineers actually work: **understand first, change second**.

### **Sub-Agents You Can Actually Observe**

Another standout feature is **sub-agent visibility**.

When OpenCode delegates work to sub-agents:

* You can see which sub-agent is running
    
* Navigate into it
    
* Observe what it’s doing in real time
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768038189161/1b230a1e-2563-4b4b-b667-ff63a9b76437.png align="center")

Once a sub-agent finishes, it sends a report back to the parent agent. You can then move between agents to understand *how* conclusions were reached, not just the final answer.

This transparency builds trust—and makes debugging AI behavior far easier than black-box systems.

### **Session Sharing That Respects Privacy**

This is a feature I already appreciated in **Amp**, and OpenCode does it well too.

You can:

* [Share a session via a link](https://opncd.ai/share/7cQOvTLV)
    
* Send it to teammates or collaborators
    
* Toggle sessions between **public** and **private** at any time
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1768038836691/f2c55ba4-d865-4f73-b7e3-d91b8c732df7.png align="center")
    

That makes it easy to:

* Review AI-assisted decisions asynchronously
    
* Share debugging context
    
* Collaborate without screen recording or copy-pasting logs
    

For team workflows, this is quietly powerful.

## **Final Thoughts**

OpenCode isn’t trying to be flashy. It’s trying to be **correct**. The agent model, execution visibility, provider freedom, and thoughtful defaults all point in the same direction:

**AI that fits real developer workflows, not demos**.

* If you want stability, start with **OpenCode**.
    
* If you want to see what’s next, explore **Shuvcode**.
    

Either way, this is a strong signal of where AI coding tools are heading, and one worth paying attention to.