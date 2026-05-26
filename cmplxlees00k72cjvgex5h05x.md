---
title: "Power-Up #6: My AI Launcher"
datePublished: 2026-05-26T01:03:03.991Z
cuid: cmplxlees00k72cjvgex5h05x
slug: power-up-6-my-ai-launcher
cover: https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/e347ea58-92ba-4f63-bf3a-b869775093af.jpg
ogImage: https://cdn.hashnode.com/uploads/og-images/56ee654dbcca2d711e191e2a/95034ee2-cfb8-42e3-97f8-628d10cd5c1e.jpg
tags: ai, ai-tools

---

AI coding tools are everywhere now: Claude Code, Codex, OpenCode, Amp, Pi, etc.

The problem is not “which AI is best” anymore. The real problem is: *How do you actually integrate them into your daily workflow without friction?*

That’s why I built: [AI Launcher](https://github.com/jellydn/ai-launcher)

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/504636dc-f015-4ab9-a56f-584c7b2cca93.png align="center")

A simple CLI launcher that turns multiple AI coding tools into one composable workflow. Instead of remembering dozens of commands, flags, prompts, and models, I now use a single command:

```shell
ai
```

Simple idea but surprisingly powerful.  

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/4db752aa-bc88-4947-881e-2217e53fb507.png align="center")

## Why I Built It

### Most AI tools today work like isolated products.

You open one tool: copy context, paste prompts, run commands, switch windows/terminal. Repeat.

That breaks developer flow. I wanted something closer to Unix philosophy:

*   composable
    
*   pipe-friendly
    
*   terminal-native
    
*   scriptable
    
*   lightweight
    
*   model-agnostic
    

## My Favorite Workflows

### Review outdated packages

`bun outdated | ai review`

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/06bad86b-f288-4438-b7aa-6bd79bebd841.png align="center")

This becomes surprisingly useful.

AI can:

*   Analyze risky upgrades
    
*   Identify breaking changes
    
*   Prioritize updates
    
*   Suggest migration paths
    

### Auto commit + PR flow

`ai ac && git push && ai pr`

This workflow:

1.  Analyzes staged changes
    
2.  Generates atomic commit messages
    
3.  Pushes changes
    
4.  Creates a draft PR automatically
    

It feels like having a lightweight AI release assistant inside Git.

### Tidy First workflow

`git diff | ai tidy`

I use this a lot before merging code.

The AI applies “Tidy First” principles:

*   guard clauses
    
*   dead code cleanup
    
*   normalize symmetry
    
*   simplify expressions
    
*   improve readability
    

Not rewriting the architecture. Just making the code easier to understand.

### The Real Superpower: Templates

The launcher itself is intentionally dumb. The power comes from reusable templates.

Example:

```json
{ 
 "name": "review-security", 
 "aliases": ["sec"], 
 "command": "ccs ghcp --permission-mode plan -p 'Security review: Check for injection vulnerabilities, input validation, auth issues, and sensitive data handling in: $@'" 
}
```

Now this becomes:

`ai sec src/auth.ts`

Or:

`git diff | ai sec`

Very small abstraction, but over time, these tiny abstractions compound heavily.

## My Philosophy

I no longer think: *“Which AI tool should I use?”* Instead, I think: *“Which workflow should AI automate?”*

That shift matters. The future is probably not one giant AI IDE. The future is:

*   composable AI utilities
    
*   programmable workflows
    
*   terminal-native automation
    
*   AI integrated into existing developer habits
    

AI Launcher is my small experiment in that direction.

## My Current Setup

[Here’s part of my setup:](https://github.com/jellydn/my-ai-tools/blob/main/configs/ai-launcher/config.json)

*   Claude CLI
    
*   OpenAI Codex
    
*   OpenCode
    
*   Amp
    
*   Pi
    
*   CCS workflows
    

With reusable templates for:

*   review
    
*   atomic commits
    
*   PR generation
    
*   security review
    
*   refactoring
    
*   performance analysis
    
*   TypeScript improvements
    
*   AI slop cleanup
    
*   tidy-first cleanup
    
*   documentation
    
*   tests
    

Everything accessible from:

`ai`

Example Config  

```json
{ 
 "name": "commit-atomic", 
 "aliases": ["ac"], 
 "command": "opencode run --model opencode/deepseek-v4-flash-free --agent build 'Run git diff --staged then do atomic commit message for the change with commitizen convention.'" 
}
```

Which enables:

`ai ac`

That tiny command now saves real cognitive load every day.

## Final Thoughts

The best AI workflows are often:

*   boring
    
*   tiny
    
*   scriptable
    
*   composable
    
*   deeply integrated into your existing habits
    

Not flashy demos. Just practical leverage. That’s what AI Launcher is for me.