*Codex (GPT-5) · 2026-08-05*

# Models and Harnesses Cleared Export

```table-of-contents
```

This public repository is the one-way personal-to-work exchange surface for reviewed research. It is not a mirror of the private personal repository.

## Publication rule

Everything committed here is public. ~~Publish only a small, self-contained packet that Jeremy has affirmatively cleared for public disclosure.~~ **Correction (2026-08-05):** publish a topic-bounded, full-fidelity research handoff that Jeremy has affirmatively cleared for public disclosure. A packet may be long; it must preserve enough eligible research, links, context, reasoning, caveats, and provenance for the receiving agent to understand, verify, and integrate it without access to the private source files.

Use the single canonical public [PACKET_TEMPLATE.md](https://github.com/jp-sfgov/sfgov-cleared-research-export/blob/main/PACKET_TEMPLATE.md) owned by the work export. Do not maintain a second template here. Each packet must pass that template's completeness test as well as the public-disclosure review.

Never publish raw intake, session history, credentials, private identifiers, City records, personal runtime details, repository history, or material marked `audience: personal-only`.

## Routine

1. Pull the work export and use its current canonical `PACKET_TEMPLATE.md` to prepare and review a packet in the private source repository.
2. Copy only the cleared packet into `Packets/` in this repository.
3. Review the exact public diff, then commit and push.
4. The work machine pulls this repository and integrates the useful content into its own canonical documents.
5. Record the destination commit; do not merge or connect the source repositories.
