---
title: "Architecture"
---
Exeges turns complex, evolving sources into durable, auditable, queryable, evidence-backed knowledge.

## The evidence foundation

**Data Mapping**
A matrix similar to latitude and longitude is created and applied to every data source, creating stable coordinates. Human and machine judgments are anchored to the spans that support them, durably and across versions. We wrote about this feature [here](/posts/the-annotation-substrate/).

**Durable Artifacts & Manifests**
Every AI analysis resolves to the original sources that informed it: the document, an annotation over it, and a manifest recording what produced both. An answer given last year replays against the record it was drawn from, not reconstructed from a log of what the system did.

## Understanding the sources

**Multimodal Ingestion**
Turns any kind of source data, including documents, datasets, HTML, XML, and media, into versioned artifacts. The front door of the platform and the first link in the evidence chain.

**Enrichment & Knowledge Derivation**
Combines machine enrichment with analyst-authored semantic layering: observations, states, transitions, derived from source artifacts, with human validation and curation as first-class knowledge surfaces.

## Analysis on arrival

**Change Detection**
A new version is aligned to the last one section by section, and every difference is written as an annotation on the sections it touches, carrying a continuity handle that survives renumbering and restructuring. Change becomes evidence like any other — anchored, queryable, replayable.

**Verification & Adjudication**
Agent citations must resolve to the source at the anchor it claims, or the write is rejected outright. Analysis is provisional and is sent to the person accountable for the result, who accepts, disputes, or supersedes it. Disputes and supersessions are annotations in their own right, so a retracted finding stays replayable.

**Findings as Events**
An accepted finding is durably stored, and filing one is something the system can react to: raise the section for the analyst who owns it, or put the next investigation to work. Because the finding lives on the corpus rather than in a session, the next reader — human or agent — starts from what has already been established.

## Retrieval and operation

**Search & Retrieval Stack**
A multi-stage retrieval system for evidence-backed exploration.

**Exploration & Discovery**
Graph-in-the-loop discovery through bounded planning and iterative computation. Candidate sets, checkpoints, and guided loops move from raw information to high-signal analytical paths without brute force.

**Agent Access (MCP)**
Agents work the corpus through a set of MCP tools: survey a corpus, read a document, search it, inspect a diff, list annotations, file one. Agents read their own coverage too — what has been examined, what was skimmed, what remains untouched — so a session builds on prior work instead of starting over.

**Control Plane & Orchestration**
Coordinates jobs, manages specifications, tracks execution, and governs change workflows — the layer that keeps the system reproducible, observable, and operational at scale.
