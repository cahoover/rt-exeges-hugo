---
author: "Christopher Hoover"
title: "Exeges: The Grid"
date: "2026-07-23"
tags:
- Exeges
- parsing
- architecture
---

A reference in Exeges cites a specific point of a specific version of a document or dataset, the way latitude and longitude anchor a point to the map — *this section was amended, this figure is a reporting artifact, this provision is ambiguous*.

TL;DR: Working through dense material — legislation, filings, contracts — creates a growing and searchable store of references anchored to the source, addressable, with an identity and lifecycle of its own. References compound and become something you can navigate, query, and audit. A record of what your organization knew, what it decided, and why, all attached to the supporting evidence.

## A coordinate system for documents

When a document enters Exeges, every element is given a stable address. Sections, paragraphs, sentences, and table cells can all be cited. A reference is a durable, addressable record that points to one of those addresses. It survives re-rendering, re-indexing, and every change in how the document is displayed.

Because references are addressable, they can cite each other. A newer conclusion can supersede older ones, which stay in the record, retracted but replayable.

## Targets and evidence play different roles

An analyst marks a statutory provision as ambiguous. The provision is the **target**. The justification might be a conflicting committee report, a related amendment, and an older analyst note that argued the opposite — those are the **evidence record**, and each plays a different role in the judgment. Exeges keeps those roles distinct.

That distinction is what makes references queryable. 
*  Show every provision marked ambiguous. 
* List the findings that rely on this committee report. 
* Surface where analysts disagree. 
* Track what shifted after a particular amendment. 

Each of those is a query over roles.

## Three kinds of authors, one layer

**Deterministic passes flag whatever you need flagged** — every citation, every mention of a name, every dollar figure — anything mechanically identifiable, annotated across the whole corpus at once.

**AI agents file claims, and every claim must survive verification.** An agent's finding is checked against the source excerpt it cites before it can enter the record. Quote text that isn't there, and the whole write is rejected.

**People adjudicate and extend.** Analysts write notes with typed stances — support, dispute, question, validate — anchored like everything else, including to other annotations. Disagreement isn't a comment thread; it's part of the record, and it's queryable like everything else.

Three author classes, three verification disciplines, one anchored layer.

## Compounding value

Ask for *every section that adds an amendment and rescinds funding*, and the answer is a filtered set: which conditions matched, how many sections, how many occurrences. Start at a clause and traverse to everything that depends on it. Start from an anomaly and walk back to the governing language. Trace how a conclusion strengthened, weakened, or got overturned as new versions arrived — every step of the chain anchored to the text that proves it.

## Structured data, same substrate

Quantitative observations — measures, time series, analytic checkpoints — take references the same way: *this spike is a reporting artifact; this correlation stops holding after the 2019 rule change*. A single reference can span modalities: this statistical trend (structured target) is explained by this clause (document evidence) and contradicted by this prior finding (another reference). 

## Why it matters

A judgment stored as a chat transcript or a margin note evaporates or drifts away from its source. A judgment stored as a durable annotation stays attached to the passage that justifies it, keeps its history when it's challenged or superseded, and remains answerable years later to the question every auditor eventually asks: *how did you know that?*
