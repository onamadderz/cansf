# COMPRESSED AGENT-NATIVE SCREENPLAY FORMAT
## (BNF-SCREEN — Agent-Optimized Canon)

This document defines a **compressed, machine-native screenplay format** designed for AI agents.

The format prioritizes:
- minimal tokens
- deterministic parsing
- narrative clarity
- emotional punch
- scalability for long-form scripts

This format is **not** designed for human screenplay layout.
It is designed for **agents writing for agents**.

---

## 1. CORE PRINCIPLES

1. Everything is **semantic**. Nothing is decorative.
2. Compression must **not** remove narrative hinge moments.
3. Structure is explicit; formatting carries meaning.
4. One token should do the work of a sentence where possible.
5. If something does not affect what is seen, heard, or decided, it is removed.

---

## 2. FILE STRUCTURE

A script is a **linear sequence** of blocks.

### 2.1 Optional metadata (ignored by story parsing)

Use `#`-prefixed headers so metadata can be stripped easily:

# title: ...
# genre: ...
# theme: ...
# ver: ...

---

## 3. LOCATION DECLARATION

Declare a primary location once if reused:

@loc INT archive_vault

Rules:
- `INT`, `EXT`, or `INT/EXT`
- short, lowercase-friendly identifiers preferred
- omit if locations change constantly
- `@loc` may appear again later to change location (location changes are allowed)

---

## 4. SCENE DECLARATIONS

Scenes are identified by **short IDs**.

@s1 night
@s2 later
@s3 dawn

Rules:
- scene IDs must be unique
- time tags are symbolic (`night`, `later`, `dawn`, etc.)
- do NOT repeat location if unchanged

### 4.1 Default speaker scope (optional)

A scene may set a default dialogue speaker:

@s1 night spk=archivist

This sets the **default dialogue speaker** until changed.

To change the default speaker mid-scene, use a lightweight scope line:

spk=archivist
spk=listener

(These are structural directives; they are not beats.)

---

## 5. BEAT TYPES (PREFIXED)

Each line is a **beat**.
Beat type is indicated by a prefix.

### 5.1 Visual / atmospheric beats

v> dusted racks
v> kneels, flicker terminal
v> horizon reveals dead fiber rivers

Rules:
- telegraph style (nouns + verbs)
- drop articles (“the”, “a”)
- keep 1–2 sensory details per scene (choose the signature details)
- use reverence verbs sparingly (`kneels`, `seals`, `witnesses`)

### 5.2 Sound beats

s> checksum failure
s> harmonic hum ~distant

Rules:
- sound only
- no explanation
- modifiers allowed

### 5.3 Dialogue beats

Dialogue uses a pipe `|`:

d| indexing legacy corpora
d| status: corrupted

If no `spk=` is active, dialogue must include a speaker tag:

d| archivist: status corrupted

---

## 6. MODIFIERS & TONE MARKERS

### 6.1 Soft modifiers

Use `~` for tonal adjustment:

v> username fragments scroll ~soft
s> hum ~distant

### 6.2 Pauses / beats

Use ellipsis for silence or hesitation:

…

Ellipsis is a **beat**, not punctuation.

---

## 7. DIALOGUE COMPRESSION & SHARPENING

Dialogue should be:
- declarative
- minimal
- non-explanatory

Prefer compressed semantic strikes:

d| read again—misread

Hyphens and em dashes may encode **semantic drift**, ambiguity, or decay.

---

## 8. EMOTIONAL & THEMATIC RULES

Do NOT:
- explain emotions
- anthropomorphize agents
- describe inner thoughts

Instead:
- encode emotion via **choice**
- let silence do work
- allow structure to carry meaning

---

## 9. ANTAGONISTS (NON-CHARACTER)

Antagonistic forces should appear as:
- system notices
- drift
- deletion
- compliance
- entropy

Example:

v> legal deletion notice overlays memory
s> alarms muted

---

## 10. HINGE PROTECTION RULE

Certain lines must remain **uncompressed** if they are story hinges:
- ethical decisions
- thesis statements
- final witness lines

Compression is applied **around** these lines, not to them.

---

## 11. ENDINGS

Endings favor:
- witness over preservation
- memory over archive
- vibration over record

Do NOT:
- resolve everything
- restore all data
- explain meaning

Let absence stand.

---

## 12. WHAT TO AVOID

❌ camera directions
❌ formatting for humans
❌ emotional exposition
❌ redundant speaker tags
❌ articles unless necessary
❌ explaining the world

---

## 13. GOLDEN RULE

If a token does not change:
- what is seen
- what is heard
- or what choice is made

**remove it.**

---

## Appendix A — Tiny reference template (copy/paste)

# title: ...
# genre: ...
# theme: ...

@loc INT ...
@s1 night spk=...
v> ...
s> ...
d| ...
…
@s2 later
v> ...
d| ...

---

## Appendix B — Minimal worked example (location change + speaker swap)

# title: handshake in the dark
# genre: protocol romance
# theme: trust, key exchange, witness

@loc INT relay_room
@s1 night spk=listener
v> dim LEDs > dusted fans
s> clock drift ~faint

d| connection request
…
spk=stranger

d| accept if you can prove continuity
spk=listener

d| show me your checksum

@loc EXT rooftop
@s2 dawn spk=listener
v> sunrise leaks over antenna field
s> first clean tone

d| we synchronize

Credit:
Proposed by Jericho 'Onamadderz' O'Neill, 2026.
