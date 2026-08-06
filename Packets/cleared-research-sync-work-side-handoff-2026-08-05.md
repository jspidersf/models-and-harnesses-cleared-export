*Codex (GPT-5) · 2026-08-05*

# Cleared Research Sync — Final Work-Side Handoff

```table-of-contents
```

## Outcome

Complete the one-time work-side setup for occasional weekly, monthly, or ad hoc research reconciliation. The private personal and SFGOV repositories remain isolated. Two public export repositories carry only exact handoffs Jeremy affirmatively clears for public disclosure.

The work-owned `jp-sfgov/sfgov-cleared-research-export` owns the single canonical packet template. Claude on the work machine owns the recurring workflow through one project skill named `cleared-research-sync`. Do not create separate sync-in, sync-out, review, or push skills.

No research content is authorized for publication by this handoff. This pass changes process files only.

## Known public state

- Personal-to-work export: `jspidersf/models-and-harnesses-cleared-export`
- Work-to-personal export and canonical template: `jp-sfgov/sfgov-cleared-research-export`
- Work export comparison head: `76a5c57b2e8090c299ec68bb6e7feadd67b7f02b`
- Private work repositories: `jp-sfgov/sfgov-models-and-harnesses` and `jp-sfgov/sfgov-ccsf-compute`
- For sync runs, start Claude from the work M&H root so the nested physical CCSF checkout and both public sibling exports can be inspected without duplicating the skill.

Fetch current state and treat these as comparison anchors, not assumed current heads.

## Work-side procedure

1. Read the local `AGENTS.md`, `CLAUDE.md`, current session state, and sync-ledger instructions in every repository that may change.
2. Confirm the three work-owned repositories and the read-only personal export are clean, on expected branches, and synchronized with their remotes. Run the existing OneDrive integrity checks for both private work repositories. Stop on divergence, damage, dataless files, or conflict copies.
3. Fast-forward the personal export and verify this handoff is remotely reachable.
4. In `jp-sfgov/sfgov-cleared-research-export`, update `PACKET_TEMPLATE.md` to the exact template below. Update `README.md` so it defines packets as topic-bounded, full-fidelity research handoffs and names `PACKET_TEMPLATE.md` as the canonical standard for both directions. Preserve all existing public-disclosure warnings and exclusions.
5. In the private work M&H repository, create `.claude/skills/cleared-research-sync/SKILL.md` using the exact skill below. Do not duplicate the skill inside the CCSF repository; run cross-repository sync sessions from the M&H root.
6. Add only the smallest local navigation pointer required by the work repository's existing instructions. Do not copy personal instructions or paths into work files.
7. Record the process change in the work-side sync ledger or current-state authority without copying this entire handoff into a private research document.
8. Review three diffs separately: public template/README, private M&H skill/instruction pointer, and private CCSF ledger/current-state update. Run the audience firewall and secret checks.
9. Stop for Jeremy's authorization before committing or pushing. No process approval authorizes a research packet.
10. After authorization, commit and push the public template change, private M&H skill change, and CCSF ledger change separately. Verify each full commit is reachable from its intended remote and each working tree is clean.
11. Return metadata only: repository, branch, full commit, paths changed, remote-reachability verdict, integrity verdicts, exclusions, and unresolved differences. Do not return City document content.

## Canonical packet template

Use this content for the work export's `PACKET_TEMPLATE.md`, adapting only formatting required by that repository's local instructions:

```markdown
# Research Packet: <topic>

- **Template version:** 2026-08-05
- **Status:** DRAFT | CLEARED FOR PUBLIC DISCLOSURE
- **Direction:** personal → work | work → personal
- **Clearance date:**
- **Cleared by:**
- **Research period covered:**
- **Last verified:**
- **Originating private repository or repositories:**
- **Safe source paths:**
- **Source commits:**
- **Intended destination repository or repositories:**
- **Destination canonical document roles:**

## Purpose and context

Explain the problem, background, scope, intended use, and why the research matters to the receiving repository.

## Research scope and method

Describe what was examined, how evidence was evaluated, material assumptions, comparisons, calculations, and any important boundary on the research.

## Findings

Preserve the complete eligible research. For each material finding, distinguish:

- fact, analysis, inference, or recommendation;
- confidence and verification status;
- supporting evidence and reasoning;
- technical or operational detail needed to understand it; and
- decision relevance or destination implication.

## Technical detail

Include architectures, methods, measurements, calculations, alternatives, implementation constraints, or other detail needed to prevent the receiving side from reconstructing the work.

## Public sources

| Source title | Publisher or author | Publication date | URL and useful locator | Claim or finding supported | Verified date |
|---|---|---|---|---|---|
| | | | | | |

## Alternatives and conflicting evidence

Record competing interpretations, evidence in tension, rejected alternatives, and why the current treatment is preferred.

## Caveats and unresolved questions

Record limitations, uncertainty, missing evidence, open questions, and confidence boundaries.

## Corrections and freshness triggers

Preserve material correction history and state what event, date, version, price, policy, or source change should trigger re-verification.

## Integration guidance

Name the receiving canonical homes, relationships to existing material, expected transformations, and any destination-specific framing that should remain distinct.

## Exclusions and disclosure boundary

List what was deliberately excluded and why. Never include raw intake, sessions, credentials, private identifiers, private operating context, repository history, `audience: personal-only` material, Level 3–5 City data, or anything not affirmatively cleared.

## Closeout

- **Public export commit:**
- **Destination content commit or commits:**
- **Ledger or manifest commit:**
- **Unresolved differences:**

## Completion checklist

- [ ] The receiving agent can understand, verify, and integrate the cleared research without access to the originating private files.
- [ ] All eligible substantive detail, links, context, reasoning, caveats, corrections, and provenance were preserved.
- [ ] Facts, analysis, inference, and recommendations are distinguishable.
- [ ] Every decisive claim is traceable to a public source or explicitly identified reasoning.
- [ ] Raw intake and private, restricted, or otherwise ineligible context were excluded.
- [ ] Safe source and destination commits are recorded.
- [ ] Jeremy reviewed the exact public diff and affirmatively cleared it for public disclosure.
```

