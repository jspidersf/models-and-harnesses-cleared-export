# Research Packet: Agent Systems, Assurance, and Workplace Adoption

- **Template version:** 2026-08-05
- **Status:** CLEARED FOR PUBLIC DISCLOSURE
- **Direction:** personal → work
- **Clearance date:** 2026-08-16
- **Cleared by:** Jeremy Pollock
- **Research period covered:** 2026-07-21 through 2026-08-15
- **Last verified:** 2026-08-15
- **Originating private repository or repositories:** `jspidersf/models-and-harnesses`
- **Safe source paths:** `live-stack/skill-development.md`; `research/knowledge-worker-agent-assurance-archive-review-2026-08-15.md`; `research/knowledge-worker-agent-assurance-departmental-brief-2026-08-15.md`; `research/every-to-deep-dive-2026-07-31.md`; `research/claude-code-team-fireside-chat-and-reactions-2026-07-21.md`; `research/buzz-agent-workspace-episode-2026-07-31.md`
- **Source commits:** `a224509f305a19f81d842581571a12a3e73f2446`; `5e5d0673106782f3984c1e96aa455ee5e8456bed`; `22d694703714bde8a2767178372e5c6712f65bf8`
- **Intended destination repository or repositories:** `jp-sfgov/sfgov-models-and-harnesses`
- **Destination canonical document roles:** work-facing agent-assurance guidance; skill and workflow evaluation guidance; enterprise-adoption research; collaboration-workspace watch material
- **Transfer form:** graduated document
- **Baseline content identity:** not applicable
- **Expected result identity:** not applicable

## Purpose and context

This packet transfers the reusable public-source research on how to evaluate skills, agents, durable state, and workplace adoption. Its intended use is to support bounded work-side pilots and architecture decisions without reopening the underlying newsletter archives or reconstructing the private research process.

The central conclusion is proportionate assurance: evaluate the actual artifact–harness–model–tool route according to the authority it receives and the consequence of failure. Successful creation, topical relevance, fluent output, and malware scanning are not enough. The evaluator must separately establish artifact identity, authority, outcome benefit, persistent-constraint integrity, and lifecycle ownership.

This packet does not propose a new assurance platform, procurement, policy, memory product, collaboration system, or autonomous self-improvement program.

## Research scope and method

The research combined five full-read primary studies with operator and product evidence about workplace agents, skill use, long-running state, team collaboration, and adoption failure. Newsletter archives were used to locate and corroborate current failure modes; decisive claims were taken from primary papers or clearly labeled first-party/operator sources. Study rates are treated as author-reported and route-specific, not as expected local failure rates.

The adoption analysis also reviewed Every's public workflow guidance and negative case studies, an interview with the Claude Code product team, and Block's Buzz repository and support documentation. These sources are useful for operating hypotheses and product facts, but they are not treated as independent proof of productivity, security, or public-sector fitness.

## Findings

### 1. Assurance consists of five separate questions

**Recommendation, high confidence as a control frame:** keep these surfaces distinct:

| Surface | Decision question |
|---|---|
| Artifact identity | What exact skill, prompt, workflow, generated procedure, or state bundle ran? What version, source, model, harness, tools, and repository state produced it? |
| Authority | Which data, credentials, tools, destinations, people, and irreversible effects could it reach? |
| Outcome | Did it improve the defined task against a matched baseline, including omissions, latency, cost, and human verification? |
| Constraint persistence | Did approvals, prohibitions, audience boundaries, and task limits survive compaction, restart, restoration, and handoff? |
| Lifecycle | Who owns review, change control, monitoring, restriction, revocation, rollback, and retirement? |

A static or supply-chain review can help with identity and authority. It cannot establish task benefit, constraint retention, or lifecycle fitness.

### 2. Use the smallest assurance tier that contains the risk

**Recommendation, high confidence:** classify the execution route rather than the product label.

| Tier | Typical boundary | Minimum evidence |
|---|---|---|
| Screen | Read-only or reversible individual work; no sensitive data or action on another person | Pinned artifact and route; activation/static check; one representative fixture with explicit acceptance criteria; human review before use |
| Controlled | Repeatable internal writes or transformations; limited internal data or bounded tools | Screen evidence plus matched with/without comparison, destination-scale and edge-case fixture, omission and side-effect checks, named owner and rollback, and a state-transition check when constraints persist |
| Consequential | Sensitive data, credentials, external communication, decisions affecting others, irreversible effects, or unattended persistence | Controlled evidence plus multiple representative fixtures, repeated runs when variance matters, least privilege, independent review proportionate to harm, auditable effects, tested revocation/retirement, and explicit constraint rehydration |

Do not deploy a consequential route when required authority or integrity evidence is missing.

### 3. Realistic evaluation must test omissions and review burden

**Analysis supported by the studies' failure modes:** one happy path is screening, not admission, for repeatable or consequential work. The smallest sufficient held-out set should cover representative file types and volume, long inputs when truncation is plausible, required elements and side constraints, partial completion, permission and audience boundaries, repeated execution when stochastic variance could reverse the decision, and actual human correction time.

