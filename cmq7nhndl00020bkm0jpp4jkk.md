---
title: "Power-Up #7: Let AI Research Your Code While You Sleep"
datePublished: 2026-06-10T05:51:08.728Z
cuid: cmq7nhndl00020bkm0jpp4jkk
slug: power-up-7-let-ai-research-your-code-while-you-sleep
tags: AI

---

In the previous Power-Up posts, I've explored AI coding assistants, AI workflows, agent-based development, and AI launchers.

This week, I want to talk about something that feels like the next step: [autoresearch](https://github.com/karpathy/autoresearch).

The idea comes from Andrej [Karpathy's autoresearch](https://github.com/davebcn87/pi-autoresearch) project and has recently been brought to Pi through pi-autoresearch.

![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/babe34e8-1e3a-461b-b43c-9d3c0003ffec.png align="center")

Instead of asking AI to generate code, we ask AI to improve a measurable outcome.

For example:

*   Reduce startup time
    
*   Improve benchmark scores
    
*   Reduce memory usage
    
*   Increase test coverage
    
*   Reduce bundle size
    

The workflow is surprisingly simple:

1.  Give the agent a goal
    
2.  Let it propose a change
    
3.  Run tests and benchmarks
    
4.  Measure the result
    
5.  Keep improvements
    
6.  Revert regressions
    
7.  Repeat  
    
    ![](https://cdn.hashnode.com/uploads/covers/56ee654dbcca2d711e191e2a/babe34e8-1e3a-461b-b43c-9d3c0003ffec.png align="center")
    

The key difference is that the agent is no longer optimizing for "writing code."

It is optimizing for outcomes.

Traditional AI coding:

Goal → Prompt → Code

Autoresearch:

Goal → Experiment → Measure → Improve → Repeat

This is important because software engineering is fundamentally an optimization problem.

The best solution is rarely obvious from a single prompt.

Human engineers already work this way:

*   Form a hypothesis
    
*   Make a change
    
*   Run tests
    
*   Analyze results
    
*   Iterate
    

Autoresearch simply automates that loop.

I recently tested pi-autoresearch on one of my projects. What impressed me wasn't the code generation itself.

It was the process.

The agent created experiments, validated assumptions, measured results, and produced a pull request with supporting evidence.

That feels much closer to having a junior performance engineer than a code generator.

Why this matters:

*   Less prompt engineering
    
*   More measurable improvements
    
*   Discover non-obvious optimizations
    
*   Fully reproducible experiments
    
*   Works while you focus on other tasks
    

I don't think autoresearch will replace developers.

But I do think it points toward a future where AI agents spend more time experimenting and less time waiting for instructions.

What would you ask an AI agent to optimize in your codebase?  
  
#ITMan #AI