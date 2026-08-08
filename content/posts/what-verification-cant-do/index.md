---
author: "Christopher Hoover"
title: "Exeges: What Verification Can't Do"
date: "2026-08-07"
tags:
- Exeges
- judgment
- architecture
---

A citation can be perfect and the conclusion built on it wrong. Exeges verifies citations. It does not (cannot) verify analysis. 

TL;DR: [The gate](/posts/the-verification-gate/) proves the cited words exist at the cited address and were in hand when the claim was written. It cannot prove the words *support* the conclusion. Nothing can — analysis has never been verifiable, for machines or for people. What professions demanded instead, for as long as analysis has existed, is accountability: attributed, reviewed, contestable, correctable. Exeges is that structure, at machine scale. 

## A structure for accoundability

Any analysis, human or agent, can reach a conclusion that turns out to be wrong. To mitigate that risk requires structure around the fallibility: you need to know who (or what) concluded it, what they looked at, who reviewed it, and that there is a process for challenging it and a record of the challenge. Trust is earned through accountability.

## Fallible by design

Exeges delivers the machinery to manage accountability for both human and agent analysis: supersession, typed dissent, confidence fields, [two clocks](/posts/when-the-ground-moves/). 

A record's promise is not *the conclusions are correct.* The promise is: that when a conclusion is wrong, that fact has somewhere to land. A challenger files a dispute, anchored to the same words (because of the citiation the gate, provably the *same* words). A correction supersedes, and the record keeps the arc: what was believed, on what evidence, for how long, and what replaced it.

Being wrong on the record is recoverable. Being wrong in a chat log is just gone.

## Flags, not determinations

To further reduce risk of mis-analysis, the workhorse judgment in the change loop is narrow: *does this edit materially touch this determination?* A new version arrives, [the join](/posts/when-the-ground-moves/) surfaces every conclusion sitting on moved ground, and the agent's job is triage — wave a flag at the changes that look like they matter.

The agent waves the flag. A person makes the determination. The record proves who did which, for every flag and every determination, permanently. That division isn't a disclaimer; it's the design. Is the AI making the call? No. The call is made where it always was. What changed is that no change arrives unexamined

## The error structure is chosen

A screening judgment can be wrong in two ways: a false positive or a false negative. The former is an immaterial change, and a reviewer spends minutes dismissing it. 

A false engative is a silent failure with material consequences. So the screener is calibrated toward the cheap failure — over-flagging. Regulated industries already run on transaction monitoring and adverse-event triage. Imperfect classifiers, required by regulators, and trusted because the process around them is auditable even though the classifier isn't.

In Exeges every change is durable data and every determination is anchored, so *all* the changes that arrived this quarter are a list. The flagged ones are a subset. The unflagged remainder is the only place a miss can hide, and is itself a query result. For most existing systems, a missed change is an unknown unknown.

## Calibration is measured

Conservative calibration has its own failure mode: cry wolf. Flag everything and reviewers stop reading flags. So conservative is the starting point, and every flag lands in the record as a typed, anchored judgment, just as [every other stance does](/posts/the-annotation-substrate/). What accumulates is labeled history pinned to exact text that says "this change, this flag, this ruling." That delivers the raw material for measuring the screener and tuning it within the same auditable record it serves.