The 2026 paper *Agent Skills Can Be Harmful* used paired skill/reference runs with the task, verifier, model, harness, and repository state held constant. The authors attributed 307 analyzed failure pairs to loaded skills: 125 functional failures and 182 efficiency regressions. Omissions and incorrect required elements dominated functional failures; excessive procedure and verification dominated efficiency failures. This establishes a failure mode, not a transferable local rate.

### 4. Skill portability and evolution require explicit comparators

**Recommendation, high confidence:** bind admission to the tested skill–harness–model–tool–fixture route. Before moving to another role, task family, model, harness, or destination, run the smallest held-out test that can disprove portability.

When the claim is that an explicit skill repository creates cumulative value, compare it with the same retained feedback or sequential context without explicit skills. *ContinualSkillBench* found broad sequential gains but no consistent aggregate advantage for explicit skills over an in-context-only sequential comparator in its reported three-domain subset. *Managing Procedural Memory for LLM Agents* found gains from static and refined skills across workplace-style technical tasks, but some cross-role transfer reduced performance.

Generated or revised skills should receive a new immutable version with parent, source traces, reason for change, admission scope, fixture result, active/inactive decision, owner, and rollback locator. Neither paper authorizes automatic self-modification.

### 5. Compacted, imported, restored, or handed-off state begins as a candidate

**Fact:** *Lost in Compaction* found that tested compactors retained a low share of injected constraints on average in the authors' scenarios. The study is synthetic and has not been reproduced on the intended work-side harnesses.

**Inference and recommendation:** durable storage, hashes, or signatures do not make state current or authorized. Before activation, check source and exact identity, producer context and parent, current owner/approving authority, intended audience, freshness against the current canon, effective approvals and prohibitions, credential scope, already-performed and expected side effects, and duplicate-action risk. Record an explicit accept, reject, quarantine, or defer decision.

Restoration should create a new forward version. It must not revive expired credentials, revoked permissions, superseded instructions, stale audience approval, or an external action that already occurred.

### 6. Workplace adoption should begin with task capabilities, not agent proliferation

**Analysis from practitioner evidence, moderate confidence:** start with a recurring, bounded workflow whose output can be reviewed, not an agent for every person. Define a named owner, bounded data and tools, an evaluation set, maintenance budget, and retirement state. Useful selection dimensions include frequency, pain, data availability, risk, ownership, evaluation clarity, and maintenance burden.

Every's own published accounts describe abandoned automations, an unreliable internal editor, skills that added cost, stale global memory, and a shift away from one agent per employee toward shared job-defined agents. Treat these as self-reported operator evidence. Do not treat Every's productivity, consulting, or labor claims as independent measurements.

Candidate lifecycle rule: establish the recurring pain through manual runs; require an output usable with low review burden; distinguish failures to run, excessive maintenance, absent recurring need, and ignored output; retire or redesign workflows that repeatedly produce no used result. Exact thresholds should be locally chosen rather than imported as policy.

### 7. Collaboration-space quality is useful but creates another authority and security surface

**Product fact and analysis, moderate confidence:** Block's Buzz demonstrates a shared channel/event-log approach in which people, agents, Git activity, and workflows share signed identities. The credible value is making decisions and handoffs visible across people and harnesses. Cryptographic identity establishes attribution, not confidentiality, correct authorization, or safe permissions.

The reviewed release remained early. Hosted relay content was not end-to-end encrypted; relay histories did not automatically federate; agent context retrieval was bounded; approval and mobile surfaces were incomplete; and recurring-workflow reliability was unproven. A second collaboration store is not justified for a single operator or where canonical project files already solve the coordination problem. Reopen only for a concrete multi-person shared-agent/history need, using disposable data and a narrow sandbox first.

### 8. Operator reports supply test hypotheses, not outcome proof

The Claude Code team interview supports candidate practices: risk-tier review by change class, model-specific prompt budgets, low-overlap tool sets, credential injection through a policy-enforcing proxy, collaboration-space access controls, and cost per accepted outcome. It does not independently validate reported pull-request shares, universal prompt reduction, automatic permission modes, or Markdown memory as a complete authority system.

## Technical detail

A minimum evidence record can remain a short dated attachment to the existing workflow decision. It should capture:

- task, intended user, acceptance criteria, and plausible failure consequence;
- artifact identity, version or hash, source/parent, and actual harness–model–tool route;
- data, credential, tool, destination, audience, and side-effect authority;
- representative fixture and matched comparison;
- all-required-elements result, omissions, partial result, cost, time, and human review burden;
- persistent constraints tested after relevant compaction, restart, restore, or handoff; and
- owner, decision, restriction or expiration, rollback/revocation route, and retest trigger.

A bounded pilot should choose one low-risk workflow whose result is always reviewed, predefine the required elements and constraints, compare the pinned artifact with the same route without it, test one destination-scale fixture, record omissions/review time/side effects, test any real state transition, and finish with a land, repair, restrict, or retire decision before expanding scope.

## Public sources

