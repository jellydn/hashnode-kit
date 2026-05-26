---
title: "Power-Up #4: My AI Workflow
"
datePublished: 2026-04-07T02:30:00.000Z
cuid: cmno05foc000121cld220gquf
slug: power-up-4-my-ai-workflow
cover: https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/ee7e716d-7cf1-46fe-a6ed-04ae2166fecd.jpg
ogImage: https://cdn.hashnode.com/uploads/og-images/56ee654dbcca2d711e191e2a/78b879a4-6d1a-44d8-bd88-6a2610307a2f.png
tags: AI

---

In the previous post, I shared about OpenCode works. Now, let’s go one level deeper. This is the exact workflow I use daily to ship code faster, combining GitHub issue, Copilot Agent, and multiple AI reviewers into a single pipeline.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/ffc4375e-93ab-4b20-a8a6-a4afece8ec62.png align="center")

## **The Big Idea**

AI is not a single tool. It’s a **system of agents** working together:

*   One writes code
    
*   Others review
    
*   Others validate
    
*   You orchestrate
    

## **Step 1 — Start with a Real Issue**

Every task begins with a clearly defined issue:

👉 [https://github.com/jellydn/my-ai-tools/issues/174](https://github.com/jellydn/my-ai-tools/issues/174)

This is critical because:

*   AI needs context
    
*   Reviews need scope
    
*   You need a single source of truth
    

A vague issue = weak AI output.

## **Step 2 — Let Copilot Do the First Draft**

  
Instead of writing code from scratch, I assign the issue to Copilot then in will open PR and work on it:

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/091d9a73-881a-44ad-99b4-7d54172a4c94.png align="center")

👉 [https://github.com/jellydn/my-ai-tools/pull/175](https://github.com/jellydn/my-ai-tools/pull/175)

At this stage:

*   Copilot generates the implementation
    
*   I review direction, not syntax
    

## **Step 3 — AI Code Review with CodeRabbit**

Before touching anything manually, I run an AI review.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/7721acce-2687-41f5-b4c6-aac548e8a60d.png align="center")

CodeRabbit helps:

*   Catch bugs early
    
*   Identify bad patterns
    
*   Suggest improvements
    

This is your **first quality gate**.

## **Step 4 — Pull PR Locally**

Next, I check out the PR locally using:

👉 [https://github.com/tobi/try](https://github.com/tobi/try/pull/30)

This makes it trivial to clone repository and manage under src/tries folder:

*   Checkout PRs
    
*   Run the code
    
*   Validate behavior
    

No friction = more testing.

## **Step 5 — Multi-Agent Review (This Is the Game Changer)**

Now comes the most powerful part. I don’t rely on a single AI. I run multiple agents:

*   Codex
    
*   OpenCode
    
*   Pi
    
*   Claude Code
    

Each one:

*   Thinks differently
    
*   Finds different issues
    
*   Suggests different improvements
    

This creates a **diverse review system**, similar to having multiple senior engineers.

## **Final Thoughts**

This workflow helps me:

*   Ship faster
    
*   Maintain high quality
    
*   Reduce mental load
    

The key is not better prompts. It’s better **orchestration**.