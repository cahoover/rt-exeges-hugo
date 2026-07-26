---
author: "Christopher Hoover"
title: "Exeges: The Annotation Substrate"
date: "2026-07-23"
tags:
- Exeges
- parsing
- architecture
---

An annotation in Exeges is a coordinate, not a comment. The way latitude and longitude anchor a point to the map, an annotation anchors a piece of judgment — *this section was amended, this figure is a reporting artifact, this provision is ambiguous* — to the exact passage it describes.

TL;DR: The value of working through dense material — legislation, filings, contracts — isn't in the raw text; it's in the judgments formed while reading it, and most software either throws those judgments away or files them in some separate store where the source can't defend them. Exeges records every judgment as a durable annotation anchored to the corpus, addressable, with an identity and lifecycle of its own. Done consistently, at corpus scale, the annotation layer becomes something you can navigate, query, and audit — a record of what your organization knows, attached to the evidence for it.

## A coordinate system for documents

When a document enters Exeges, parsing gives every element a stable address — sections, paragraphs, sentences, table cells. An annotation is a durable, addressable record that points at one of those addresses. It survives re-rendering, re-indexing, and every change in how the document is displayed.

Because annotations are addressable, they can point at each other. A finding can cite another finding as evidence. A newer conclusion can supersede an older one — which stays in the record, retracted but replayable.

## Targets and evidence play different roles

An analyst marks a statutory provision as ambiguous. The provision is the **target**. The justification might be a conflicting committee report, a related amendment, and an older analyst note that argued the opposite — those are **evidence**, and each plays a different role in the judgment. The substrate keeps those roles distinct.

That distinction is what makes the layer queryable. Show every provision marked ambiguous. List the findings that rely on this committee report. Surface where analysts disagree. Track what shifted after a particular amendment. Each of those is a query over roles, and none of them is possible if judgment is stored as free-text notes.

## Three kinds of authors, one layer

**Deterministic passes flag whatever you need flagged** — every citation, every mention of a name, every dollar figure — anything mechanically identifiable, annotated across the whole corpus at once.

**AI agents file claims, and every claim must survive verification.** An agent's finding is checked against the source excerpt it cites before it can enter the record. Quote text that isn't there, and the whole write is rejected.

**People adjudicate and extend.** Analysts write notes with typed stances — support, dispute, question, validate — anchored like everything else, including to other annotations. Disagreement isn't a comment thread; it's part of the record, and it's queryable like everything else.

Three author classes, three verification disciplines, one anchored layer.

## What a seeded corpus unlocks

Annotations compound. Ask for *every section that adds an amendment and rescinds funding*, and the answer is a proven set, not a relevance ranking: which conditions matched, how many sections, how many occurrences. Start at a clause and traverse to everything that depends on it. Start from an anomaly and walk back to the governing language. Trace how a conclusion strengthened, weakened, or got overturned as new versions arrived — every step of the chain anchored to the text that proves it.

## Structured data, same substrate

The idea doesn't stop at documents. Quantitative observations — measures, time series, analytic checkpoints — take annotations the same way: *this spike is a reporting artifact; this correlation stops holding after the 2019 rule change*. A single annotation can span modalities: this statistical trend (structured target) is explained by this clause (document evidence) and contradicted by this prior finding (another annotation). One coordinate system, whatever the material.

## Why it matters

A judgment stored as a chat transcript or a margin note evaporates or drifts away from its source. A judgment stored as a durable annotation stays attached to the passage that justifies it, keeps its history when it's challenged or superseded, and remains answerable — years later — to the question every auditor eventually asks: *how did you know that?*