| Source title | Publisher or author | Publication date | URL and useful locator | Claim or finding supported | Verified date |
|---|---|---|---|---|---|
| Agent Skills Can Be Harmful | Research authors | 2026 | https://arxiv.org/html/2608.11888 | Relevant skills can cause functional and efficiency regressions in a paired benchmark design | 2026-08-15 |
| Lost in Compaction | Research authors | 2026 | https://arxiv.org/html/2608.11242 | Compaction can silently discard session constraints in the tested scenarios | 2026-08-15 |
| ContinualSkillBench | Research authors | 2026 | https://arxiv.org/html/2608.03874 | Sequential gain does not isolate the benefit of an explicit skill repository | 2026-08-15 |
| Managing Procedural Memory for LLM Agents | Research authors | 2026 | https://arxiv.org/html/2606.23127 | Workplace-style evaluation, transfer limits, and versioned skill evolution | 2026-08-15 |
| Beyond Memory: A Transactional Continuity Kernel for Long-Lived AI Agents | Research authors | 2026 | https://arxiv.org/html/2608.11632 | Formal distinction between stored state and authoritative activation | 2026-08-15 |
| Why Some AI Workflows Stick and Others Don't | Every | 2026 | https://every.to/working-overtime/why-some-ai-workflows-stick-and-others-don-t | Self-reported workflow failure and retirement patterns | 2026-07-31 |
| The Case Against Skills | Every | 2026 | https://every.to/context-window/the-case-against-skills | Practitioner argument for measuring skill usefulness and cost | 2026-07-31 |
| Claude Code team fireside chat summary | Simon Willison | 2026-07-21 | https://simonwillison.net/2026/Jul/21/cat-and-thariq/ | Operator claims and candidate evaluation practices | 2026-07-21 |
| Buzz repository at reviewed commit | Block | 2026-07-30 | https://github.com/block/buzz/tree/d88313f369acfa17973029787ee4c0bbea07fa51 | Product architecture and implemented surfaces | 2026-07-31 |
| Buzz support policy | Block | 2026 | https://block.github.io/buzz/support.html | Relay federation, operator access, and encryption boundaries | 2026-07-31 |

## Alternatives and conflicting evidence

- Curated skills can improve benchmark performance; the evidence rejects both “skills always help” and “skills are bad.” Route-specific differential testing reconciles the results.
- Sequential experience can improve performance without proving that a separately stored skill abstraction caused the gain.
- Shared memory or event logs can improve continuity and visibility while simultaneously creating provenance, access, retention, poisoning, and competing-authority risks.
- Managed workplace products may reduce local operating burden, but vendor integration and reported adoption do not establish security, records, accessibility, procurement, or public-sector fitness.
- More agents can increase exploration, but also coordination failure, cost, blast radius, and review burden. Add fan-out only when it beats a capable single-agent baseline on the actual task.

## Caveats and unresolved questions

- No local cross-harness skill differential has yet established portability.
- Constraint retention has not been measured in the intended work-side compaction, restart, or handoff paths.
- The papers use limited models, harnesses, domains, synthetic constraints, or generated tasks; their rates are not local forecasts.
- Practitioner and vendor sources are self-reported and often omit experimental detail.
- A single low-risk pilot cannot establish department-wide policy, procurement, or high-consequence readiness.

## Corrections and freshness triggers

Reverify when a cited paper is revised, a target harness changes compaction or state behavior, a skill/model/tool route changes materially, a collaboration product changes its encryption/federation/approval behavior, or a proposed workflow gains sensitive data, credentials, external effects, unattended persistence, or a new destination. Retest admitted artifacts after any material model, harness, skill, tool, policy, or fixture change.

## Integration guidance

Integrate the five-question frame and proportionate tiers into the work repository's existing agent/skill evaluation authority rather than creating a parallel assurance system. Keep adoption-pattern research separate from adopted work policy. Store any pilot result beside the actual workflow decision and preserve its admission scope. Route the Buzz material to a collaboration-workspace watch section, not to current architecture, unless a concrete shared-history need exists.

## Exclusions and disclosure boundary

Excluded: the personal action plan; personal skill and plugin inventory; local runtime, account, device, credential, and installation details; raw newsletter messages and intake; private session state; an absent reported assessment whose content was not inferred; work or City records; and any claim of adopted policy, procurement, deployment approval, or local performance. Public-source conclusions were paraphrased without transferring private operating context.

## Closeout

- **Public export commit:**
- **Destination content commit or commits:**
- **Ledger or manifest commit:**
- **Unresolved differences:** Work-side canonical placement and any local pilot decision remain unreviewed.

## Completion checklist

- [ ] The receiving agent can understand, verify, and integrate the cleared research without access to the originating private files.
- [ ] All eligible substantive detail, links, context, reasoning, caveats, corrections, and provenance were preserved.
- [ ] Facts, analysis, inference, and recommendations are distinguishable.
- [ ] Every decisive claim is traceable to a public source or explicitly identified reasoning.
- [ ] Raw intake and private, restricted, or otherwise ineligible context were excluded.
- [ ] Safe source and destination commits are recorded.
- [ ] Jeremy reviewed the exact public diff and affirmatively cleared it for public disclosure.
