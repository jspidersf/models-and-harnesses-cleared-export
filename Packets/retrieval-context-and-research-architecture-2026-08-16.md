# Research Packet: Retrieval, Context, and Research Architecture

- **Template version:** 2026-08-05
- **Status:** CLEARED FOR PUBLIC DISCLOSURE
- **Direction:** personal → work
- **Clearance date:** 2026-08-16
- **Cleared by:** Jeremy Pollock
- **Research period covered:** 2026-07-15 through 2026-08-04
- **Last verified:** 2026-08-05
- **Originating private repository or repositories:** `jspidersf/models-and-harnesses`
- **Safe source paths:** `research/cerebras-knowledge-base-2026-07-16.md`; `research/jeff-dean-inference-systems-ccsf-relevance-2026-08-04.md`; `research/quesma-deep-research-pipeline-2026-07-20.md`
- **Source commits:** `22d694703714bde8a2767178372e5c6712f65bf8`
- **Intended destination repository or repositories:** `jp-sfgov/sfgov-models-and-harnesses`; `jp-sfgov/sfgov-ccsf-compute`
- **Destination canonical document roles:** retrieval and context architecture; research workflow method; future governed-workflow pilot evidence
- **Transfer form:** graduated document
- **Baseline content identity:** not applicable
- **Expected result identity:** not applicable

## Purpose and context

This packet transfers the reusable public-source research on hybrid retrieval, canonical versus derived state, context preservation, staged deep research, and the relationship between inference systems and governed workflows. Its purpose is to let the work side reuse the architecture and method conclusions without reconstructing three token-intensive source reviews.

The conclusion is a bounded pattern, not an implementation decision: leave authoritative information in source-native systems; build rebuildable, policy-scoped derived retrieval; separate discovery from verification; expand context only for ranked evidence; preserve provenance and corrections; and evaluate the complete model–retrieval–tool–workflow system.

## Research scope and method

The analysis used a first-party Cerebras engineering account of a production knowledge base, a public Jeff Dean interview with timestamped source claims, and a Quesma practitioner account of a custom deep-research pipeline. Claims were separated into source facts, architectural inference, and recommendations. Vendor/operator scale and cost claims were not treated as independent performance proof.

## Findings

### 1. Hybrid retrieval should operate over source-native canonical systems

**First-party fact:** Cerebras described a deployed knowledge system that leaves information in collaboration, code, ticketing, document, and specialist systems while maintaining a common derived search representation. It combines exact lexical retrieval, embeddings, rarity weighting, recency, independent ranked lists, reciprocal rank fusion, reranking, late context restoration, and narrow retrieval tools.

**Analysis, high confidence:** the transferable value is composition, not a specific database. Exact search protects identifiers, error strings, citations, and names. Semantic search handles paraphrase. Independent ranks preserve inspectability. Cheap deterministic fusion should precede costly model reranking. Neighboring context should be restored after ranking rather than attached to every candidate.

**Recommendation:** keep source systems and destination canonical files authoritative. Treat summaries, chunks, vectors, caches, and rank outputs as rebuildable derived state. A search result can orient an agent; it does not create authority, disclosure permission, or current factual state.

### 2. Normalize for matching while preserving a recovery path to omitted detail

Cerebras distilled threads into likely questions, summaries, resolutions, and named systems, while also embedding selected message “bursts.” This addresses a real tradeoff: normalized summaries improve matching but can omit decisive tangents or constraints.

**Recommendation:** pair any normalized representation with smaller high-signal units and a link to the canonical source/version. Restore bounded surrounding context only for selected results. Corrected or superseded claims should remain searchable for provenance, but the current statement should rank first and carry the older statement as history.

### 3. Scope and authorization must precede retrieval

**Inference for organizational use, high confidence:** a final answer filter is not an authorization system. If filtering occurs after search, forbidden content may already have reached embeddings, rerankers, model context, logs, or caches.

The required order is:

1. authorize identity, purpose, project/department, and data class;
2. expose only permitted source/tool descriptions to the planner;
3. search only the authorized slice;
4. preserve policy/classification and canonical identity in every derived object;
5. fuse, diversify, and rerank permitted candidates;
6. restore permitted context;
7. synthesize with citations; and
8. propagate source correction, deletion, access change, retention, and legal-hold effects to all derived representations.

Separate physical stores or strongly isolated namespaces and credentials are appropriate for materially different trust zones. Shared schemas and retrieval code do not imply a shared corpus.

