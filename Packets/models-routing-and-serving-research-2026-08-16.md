# Research Packet: Models, Routing, and Serving

- **Template version:** 2026-08-05
- **Status:** CLEARED FOR PUBLIC DISCLOSURE
- **Direction:** personal → work
- **Clearance date:** 2026-08-16
- **Cleared by:** Jeremy Pollock
- **Research period covered:** 2026-08-11 through 2026-08-12
- **Last verified:** 2026-08-12
- **Originating private repository or repositories:** `jspidersf/models-and-harnesses`
- **Safe source paths:** `research/mai-code-1-1-flash-analysis-2026-08-12.md`; `research/nvidia-nemotron-3-5-lightning-switchyard-analysis-2026-08-12.md`; relevant synthesis in `models-and-harnesses-summary.md`
- **Source commits:** `537ef52105f1c30d3f5da74dc9ba604099fa71ab`
- **Intended destination repository or repositories:** `jp-sfgov/sfgov-models-and-harnesses`; `jp-sfgov/sfgov-ccsf-compute`
- **Destination canonical document roles:** model and harness landscape; routing and serving evaluation; future municipal workload-pilot evidence base
- **Transfer form:** graduated document
- **Baseline content identity:** not applicable
- **Expected result identity:** not applicable

## Purpose and context

This packet transfers two August 2026 model-and-routing analyses that illuminate different control choices: Microsoft's closed, Copilot-native specialist model and NVIDIA's open, composable efficient model plus per-turn router. The reusable finding is that model quality, cost, and governance depend on the production harness and serving control plane. Neither release justifies an immediate route, infrastructure, or procurement change.

## Research scope and method

The review used first-party model cards, data documentation, live product documentation, model repositories, routing documentation, known-issues and security pages, and a secondary report for partner benchmark claims. It separated model facts from vendor benchmarks, unit token prices from total workflow cost, and model-only quality from harness-native production outcomes.

Live price, availability, version, context, and licensing facts were verified on 2026-08-12 and must be rechecked before use.

## Findings

### 1. MAI-Code-1.1-Flash is a harness-native managed specialist, not a general frontier or self-hosted route

**First-party fact:** Microsoft describes a closed sparse mixture-of-experts coding model with 138 billion total parameters, 5 billion active per token, a 256K context window, text/image input, English support, and availability through GitHub Copilot. The weights were not published. GitHub described hosting on Azure AI Foundry inside GitHub's tenant.

**Analysis, high confidence:** the strongest signal is the development loop. Microsoft trained and evaluated against the Copilot production harness, used product telemetry to choose improvements, and reported gains in benchmark and product measures. This is evidence for vertical integration between model, tools, repository environment, telemetry, and evaluation—not evidence that the model is generally frontier-capable.

In Microsoft's common Copilot VS Code harness, the model card reported:

| Evaluation | MAI Code 1.1 | MAI Code 1.0 | Claude Haiku 4.5 | GPT-5.4 mini |
|---|---:|---:|---:|---:|
| SWE-Bench Verified pass rate | 72.6 | 71.6 | 69.8 | 69.2 |
| Average solution tokens | 8.6K | 10.8K | 20.9K | 9.4K |
| Terminal-Bench 2.1 pass rate | 62.9 | 51.7 | 49.4 | 60.7 |
| Average solution tokens | 17.0K | 14.2K | 25.5K | 21.9K |

These are Microsoft-run, harness-specific figures. Terminal-Bench solution tokens rose while pass rate improved, showing why “25% fewer tokens” should be treated as an aggregate product claim rather than a universal task property.

The reviewed GitHub pricing listed $0.20 per million input tokens, $0.02 cached input, and $1.20 output for MAI-Code-1.1-Flash. Those rates were roughly 26.7% of the prior model's unit prices, not exactly one quarter. Unit price does not establish task cost; completion rate, token mix, retries, tool use, human correction, and product packaging also matter.

Microsoft reported improvements in “code survival” and return visits without publishing enough experimental detail to audit the effect. Treat these as promising operator evidence, not independent outcome proof.

### 2. Enterprise data treatment improves the managed-service case but does not settle authorization

**First-party fact:** the reviewed data summary said opted-in or non-opted-out consumer Copilot conversation data contributed to reinforcement-learning rollouts and an internal reward model, with specified filtering. GitHub separately said Business and Enterprise customer data was not used to train models.

**Recommendation:** evaluate the exact tenant, product surface, data-use terms, regional hosting, retention, filtering, audit, version-notice, rollback, budget, intellectual-property, accessibility, and exit controls. A no-training statement does not override local data classification, records, acceptable-use, security, labor, or procurement requirements.

