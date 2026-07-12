---
title: "Architecture"
---

Exeges is a multi-layered platform that turns complex, evolving sources into durable, queryable, evidence-backed knowledge. This page is the machinery behind the claims on the rest of the site — the reason work in Exeges compounds, replays, and holds up under audit. It's built in Python and Rust.

## The evidence foundation

**Durable Artifact Plane**
The source-of-truth layer: deterministic identities, reproducible artifacts, manifest-based publishing, and stable contracts for downstream systems. Everything above this layer is a rebuildable projection of it — which is what makes replay and audit possible rather than aspirational.

**Annotation Substrate**
Stand-off semantics on stable document coordinates: canonical annotation bundles and deterministic resolution keep human and machine judgments anchored to the exact spans that support them, durably and across versions. This is the substrate that lets knowledge work compound. We wrote about it [here](/posts/the-annotation-substrate/).

## Understanding the sources

**Multimodal Ingestion**
Turns raw sources — documents, datasets, HTML, XML, media — into durable, versioned artifacts. The front door of the platform and the first link in the evidence chain: provenance is preserved from the first step of processing.

**Document & Media Parsing**
Preserves structure, hierarchy, and evidence fidelity across PDFs, HTML, XML, and media transcripts. Rather than flattening everything into undifferentiated chunks, it retains the internal form of source material so downstream systems can reason over real structure.

**Structured Data Engine**
Transforms structured data into governed analytical surfaces that can be normalized across sources, compared over time, and projected into reusable states and relationships. In testing, the engine has processed millions of rows without strain — so far, the limit has been how much data we could feed it, not how fast it processes.

**Enrichment & Knowledge Derivation**
Combines machine enrichment with analyst-authored semantic layering: observations, states, arcs, and annotations derived from source artifacts, with human validation and curation as first-class knowledge surfaces.

## Acting on the evidence

**Search & Retrieval Stack**
Query understanding, hybrid retrieval, graph context expansion, and answer generation — a multi-stage retrieval system for evidence-backed exploration, not a thin keyword layer. Some notes [here](/posts/search-discovery-loop/).

**Graph Projection & Runtime**
Projects durable artifacts into navigable runtime surfaces — graph, search index, and vector representations — through staged, rebuildable projection. On why the graph is a projection and not the source of truth: [Graph Projection without Graph Worship](/posts/graph-projection-without-worship/).

**Exploration & Discovery Loop**
Graph-in-the-loop discovery through bounded planning and iterative computation. Candidate sets, checkpoints, and guided loops move from raw information to high-signal analytical paths without brute force.

**Control Plane & Orchestration**
Coordinates jobs, manages specifications, tracks execution, and governs change workflows — the layer that keeps the system reproducible, observable, and operational at scale.
