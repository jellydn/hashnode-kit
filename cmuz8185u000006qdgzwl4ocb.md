---
title: "Power-Up #8: Three Months with Amp Orb: From CLI to Cloud Agents"
datePublished: 2026-10-08T07:34:50.529Z
cuid: cmuz8185u000006qdgzwl4ocb
slug: power-up-8-three-months-with-amp-orb-from-cli-to-cloud-agents
tags: cloud-ai-agents, cloud-agents, amp-code

---

I've been using [Amp](https://ampcode.com/) Orbs for about three months, and it has changed how I build software.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/14ef8499-b93b-4035-a1df-4988840ed0f6.png align="center")

I've used AI coding assistants for a long time, from terminal agents to IDE integrations. Amp is the first one that changed where my time goes. I spend less time talking to a coding agent and more time deciding what to build and reviewing what got built.

And a surprising amount of that now happens on my phone.

### The CLI worked, but ...

My old loop looked like this:

Open the laptop and terminal. Go to the project. Start the agent. Explain the task. Wait for the implementation and tests. Review. Repeat. It worked. But I still had to manage the environment, watch progress, and keep coming back to the terminal. Even when the agent could work on its own, it only moved forward when I pushed it.

The agent was helping me write code, but I was still managing the agent.

### From CLI to cloud agents

With cloud Orbs, tasks run in remote environments instead of on my laptop.

I start something, walk away, and come back when there's something to review. That changes the question I ask myself. It used to be: I have 30 minutes. What can I implement?

Now it's:

I have an idea. Can I hand it off now and review it later?

When you're juggling several projects, that difference adds up fast.

### Puck plans and coordinates the work

Instead of talking to individual agents all day, I talk to Puck. It plans the implementation, breaks it into smaller tasks, and coordinates the work.

I've given Puck my engineering preferences once, so I don't repeat them every conversation:

Propose a plan before making changes. Break complex tasks into manageable steps. Follow modular design and self-documenting code. Run code-quality reviews. Check pull requests before calling the work done. Ask before doing anything destructive. My favourite one:

Code is communication. Prefer clarity and simplicity.

So I start every conversation on the problem, not on my coding philosophy.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/10273d88-5508-4d7e-9ef4-1b6f80140bf6.png align="center")

### Starting work from my phone

This is the biggest change in my day. Ideas used to wait until I was back at my desk. Now I open Amp on my phone, talk the idea through with Puck, and start the work. Later I check progress, open the pull request, or leave feedback.

My loop is now: Idea -> Plan -> Delegate -> Review -> Merge

That doesn't mean I trust everything blindly. I still review the implementation, the architecture, the tests, and the security. I just don't have to supervise every step.

### My Mac works as a runner too

Amp doesn't force everything into its cloud. My Mac already has my repos, dependencies, and tools, so I can enable it as a runner, start a task from the web or mobile app, and have it run on my own machine.

Cloud Orbs My Mac runner Where it runs Amp's cloud My own hardware Needs my Mac online No Yes Environment Separate, fresh My existing setup Compute cost Cloud charges may apply No extra Amp cloud compute charge Best for Isolated tasks Existing local projects Not every task needs the cloud. Sometimes the best place to run it is the computer I already own.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/a3ecb1b9-53d4-4266-9c80-356edf0a6776.png align="center")

### Bring your own AI subscription

I already pay for several AI services, and I don't want to pay for the same capability twice.

Amp lets me connect supported subscriptions and providers, including ChatGPT and X Premium+/SuperGrok, and I can add OpenCode Go, OpenRouter, and others. That means I can pick a model per job: one for planning, another for implementation or review.

It doesn't make everything free. Cloud compute, subscription limits, and extra model usage still cost money. But I decide where that money goes.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/2cd61359-cd56-4f97-936a-6a3032780b12.png align="center")

### You don't need the top plan

I'm on Amp's Megawatt tier and don't feel any need to upgrade. My setup is:

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/902555e4-630b-4a91-b305-290d6f7be9bb.png align="center")

Subscriptions I already have Amp's model routing Cloud Orbs when I need them My Mac as a runner Puck for coordination Orb sizes help too. A small project gets a small Orb. A heavy build or test suite gets a bigger one.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/606a5821-97ac-4428-b625-52a7d6a37514.png align="center")



### What I still review myself

Delegating the implementation doesn't mean delegating responsibility.

Agents can write code, run tests, and open pull requests. That doesn't make the work correct. I still check:

Does it actually solve the problem? Is the architecture right? Are there security concerns? Do the tests mean anything? Is it more complicated than it needs to be? Will it be maintainable? I use code-review tools too. The goal isn't to remove human review. It's to spend my review time on real results instead of on babysitting each step.

### What I've learned, and where this is going

For years we've pushed AI to write better code: better models, longer context, better tool calling, better benchmarks. That matters.

But after two months with Amp, I think the next big shift is how we work with AI. We'll spend less time supervising assistants and more time defining problems, designing systems, reviewing results, and making architecture calls, from wherever we are.

It isn't perfect. There are limits, costs, and times when writing the code myself is faster. But I don't want to go back to a workflow where everything depends on keeping a terminal open.

I still love writing code. I love building things even more, and this workflow gives me more time to do that.