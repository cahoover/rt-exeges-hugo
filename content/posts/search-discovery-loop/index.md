---
author: "Christopher Hoover"
title: "Search as Part of an Iterative Discovery Loop"
date: "2026-04-10"
tags:
- Exeges
- exploration
- architecture
---
Most systems think in terms of search first, analytics second. But once a corpus becomes large, heterogeneous, and dynamic enough, that sequence starts to struggle.

As the depth and breadth of data grow, search can start to wander, analytics can become brute force, and graphs can become more of an ornament than a provider of real context. This is a real challenge if you aren't sure what you're looking for, and you don't know what's available to explore.

Exeges approaches this challenge with an iterative discovery loop. In each round, search converts an underspecified question into the next bounded investigative move. The graph/lexical/vector stack helps decide what's worth computing by evaluating topology, neighborhood, joinability, coverage, prior outcomes, and known dead ends. 

Every round produces a durable checkpoint that informs the next one. Checkpoints describe what was done and what was found, and inform the next planning pass about what was already tried, what succeeded, what failed, and what inputs produced which outcome.

For example, imagine a bill with forty changed sections. The first pass does not ask the machine to “understand the whole bill.” It publishes a CandidateSet that says, in effect: compare sections 101, 302, and 401 first, because they changed and they join cleanly to downstream budget measures. The planner can see that those sections have not yet been analyzed in the same way with the same inputs, so it does not waste a cycle re-running the same work. 

Those three work items are then run, and a checkpoint is written for each with a stable work-item key, a status, an input digest, and pointers to the output manifests. When the next round begins, the planner can see that section 101 already succeeded, section 302 failed, and section 401 surfaced the strongest signal. So the next move is not “search again,” it's: skip 101, retry 302, and widen the neighborhood around 401. The checkpoint turns exploration from repeated searching into cumulative investigative work.

Compare this to the typical RAG/GraphRAG stack: a user asks a question, the system finds documents, maybe ranks and summarizes them, maybe layers on vector search, graph context, reranking, and a chat interface. However it is the stack assembles data, the system hands back information, and declares victory.

An important part of our discovery loop is that the system proposes the next move without pretending it owns the investigation. The system helps bound the next action, surface the most promising branch, and preserve what happened last time, but the user still steers.

This way, the system is strong where machines are strong: constraining search spaces, preserving lineage, checking coverage, remembering prior work, and producing bounded plans. Users remain strong where humans are strong: deciding whether the next move is actually the right move, recognizing when a branch is semantically off, changing the question, and judging what matters.

For most analyses, "finding something" is rarely the hard part of working across large datasets. What's tougher is deciding what to do next without exploding the search space, wasting compute, or drifting into arbitrary exploration.

In Exeges, search results aren't (just) answers. They're entry points into the next move: compare these versions, inspect these changed sections, test this correlation on this cohort, widen this neighborhood, narrow that taxonomy, follow this chain.
