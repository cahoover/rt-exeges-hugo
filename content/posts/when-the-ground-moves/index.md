---
author: "Christopher Hoover"
title: "Exeges: When a New Version Arrives"
date: "2026-08-03"
tags:
- Exeges
- versioning
- architecture
---

A stale answer looks exactly like a fresh one. The citation still resolves, the prose is still confident, the verification still passes — because the claim really was true against the version it cites. Nothing about the answer changed. The world underneath it did. In most systems that failure is silent, and you learn about it from a client, an examiner, or a competitor. Exeges is built to make it loud.

TL;DR: The previous posts described a record where every judgment is [anchored to an exact version of its source](/posts/the-annotation-substrate/) and [verified against the bytes at write time](/posts/the-verification-gate/). This post is about what those two properties buy together. When a document changes, Exeges computes the change as durable, addressable data. Every claim carries the address it stands on, and "which of our conclusions did this amendment touch?" becomes a query answered with the edit attached. Staleness becomes a signal that arrives with the new version.

## Two clocks

Every claim in Exeges carries two timestamps that most systems collapse into one. The first is the *corpus clock*: which version of the source this claim is about. The second is the *belief clock*: when the claim was made, and whether anything has superseded it since. Keeping them separate is what makes staleness a precise idea instead of a vague worry. "What did the text say in March?" and "what did we believe in March?" are different questions, and the interesting one — *did our belief survive what happened to the text?* — is their join.

The verification gate settles claims against the corpus clock, permanently: a claim verified against a version stays verifiable against it forever. What the gate deliberately does not promise is that the version stays the ground. 

## Versions accumulate

When a revised document arrives — an amended statute, updated guidance, a restated filing — Exeges parses it into a new version that sits beside the old one. Nothing is overwritten. The old version keeps its addresses, its text, and every claim anchored to it, all still verifiable.

This sounds like archival hygiene. It is actually the precondition for noticing movement at all. A system that replaces old text with new text has destroyed one side of the comparison: it can tell you what the document says, but not what changed, and it certainly can't tell you what your conclusions were standing on when it changed.

## Change is computed, not noticed

With both versions durable, Exeges computes the difference between them as data: which sections changed, what the edits were, and — the part that matters more than it sounds — *continuity*. A section that moved or was renumbered keeps its identity thread across versions, so "same provision, new address" and "genuinely new text" are distinguishable, mechanically. The diff isn't a visual compare someone runs by hand; it's a durable artifact with addresses, queryable like everything else in the record.

## The join

Here's where the two halves meet. Every claim carries its pin: version, section, exact span. Every diff carries addresses: these sections changed, in these ways. Which claims sit on moved ground is the intersection. 

The record reports as *matched* or *the document has moved on*, with the current version named. What it never does is silently re-attach your conclusion to whatever text is there now. 

Exeges flags the claim for re-examination. A or an agent reads the new version and either re-files the conclusion or supersedes it. Supersession is append-only, so the record keeps the whole arc: what was believed, against which version, for how long, and what replaced it. Conclusions strengthen, weaken, and get overturned in the open.

## Change is the point

The corpora that matter are the ones that move: legislation is amended, guidance is revised, filings are restated. Every new version re-asks the entire record one question — *is this still current?* — and the record answers with addresses and edits, not vibes.

An auditor asks: *how did you know that?* An operator asks the harder question: *and is it still true?* The first two posts answer the auditor by construction. Exeges answers the operator on arrival of every new version, for every claim in the record, with the evidence attached.
