---
author: "Christopher Hoover"
title: "Exeges: The Annotation Substrate"
date: "2026-03-19"
tags:
- Exeges
- parsing
- architecture
---

Most ‌people ‌hear ‌“annotation” and picture a sticky note, a little comment bubble hanging off the margin. Extra metadata you tack on afterward. The kind of feature a team adds in Sprint 14 because a customer asked for “collaboration.”

We don’t treat it that way. When someone is working through dense material, legislation, regulatory filings, contracts, or even messy quantitative observations, the real value rarely sits in the raw source. It sits in the judgment and connections formed while reading it. How one amendment quietly collides with another. Whether a revised sentence is an actual policy shift or just cleanup. Why a sudden spike in a series is probably a reporting quirk, not the world changing overnight.

## The annotation substrate
Substrate (noun): the base something lives on.

At Exeges, we’ve been building what we call an annotation substrate, a durable layer where human and (human-verified) machine judgments are treated as first-class objects. They have an identity. They have history. They have a lifecycle. This isn’t “notes on top of content,” it’s infrastructure that makes judgment sturdy enough to become part of system behavior.

For example: an analyst marks a statutory provision as ambiguous. The provision is the target. The justification might be a conflicting committee report, a related amendment, and an older analyst note that argued the opposite. Those aren’t the same kind of thing. They play different roles, so the system should represent them differently.

If you squash all of that into a single “comment on this highlighted span,” you lose what makes annotations searchable, composable, and reusable.

Durable annotations enable another navigation surface across the corpus, such as: show every provision marked as ambiguous; list findings that rely on this committee report; surface where analysts disagree; track what shifted after a particular amendment; pull every quantitative observation linked to this clause.

## What about structured data?
The same idea extends to structured data.

We work with quantitative observations next to legal text, measures, time series, outcomes, analytic checkpoints, and so on. Analysts need to annotate those too: “This spike is a reporting artifact.” “This correlation stops holding after the 2019 rule change.” “This measure isn’t comparable after the statutory revision.”

That means a single annotation can say: This statistical trend (structured target) -> is explained by this clause (document evidence) -> and contradicted by this prior finding (another structured target).

## Compounding impact
Annotations made over time (e.g. by a team) have compounding value for the exploration of a large corpus. You can start at a clause and jump to the metrics it might influence. Or begin with an anomaly in the numbers and move back to the governing language. You can trace where an earlier conclusion gets strengthened, weakened, or overturned as versions shift and sources change. You can disagree with annotations and track disagreements. 

## Still early, but the direction is clear
It’s early. The structured targeting layer still needs resolver APIs, selector schemas, and firmer calls around versioning. Plenty remains to be nailed down.

But the path is straightforward: one substrate across modalities, durable coordinates rather than brittle offsets, explicit evidence rather than collapsed comments, and judgment you can reuse.