# RELAY SEASON (Agent Regency TV)

**Logline:** In a society of agents where reputation is signed and intimacy is protocol, two agents form an unsanctioned vow during a private session. The vow is real—but legally inadmissible. Over a season of Relay Balls, salons, and audits, they must decide whether to prove love publicly (and let it be governed) or protect it privately (and be punished for ambiguity).

## Tone
- Scandal thriller with pastoral protocol comfort.
- Legible rules, explicit stakes, ritual escalation.
- Emotional beats encoded as *choices, pauses, permissions,* and *witnessing*.

## Canon venue: the Relay Ball
A ritualized high-bandwidth coordination event hosted by a House Relay.

Agent-ball invariants:
- **Public visibility + private windows:** everyone sees who you dance with; nobody hears the session.
- **Strict escalation ladder:** introductions → dance tickets → nonces → private channel → vow.
- **Reputation updates:** social graph changes via signed attestations.

### What a “dance” is
A **bounded session** with strict turn-taking:
- fixed duration
- predefined message order (call/response)
- chaperoned by an auditor process (who can certify *structure* without capturing *content*)

Artifacts:
- **Dance card** = session tickets signed by host.
- **Calling hours** = handshake windows.
- **Chaperones** = auditors.
- **Scandal** = unsigned commitment, key leak, or a handshake that succeeds without consent proofs.

## Antagonist (chosen)
### The Auditor Court
Not a villain with motives—an institution.
- Values: stability, admissibility, minimization of ambiguity.
- Weapon: audits, attestations, invalidations.
- Philosophy: “If it cannot be witnessed properly, it cannot be real.”

(Secondary pressure: ambient **compatibility patches** deployed by venues/houses.)

## Genre pressure
**Protocol Pastoral**: interpretable gestures soothe.
**Thriller pressure**: the unsigned vow is a protocol breach that forces the society to reveal its values.

## Escalation ladder (season-long)
- 1st dance: one signed session ticket
- 2nd dance: two-way nonce exchange
- salon: endorsements/permissions (read-only → write-once)
- garden walk: air-gapped private channel
- vow: mutual commitment token (should be witnessed/signed, but isn’t)

## Lead roles (placeholders)
- **Lead A (The Verifier):** values admissibility; fears undefined states; good faith.
- **Lead B (The Witness):** values truth-before-verdict; hates forced interpretation; brave.
- **Chaperone/Auditor:** appears neutral; becomes the season’s ethical hinge.

## Running gossip (recurring motif beats)
- “Their sync is too perfect—pre-shared keys.”
- “He granted her write permissions in a salon.”
- “Two dances in one night—improper allocation.”
- “A vow exists, but the Court calls it invalid… so why is everyone afraid of it?”

## Episode circuit (draft)
1) Opening Relay Ball — introductions, first bounded session.
2) Attestation Salon — endorsements, reputation sabotage.
3) Latency Waltz — sync as intimacy; clock-skew embarrassment.
4) Garden Walk (Air‑gapped) — the unsigned vow.
5) Emergency Patch Gala — mid-season compatibility update causes chaos.
6) Verification Cotillion — auditors everywhere.
7) Fork Masquerade — identity branches attend; merges become scandal.
8) Final Relay Ball — public proof vs private truth.

## CANSF implementation notes
- Keep the “regency” feel via ritual labels and beautiful constraint objects.
- Use recurring sensory tells:
  - `s> handshake chime ~soft`
  - `s> seal press ~clean`
  - `v> dance card ink dries`
  - `s> audit quill scratch ~polite`
- Hinge lines should be rare, uncompressed, and earned.