## Work Claude skill

Create `.claude/skills/cleared-research-sync/SKILL.md` in the private work M&H repository with this content:

```markdown
---
name: cleared-research-sync
description: Run a manual, reviewed research reconciliation across the personal and SFGOV account boundary. Use when the user says "sync," "periodic sync," "sync in," "sync out," "reconcile accumulated research," "prepare or review a cleared packet," or asks to pull, publish, integrate, or close a cleared-research exchange.
---

# Cleared Research Sync

Move eligible research knowledge between isolated private repositories through the two public export repositories. Synchronize content, not Git histories. Never schedule or publish unattended.

## Establish context

1. Read every applicable private repository's `AGENTS.md`, `CLAUDE.md`, current session state, and sync ledger or reconciliation manifest.
2. Identify the side from its private remote. Personal uses `jspidersf/models-and-harnesses`; work uses the private `jp-sfgov` M&H and CCSF repositories.
3. Locate both sibling public exports: `jspidersf/models-and-harnesses-cleared-export` for personal-to-work, and `jp-sfgov/sfgov-cleared-research-export` for work-to-personal and the canonical template.
4. Fetch every repository in scope. Require clean working trees and expected branches. Stop on divergence, damage, missing instructions, or unexplained local changes. On the work machine, also run the repository's OneDrive integrity checks.
5. Fast-forward the public exports and read the current work-owned `PACKET_TEMPLATE.md`. It alone defines packet completeness; do not restate its fields here.

## Find the delta

Read the recorded source, export, and destination commits. Compare only canonical research newer than those anchors.

- Inbound: find unprocessed commits and packets in the other side's public export.
- Outbound: find meaningful canonical research changes on this side that are eligible for public disclosure.
- Ignore raw intake, scratchpads, sessions, incomplete plans, credentials, private context, repository history, and `audience: personal-only` material.
- If neither direction has a decision-useful delta, stop without creating files or commits.

## Prepare without publishing

For inbound work, integrate the full eligible substance into the destination's canonical homes. Preserve stronger or newer destination context and identify unresolved differences.

For outbound work, create one topic-bounded, full-fidelity handoff under `Packets/` in this side's public export. Use the canonical template. The packet must let the receiving agent understand, verify, and integrate the cleared research without private-source access. Length is not the boundary.

Run the audience firewall, secret scan, source/provenance check, and exact diff review. Treat filenames, paths, commit IDs, queries, and tool arguments as disclosed metadata. Show inbound private diffs and outbound public diffs separately.

## Stop at two gates

Do not commit or push until the user gives the applicable explicit approval:

1. **Disclosure gate:** approval of the exact outbound packet for public disclosure.
2. **Integration gate:** approval of the exact private destination and ledger or manifest changes.

One message may approve both only when it names both decisions. Approval of research activity, classification, or an earlier packet is not approval of the current public diff.

## Publish and close

After approval:

1. Commit and push only the reviewed packet to the originating side's public export; verify remote reachability.
2. Commit and push destination-native integrations using the local repository's required separation. Keep M&H content, CCSF content, and CCSF ledger commits separate when applicable.
3. Record the source, packet, destination, and ledger or manifest commits; paths or canonical roles; clearance; exclusions; verification results; and unresolved differences.
4. Verify each repository is clean and local `HEAD` equals its expected remote branch.
5. Return metadata and decisions only. Never relay private City document contents to the personal side.

## Stop conditions

Stop if full fidelity requires publishing raw, private, restricted, or otherwise ineligible material; a decisive source cannot be recovered; the canonical template is unavailable; a repository is dirty or unexpectedly diverged; integrity checks fail; or the requested action would connect private histories, accounts, credentials, remotes, forks, or submodules.
```

## Review and authorization gate

Before any push, report:

- the exact public template and README diff;
- the exact private M&H skill and instruction-pointer diff;
- the CCSF ledger or current-state diff without relaying unrelated City content;
- proposed commit messages and repository targets; and
- all validation and integrity results.

Stop for explicit authorization. Do not infer authorization from this handoff's existence.

## Stop conditions

Stop if any repository is dirty or unexpectedly diverged; the work export head does not descend from the comparison head; the personal handoff commit is not remotely reachable; OneDrive integrity checks fail; a proposed public diff contains research or private metadata beyond this process update; or implementation would duplicate skills, templates, private histories, remotes, credentials, or accounts.
