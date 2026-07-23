---
title: "Architecture"
---

Exeges turns complex, evolving sources into durable, auditable, queryable, evidence-backed knowledge.

## The evidence foundation

**Durable Artifact Plane**
The source-of-truth layer: deterministic identities, reproducible artifacts, manifest-based publishing, and stable contracts for downstream systems. Everything above this layer is a rebuildable projection, supporting both exploration and retention.

**Annotation Substrate**
Stand-off semantics on stable document coordinates: annotation bundles and deterministic resolution keep human and machine judgments anchored to the spans that support them, durably and across versions. This is the substrate that lets knowledge work compound. We wrote about it [here](/posts/the-annotation-substrate/).

## Understanding the sources

**Multimodal Ingestion**
Turns any kind of source data, including documents, datasets, HTML, XML, and media, into durable, versioned artifacts. The front door of the platform and the first link in the evidence chain.

**Document & Media Parsing**
Preserves structure, hierarchy, and evidence fidelity across PDFs, HTML, XML, and media transcripts. Rather than flattening everything into undifferentiated chunks, it retains the internal form of source material so downstream systems can reason over original structure.

**Enrichment & Knowledge Derivation**
Combines machine enrichment with analyst-authored semantic layering: observations, states, transitions, derived from source artifacts, with human validation and curation as first-class knowledge surfaces.

## Information retrieval

**Search & Retrieval Stack**
Query understanding, hybrid retrieval, graph context expansion, and answer generation — a multi-stage retrieval system for evidence-backed exploration, not a thin keyword layer. Some notes [here](/posts/search-discovery-loop/).

**Projection & Runtime**
Projects durable artifacts into navigable runtime surfaces — graph, search index, and vector representations — through staged, rebuildable projection.

**Exploration & Discovery Loop**
Graph-in-the-loop discovery through bounded planning and iterative computation. Candidate sets, checkpoints, and guided loops move from raw information to high-signal analytical paths without brute force.

**Control Plane & Orchestration**
Coordinates jobs, manages specifications, tracks execution, and governs change workflows — the layer that keeps the system reproducible, observable, and operational at scale.