### 3. Nemotron 3.5 Lightning is an efficient worker candidate, not a frontier substitute

**First-party fact:** NVIDIA released 30B-total/3B-active text-only checkpoints under OpenMDW 1.1 and published optimized BF16 and NVFP4 serving recipes. Selected configurations support very long context, but practical context depends on precision, hardware, memory, and serving configuration. Three billion active parameters does not make the system equivalent to a dense 3B deployment because full weights, cache, concurrency, and redundancy still matter.

**Analysis, high confidence:** NVIDIA's own table placed Qwen 3.6 35B A3B ahead on most broad reasoning, coding, research-agent, and long-context benchmarks. Lightning's proposition is speed, cost, customization, and hardware efficiency at a sufficient quality floor. Context length is not evidence of equal long-context use, and “up to 4x faster” is an optimized-path ceiling rather than a fleet-sizing multiplier.

### 4. Switchyard's durable advance is per-turn routing inside an agent trajectory

**First-party fact:** Switchyard can observe multi-turn tool results and progress signals, then choose an efficient or capable model before the next model call. It does not switch within a single completion. Its stage router escalates on errors, stalled loops, exploration, and critical failures, and favors the efficient model after productive progress.

**Analysis, high confidence:** routing inside the trajectory is more expressive than assigning one model at task start. It also makes the router part of the governed system boundary. Adaptive logic must operate only within a deterministic allowlist established by data class, identity, purpose, tool scope, provider, and destination. Escalation must not override those controls.

The recommended efficient-first threshold was calibrated on a coding task set. It cannot be assumed to transfer to records work, policy analysis, multilingual interaction, or municipal operations.

### 5. Vendor cost claims demonstrate possibility, not a planning constant

The reviewed secondary report cited partner results ranging from 28% to 74% lower cost on different private or task-specific workloads, sometimes with a quality tradeoff. The headline “one-third the cost” lacked a public reproducible packet with the exact model pair, route distribution, task set, accuracy definition, and price snapshot.

**Recommendation:** measure cost per accepted workflow, including router overhead, frontier escape calls, retries, rework, human review, and failures. Cheap tokens can produce expensive workflows.

### 6. The releases strengthen a three-plane system view

**Inference for future work:** physical compute, serving/control, and workflow/governance are separate but coupled.

- Physical compute owns capacity, storage, networking, facilities, energy, cooling, resilience, and asset ownership.
- Serving/control owns approved model pools, APIs, routing, versioned runtimes, telemetry, staged rollout, failure recovery, and rollback.
- Workflow/governance owns purpose, human responsibility, identity, data and tool authority, credentials, evaluation, records, budgets, and lifecycle.

A GPU fleet alone cannot realize routing economics. A managed model alone cannot supply organization-specific authority and evaluation.

## Technical detail

The cheapest sufficient evaluation is sequential:

1. Establish whether the efficient or managed specialist model clears the quality floor on the actual product surface.
2. Use real repository or workflow tasks with predefined required elements.
3. Record accepted outcome, corrections, tests/regressions, tool validity, elapsed time, input/output tokens, credits or cost, retries, and failures.
4. Only after worker quality is established, replay representative multi-turn trajectories through capable-only, efficient-only, deterministic task-tier, and adaptive per-turn routes.
5. Record route share, escalation/de-escalation, p50/p95 latency, cache behavior, total tokens/GPU-seconds, memory pressure, human review, and cost per accepted workflow.
6. Stop if two calibrated thresholds add no decision-changing improvement or if attribution remains incomplete.

Operational caveats identified in the reviewed Switchyard release included incomplete route attribution in some failures/fallbacks, missing session identifiers in some statistics, possible upstream cost after cancellation, concentrated gateway credential and protocol risk, coding-derived calibration, and separate software/model license objects.

## Public sources