### 4. Thin evidence-returning tools preserve orchestration visibility

**Analysis:** lexical search, semantic search, scoped source retrieval, exact file retrieval, and expertise/source discovery are better exposed as narrow tools than hidden behind multiple autonomous answer services. The client can see the evidence, choose tools, enforce budgets, and cite authoritative sources. This reduces the risk of an opaque second agent loop and preserves client choice.

### 5. Retrieval quality and authorization leakage are separate evaluation dimensions

Before optimizing answer quality, test stable canonical identity, idempotent writes, policy inheritance, revocation fan-out, citation integrity, source-specific temporal semantics, and deterministic observability. A model or reranker upgrade requires an index/version migration and reproducibility plan.

The Cerebras source did not publish retrieval accuracy, answer baseline, latency, cost, model choices, authorization propagation, event-ordering, or index migration detail. Its reported usage supports production relevance but does not establish accuracy, security, or economics.

### 6. Inference is a system property, not a model-only property

**Source claim from the Jeff Dean interview:** model utility depends on retrieval, tools, context, skills, evaluation, serving, and data movement; long-running agents can degrade off-distribution; multiple branches can improve search at added cost; clear specifications and fast evaluators change what can be automated; shared abstractions can move reliability beneath application logic.

**Work-side inference:** compare workflow configurations, not just models. Useful baselines may hold the model constant while adding or removing governed retrieval, skills, tools, and evaluation, then compare approved local/hosted models where policy permits. Measure total inference across branches, retries, fallbacks, and failed paths.

The interview does not validate municipal capacity, topology, hardware, economics, sovereignty percentages, legal compatibility, or authorization. It supports pilot sequencing and telemetry design only.

### 7. Deep research benefits from staged admission rather than open-ended fan-out

**Practitioner evidence, moderate confidence:** the Quesma account describes a staged workflow in which inexpensive workers discover candidates, a different role verifies sources and numbers, a stronger model plans or resolves disputes, tool execution supplies observable evidence, and synthesis operates on a bounded vetted set.

**Recommendation:** separate claims, sources, and entities/projects. Rejecting a weak claim should not erase a useful source or project. Track claim disposition as accepted, rejected, uncertain, or superseded. Prefer directly inspected or executed evidence over model consensus when the claim bears a decision.

Independence between agents can reduce self-confirmation but does not eliminate correlated errors from shared prompts, memory, sources, or training. Human review remains proportionate to stakes.

### 8. Token savings must be measured per accepted decision-changing claim

The Quesma author's reported endurance improvement was uncontrolled across subscriptions, tasks, models, and roles. “No marginal bill” omits subscriptions, coordination, latency, duplicate work, human review, and security exposure.

**Recommendation:** for large research runs, record model/effort, fan-out, stop condition, accepted/rejected claim counts, tool use, tokens/cost, and review burden. The useful denominator is cost per accepted decision-changing claim. Routine ingestion should remain lightweight; independent verification and fan-out should be reserved for claims whose expected error cost justifies them.

## Technical detail

A minimal retrieval pipeline is:

```text
authorized scope
  → parallel lexical, semantic, and domain-specific search
  → reciprocal-rank fusion
  → canonical-source deduplication and source diversity cap
  → small reranked candidate set
  → authorized neighboring-context restoration
  → cited synthesis
```

Recommended invariants:

- every derived object resolves to one canonical source and source version;
- reprocessing the same version is idempotent;
- derived content inherits the source's policy and classification;
- source deletion, access change, correction, or supersession invalidates every downstream copy and cache;
- citations point to authoritative sources, not merely summary rows;
- recency rules differ by source type and never silently weaken still-binding policy;
- the system can show which retrievers returned a source and why it survived;
- source scope applies to search, reranking inputs, context expansion, synthesis, logs, and caches.

A smallest-sufficient pilot would use one bounded read-only Level 1–2 or otherwise low-risk corpus, a named owner, fixed question set, explicit authorization scope, direct lexical baseline, hybrid retrieval candidate, citation/omission tests, authorization-leakage tests, review-burden measurement, and a stop decision. This packet does not authorize that pilot.

## Public sources

