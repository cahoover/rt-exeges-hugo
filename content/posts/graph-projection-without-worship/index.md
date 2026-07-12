---
author: "Christopher Hoover"
title: "Graph Projection without Graph Worship"
date: "2026-04-03"
tags:
- Exeges
- exploration
- architecture
---

(Being what I hope is a catchier title than "Why we stopped treating the graph as the center of the system.")

When we began building Exeges, the graph was seductive because it was the most visible, queryable, integrated surface. It looks like the place where everything should live. The first iterations of the platform used the graph as the source of truth and the center of gravity. More or less everything revolved around it. I even subscribed to Neo4J marketing emails. 

But we discovered that the graph as center of gravity was pulling too many responsibilities into itself:

- truth storage
- orchestration assumptions
- retrieval semantics
- lineage
- application state
- product meaning
- and on
- and on

That actually felt kind of elegant at first. Then it started to chafe, because too many concerns were getting entangled.

Projection logic started bleeding into truth. Storage decisions started shaping product behavior. Retrieval behavior became harder to separate from graph layout. Debugging got harder, because we couldn't tell if a problem lived in the source artifacts, the projection pipeline, the graph model, or the consuming service. Replay became harder.

Graphs are genuinely great, but they are so expressive that it's easy to overreach. Because they can represent almost anything, it's easy to let them absorb responsibilities that should have remained distinct.

We began to struggle with heisenbugs, and it felt like everything was getting harder. (An aside: this was my introduction to the concept of "heisenbugs." They're awful, but what a clever name, huh?)

After beating our heads against a wall for too long, we were forced to step back and reconsider the role of the graph in our platform. We decided the answer was that the graph is not a canonical store; it is a projection.

The graph is an excellent planning surface, exploration surface, and a derived integration surface. It is great at helping traverse structure, discover relationships, and bound useful work. It is great at making meaning navigable. But for us it's not where truth should live, and it is not where every contract in the system should collapse together.

Once we accepted that, which was surprisingly painful and anxiety-provoking, the architecture got cleaner. [Cue major-key background music]. We moved truth into durable artifacts and producer-owned contracts, and ensured the graph could be rebuilt from those artifacts (without using GraphAR, which was also painful, but we got a lot more flexibility). Projection became something we could replay, inspect, and change without fear of mutating the meaning of the whole system. 

I don't want to treat our journey as some sort of groundbreaking insight, but things did get easier. Services became easier to reason about because producer and consumer boundaries were sharper. Debugging was more straightforward because we could ask simpler questions: was the source wrong, the contract wrong, the projection wrong, or the read model wrong? (Sometimes the answer to that is "yes").

Net: The graph is no longer the center of the system; it is one member of set of lenses over the system. 