| Source title | Publisher or author | Publication date | URL and useful locator | Claim or finding supported | Verified date |
|---|---|---|---|---|---|
| MAI-Code-1.1-Flash announcement | Microsoft AI | 2026-08-11 | https://microsoft.ai/news/mai-code-1-1-flash-br-better-faster-at-a-quarter-of-the-cost/ | Launch and product claims | 2026-08-12 |
| MAI-Code-1.1-Flash model card | Microsoft AI | 2026-08 | https://microsoft.ai/pdf/MAI-Code-1.1-Flash-Model-Card.PDF | Architecture, training, benchmarks, limitations | 2026-08-12 |
| MAI-Code-1.1-Flash data card | Microsoft AI | 2026-08 | https://microsoft.ai/pdf/MAI-Code-1.1-Flash-Data-Card.PDF | Training-data and product-interaction treatment | 2026-08-12 |
| GitHub Copilot model pricing | GitHub | live | https://docs.github.com/en/copilot/reference/copilot-billing/models-and-pricing | Unit prices and billing mechanics | 2026-08-12 |
| GitHub Copilot model hosting | GitHub | live | https://docs.github.com/en/copilot/reference/ai-models/model-hosting | Hosting and enterprise training-data treatment | 2026-08-12 |
| Nemotron 3.5 Lightning BF16 model card | NVIDIA | 2026-08-11 | https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-BF16 | Architecture, license, hardware, benchmark table | 2026-08-12 |
| Nemotron 3.5 Lightning NVFP4 model card | NVIDIA | 2026-08-11 | https://huggingface.co/nvidia/NVIDIA-Nemotron-3.5-Lightning-30B-A3B-NVFP4 | Quantized deployment recipes and results | 2026-08-12 |
| NeMo Switchyard repository | NVIDIA | 2026 | https://github.com/NVIDIA-NeMo/Switchyard | Router architecture and implementation | 2026-08-12 |
| Stage-router documentation | NVIDIA | 2026 | https://github.com/NVIDIA-NeMo/Switchyard/blob/main/docs/routing_algorithms/stage_router_routing.md | Per-turn routing logic and calibration | 2026-08-12 |
| Known issues | NVIDIA | 2026 | https://github.com/NVIDIA-NeMo/Switchyard/blob/main/docs/known_issues.md | Current operational caveats | 2026-08-12 |
| Switchyard report | VentureBeat | 2026-08-11 | https://venturebeat.com/orchestration/nvidias-switchyard-router-reshuffles-ai-models-mid-task-cutting-task-costs-to-a-third-in-its-own-tests | Partner-reported cost/quality results | 2026-08-12 |

## Alternatives and conflicting evidence

- Microsoft's closed vertical integration may improve task fit and iteration speed; NVIDIA's open composition offers more control, portability, and independent evaluation. Neither is universally superior.
- A smaller active parameter count can reduce compute but does not eliminate full-weight memory, context-cache, concurrency, serving, and redundancy costs.
- Adaptive routing can reduce cost but adds another control plane, calibration problem, audit surface, and failure mode. Deterministic task-tier routing is the simpler comparator.
- Vendor common-harness results are more useful than unmatched leaderboards, but still require local outcome testing.

## Caveats and unresolved questions

- MAI-Code is coding-focused, closed, and product-bound; transfer to other harnesses and general knowledge work is unproven.
- Product availability and documentation had launch-day inconsistencies; verify the exact tenant and client.
- Lightning and Switchyard benchmark claims remain vendor/partner results until independently reproduced.
- The routing threshold is coding-derived and may fail on other domains.
- No municipal workload quality, capacity, energy, economics, or authorization decision follows from these releases.

## Corrections and freshness triggers

Reverify prices, billing, model availability, context limits, license terms, data-use policy, hosting, model cards, repository release, known issues, security policy, and router calibration before any evaluation or decision. Re-run outcome tests after a model, product surface, harness, tool set, provider, price, or policy change.

## Integration guidance

Integrate MAI-Code as a managed Copilot specialist candidate and Switchyard/Lightning as open serving-and-routing evidence. Preserve the distinction between model evaluation and routing evaluation. Do not alter a current default route from this packet. In CCSF material, use the three-plane and policy-constrained-routing implications only as pilot-design evidence, not as an architecture, vendor, capacity, or procurement decision.

## Exclusions and disclosure boundary

Excluded: personal live-stack route names and credentials; local hardware/runtime details; account licensing state; private task data; raw vendor intake; any unverified current service claim after 2026-08-12; and any assertion that CCSF or a department approved a pilot, provider, model, gateway, capacity, or procurement.

## Closeout

- **Public export commit:**
- **Destination content commit or commits:**
- **Ledger or manifest commit:**
- **Unresolved differences:** Work-side candidate status, product availability, and canonical placement remain unreviewed.

## Completion checklist

- [ ] The receiving agent can understand, verify, and integrate the cleared research without access to the originating private files.
- [ ] All eligible substantive detail, links, context, reasoning, caveats, corrections, and provenance were preserved.
- [ ] Facts, analysis, inference, and recommendations are distinguishable.
- [ ] Every decisive claim is traceable to a public source or explicitly identified reasoning.
- [ ] Raw intake and private, restricted, or otherwise ineligible context were excluded.
- [ ] Safe source and destination commits are recorded.
- [ ] Jeremy reviewed the exact public diff and affirmatively cleared it for public disclosure.