| Source title | Publisher or author | Publication date | URL and useful locator | Claim or finding supported | Verified date |
|---|---|---|---|---|---|
| How We Built Our Knowledge Base | Cerebras | 2026-07-15 | https://www.cerebras.ai/blog/how-we-built-our-knowledge-base | Production hybrid-retrieval architecture | 2026-07-18 |
| Cerebras article announcement | Cerebras | 2026-07-16 | https://x.com/cerebras/status/2077822555159945507 | Authorship and reported production use | 2026-07-18 |
| Jeff Dean: The #1 Rule for Building in AI | Y Combinator | 2026 | https://www.youtube.com/watch?v=CxXgV54KzpQ | Timestamped source for system, evaluation, and inference observations | 2026-08-04 |
| Performance Hints | Abseil / Google | live | https://abseil.io/fast/hints.html | Example of reusable expert performance guidance | 2026-08-04 |
| I burned all my tokens researching how to save tokens | Quesma / Bartosz Kotrys | 2026-07-17 | https://quesma.com/blog/custom-deep-research-pipeline/ | Practitioner staged research workflow | 2026-07-20 |
| Claw-SWE-Bench | Research authors | 2026 | https://arxiv.org/abs/2606.12344 | Harness effects and limits of bare-adapter comparisons | 2026-07-20 |
| Terminal-Bench 2.0 | Research authors | 2026 | https://arxiv.org/abs/2601.11868 | Model/scaffold interaction and cost variation | 2026-07-20 |
| Prompt caching with tools | Anthropic | live | https://platform.claude.com/docs/en/agents-and-tools/tool-use/tool-use-with-prompt-caching | Tool-definition changes invalidate cached prefixes | 2026-07-20 |

## Alternatives and conflicting evidence

- A knowledge graph can add value for explicit relationships, but the Cerebras example shows that hybrid search, scope, reranking, and source metadata can work without one. Graph extraction should follow measured relationship-query demand.
- A unified physical index is operationally simple inside one authority domain; separated stores or namespaces better contain materially different trust zones. Reuse schemas/code while keeping visibility separate.
- Summary-only retrieval is compact but lossy; raw-only retrieval preserves detail but matches and ranks poorly. Pair normalized records with recoverable detail.
- Multi-agent research can add discovery and cross-checking, but a capable single-agent plus human review is the cheaper baseline and may be sufficient.
- Fine-tuning or distillation may help a stable, high-volume residual gap, but retrieval, tools, specifications, and evaluation should be tested first.

## Caveats and unresolved questions

- No local retrieval implementation or work-side outcome comparison is included.
- Cerebras supplied no public accuracy, security, cost, or migration evaluation.
- The interview and practitioner article are not public-sector evidence.
- Authorization, retention, deletion, legal holds, records, accessibility, and audit require destination-native design.
- Shared memory and cross-harness orchestration remain unproven and can create provenance, poisoning, privacy, and concurrency risk.

## Corrections and freshness triggers

Reverify when source access, policy, classification, retention, connector behavior, embedding/reranker models, index schema, tool contracts, or target harness caching behavior changes. A new corpus, department, trust zone, or side-effect authority requires a fresh scope and leakage evaluation. Corrected or superseded source material must trigger derived-state invalidation and reranking.

## Integration guidance

Route hybrid retrieval and canonical/derived-state principles to the work-side retrieval/context authority. Route staged research and claim admission to the research-method authority. Route the inference-system observations to future workflow-pilot telemetry, clearly labeled as candidate implications. Do not create an enterprise-wide index, shared memory layer, cross-harness orchestrator, or fine-tuning program from this packet.

## Exclusions and disclosure boundary

Excluded: private corpus contents and names; local repositories, devices, accounts, model routes, and implementation state; raw intake and session transcripts; personal or City records; any cross-domain corpus mapping; uncontrolled token logs; and any claim that a work-side or CCSF retrieval pilot, architecture, vendor, or data integration is approved.

## Closeout

- **Public export commit:**
- **Destination content commit or commits:**
- **Ledger or manifest commit:**
- **Unresolved differences:** Destination-native authorization, records, architecture, and pilot decisions remain unreviewed.

## Completion checklist

- [ ] The receiving agent can understand, verify, and integrate the cleared research without access to the originating private files.
- [ ] All eligible substantive detail, links, context, reasoning, caveats, corrections, and provenance were preserved.
- [ ] Facts, analysis, inference, and recommendations are distinguishable.
- [ ] Every decisive claim is traceable to a public source or explicitly identified reasoning.
- [ ] Raw intake and private, restricted, or otherwise ineligible context were excluded.
- [ ] Safe source and destination commits are recorded.
- [ ] Jeremy reviewed the exact public diff and affirmatively cleared it for public disclosure.
