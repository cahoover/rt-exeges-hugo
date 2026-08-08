---
author: "Christopher Hoover"
title: "Exeges: The Verification Gate"
date: "2026-07-30"
tags:
- Exeges
- verification
- architecture
---

When an AI agent files a finding in Exeges, its citation is checked and proven before the finding can enter the record. 

TL;DR: AI made document analysis at scale cheap; conclusions with confident citations, produced faster than anyone can hand-check them. When plausible answers are free, the scarce asset is a trustworthy record of them. Exeges ensures a claim enters the record only if the passage it cites actually contains the words it quotes, verified deterministically. 

## What happens at the moment of writing

A claim must carry a citation "see section 4502(b)" and a quote "section 4502(b), and here are the words I relied on." An address without a quote is refused before any checking begins. 

When an agent writes a claim, the platform automatically loads the cited version of the document, pinned by fingerprint, so it is provably the same parse the address refers to. The quote must match the passage character for character.

When the comparison succeeds, the proof is stamped into the record alongside the claim: the version it cites, the fingerprint of the parse it verified against, the fingerprint of the exact verified span. And because a claim's identity is derived from its content, filing the same claim twice yields the same record.

## By construction, not after the fact

Most systems that talk about grounding check answers after the fact: the answer ships, an evaluation scores it, a dashboard flags the worst ones. Exeges runs the check *as* the write. There is no path into the record that bypasses the gate, so the record cannot contain an unchecked citation.

The byte comparison produces a fact: *these words are at this address in this version.* Run it today or in five years, on your infrastructure or an auditor's, and get the same verdict.

Immutability finishes the argument. Document versions in Exeges are never overwritten; a new revision lands beside the old one, so a claim verified against a version stays verifiable against it forever.

## A citation is not a guarantee of strong analysis

The comparison proves that the cited words exist at the cited address in the cited version, and that the author had those exact words in hand when the claim was written. It does not prove the words *support* the conclusion. No deterministic check can adjudicate meaning.

Support gets judged the way it always has been: by other readers. In Exeges that judgment lands in the same record: the typed stances, disputes, and supersessions described in [the annotation substrate](/posts/the-annotation-substrate/), each anchored and attributed like everything else.
