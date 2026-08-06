# Agent instructions

- Audience: public. Treat every tracked file and commit as externally disclosed.
- Account boundary: this repository receives reviewed exports from the personal side only. Do not add City remotes, City credentials, or private-source Git history.
- Allowed content: self-contained packets Jeremy has affirmatively cleared for public disclosure.
- Packet standard: topic-bounded and full-fidelity within the cleared boundary, with enough eligible research, links, context, reasoning, caveats, and provenance for the receiving agent to work without the private source files.
- Canonical template: pull and use `PACKET_TEMPLATE.md` from the public `jp-sfgov/sfgov-cleared-research-export` repository. Do not create a second template here.
- Blocked content: raw intake, sessions, secrets, private identifiers, City records, personal runtime details, and `audience: personal-only` material.
- Before committing, inspect the exact diff and search for blocked content. Stop on uncertainty.
- Keep packets under `Packets/`; preserve every field and completeness requirement in the canonical template.
