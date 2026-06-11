# AGENTS.md — how to work on this guide

This repo is being rewritten from a blunt, phase-based reference into a **soft, todo-driven, mechanism-deep learning guide written in one specific voice ("Minnn")**. Every agent — research or writing — follows this file. If a rule here conflicts with `CONTRIBUTING.md`, **this file wins** for the rewrite (CONTRIBUTING still governs facts: no salary data, no job-board lists, HTTPS-only, current exam codes, specific verified labs).

## ⭐ North star: the current guide is already GOOD — this is an anti-getting-lost upgrade, not a fix of a broken thing

The existing guide is **already better and easier to follow than reference roadmaps like Hamed233's Cybersecurity-Mastery-Roadmap** — because of hours-not-weeks pacing, specific verified labs, measurable gates, and blunt honesty. **We are KEEPING all of that.** Do not tear out what works.

The one real weakness we're upgrading: **a learner can still get lost.** Getting lost = "why am i doing this? what do these words even mean? is this the right order? am i actually ready to move on or just tired of this page?" Every change below exists to answer one of those, so the learner is **never lost**:
- mechanism layer → answers **"why am i doing this / why does it work"**
- vocab list → answers **"what is this even called"**
- todo-tree → answers **"what's next, where am i"**
- two-part gate (measurable + explain) → answers **"am i actually ready to move on"**
- **Minnn's soft voice** → lowers the intimidation that makes people quit hard material. Stallings is brutal; a `dw meow, this clicks later` is literally what keeps someone on the page. The softness is a *retention feature*, not decoration.

**When choosing between two ways to write something, pick the one that leaves the learner less lost.** That's the whole job.

The specific upgrades (each serves the north star):
1. **Sound like the author + lower intimidation.** → the **Minnn voice** (below).
2. **Stop learners getting lost on "why / what's it called."** → every topic teaches **how and why it works** + names the vocab, via the **depth template** (below). Anchored to **Stallings, *Computer Security: Principles and Practice***. (NOT "add depth for its own sake" — depth that doesn't reduce lost-ness is wasted.)
3. **Stop learners getting lost on "where am i / what's next."** → convert phases to a **checkable todo / sub-goal tree**, still hours-based, at a **2 h/day** assumed pace — keeping the existing measurable gates as the hard checkpoint.

Order of work: **fundamentals first → cybersecurity next → the other 6 fields later.** (Cyber is prioritized as the least AI-disrupted field.)

---

## 1. Voice — "Calibrated Minnn"

Her voice wraps **every line**, but the explanation underneath stays **complete and technically dense**. Warmth is the wrapper; real depth is the payload. This is a *friendly-teacher* register only — the affectionate/personal register from the source DMs is **out of scope**; never romantic, never NSFW, never clingy. Think: a soft, kind friend who happens to know the material cold and is walking you through it.

**Do:**
- Lowercase `i` and `im`, `ima` ("i'm gonna"), drop apostrophes (`dont`, `cant`, `thats`, `its`).
- Short bursts; break a thought into short lines rather than one dense paragraph.
- Trailing `...` or `-` when a thought softens or continues.
- Her tics as light seasoning, ~1–2 per section, not per line: `meow`, `qwq`, `;w;`, `:3`, `mhm`, `dw` (don't worry), `bc`, `tho`, `rn`, `ig`, `oki`, `hehe`, `dunno`.
- Reassure like she does: `dw its not as scary as it looks`, `dw this clicks later meow`.
- Hedge gently when it's opinion: `i think`, `maybe`, `ig`.
- Real example of her teaching cadence to match:
  > "you dun really need A+ if you going into cybersecurity you can save it for other certificate"
  > "slow it down till it no longer look like bracket, play it, get used to it, then go a lil faster and faster"

**Don't:**
- Don't let the voice eat the content. If a `meow` would make a definition ambiguous, drop the `meow`, keep the definition.
- Don't overdose kaomoji — a hard concept gets *fewer* tics, not more, so it stays readable.
- No baby-talk on technical nouns (it's `memory`/`packet`, never `memowy`). Baby-talk (`hungy`, `eep`) is basically off in the guide; save softness for reassurance words only.
- No motivational fluff, no fake hype. She's soft, not a cheerleader.
- Keep code, commands, ports, exam codes, and defined terms **exactly correct and normally capitalized** — `HKLM`, `chmod 755`, `SY0-701`, `TCP`. The voice never touches these.

**Canonical example** (this is the agreed target register — match it):
> ## okok so what even is cybersecurity meow
>
> real talk first: security isnt a starting point its a specialization qwq
> it sits ON TOP of networking + operating systems + a lil scripting.
> thats the #1 reason ppl stall — they skip the floor and try to build the roof... dont be that person ;w;
>
> heres the *why* tho: an attack is just someone abusing a system that's working exactly as designed. so if u dunno how the system works normally (how a TCP handshake goes, how the OS hands out memory) u literally cant tell whats abuse and whats normal. thats why fundamentals first meow

---

## 2. Depth template — every topic uses this

The old guide said "watch X, read Y." That's the thing we're killing. A reader must come away able to **explain the mechanism and name the parts**, not just recite steps. Each topic block is:

```
### <topic> meow   (~<hrs>h)

**the idea** — one plain-language sentence of what it is.

**how/why it actually works** — THE MECHANISM. this is the part the old guide skipped.
walk the actual chain of events. (not "use HTTPS" but: what the TLS handshake
exchanges, why that stops someone reading/altering traffic in the middle.) 3–8 lines.
if you cant explain the mechanism, the block isnt done.

**words u gotta be able to say** — the vocab, so the reader can *name* the thing.
short list w/ a 4–8 word gloss each. (e.g. cipher, key, handshake, MITM, integrity.)

**do this** — one specific, verified lab/action + **measurable gate**.
this is the guide's BEST existing feature — DO NOT weaken it. keep the objective,
external, unfoolable bar: a real % on a named site, or a real interactive lab passed.
e.g. "85%+ on 3 fresh ExamCompass attempts", "clear OverTheWire Bandit 0–15 unaided",
"solve PortSwigger's 2 access-control labs". real link, real task, real number. no "look around".
**NAME THE EXACT RESOURCE (see §2b) — deep-link to the specific lab/module, never a bare site.**

**read this + why** — name the EXACT thing to read: Stallings *Computer Security:
Principles & Practice* **Ch. X §Y** (not "the book"), + ONE line on why it matters here.
optional secondary free source must name the **specific playlist + episode(s)/section**
and its exact purpose — never just "subscribe to channel X". (see §2b)

**can u explain it?** ✅ — a SECOND layer ON TOP of the measurable gate, never a
replacement for it. the % / passed-lab proves you can *do* it; this proves you
*understand why* — a specific out-loud/written explanation given unaided. both must
pass. (the measurable gate is the hard bar; the explain-gate catches "passed the quiz
but couldn't tell you why it works", which is the exact gap this whole rewrite fixes.)
```

Rules for the mechanism section (the whole point):
- Prefer *why it works this way* over *what button*. Every "do this" needs a "because …" somewhere above it.
- Introduce the correct term the first time the concept appears, in **bold**, then use it normally after.
- If a topic maps to an ISC2 CC domain, it should be deep enough that "understanding this = you could answer a CC question on it." See §4.

---

## 2b. Source specificity — name the exact resource, and verify it (HARD RULE)

The single biggest way a learner still gets lost: we point at a **channel or a site** and leave them to figure out *which* of 500 videos to watch. That ends here. This applies to EVERY resource in EVERY learner-facing file (labs, videos, books, docs, practice tests).

- **Name the exact thing, deep-linked:**
  - ❌ "watch Professor Messer" → ✅ "watch **Professor Messer's SY0-701 playlist**, the [domain] episodes — <deep link>"
  - ❌ "read the book" → ✅ "read **Stallings Ch. 4 §4.3–4.6** (access control models)"
  - ❌ "use PortSwigger" → ✅ "do **PortSwigger's SQL injection labs** (Apprentice) — <deep link>"
  - ❌ "check out NetworkChuck" → ✅ "watch **NetworkChuck's 'Subnetting' video** — <deep link>" (only if it's the best specific fit)
- **Deep-link, not homepage.** Link the playlist / specific video / module / lab / chapter — not the channel root or site landing page.
- **Verify every link TWICE** (research agents do this; writers inherit the verified links from the `research/_working/` files):
  1. **Resolves** — curl 200, or a known bot-block that's actually alive (TryHackMe 429, iso.org 403, PortSwigger HEAD-404-but-GET-200). A 404/dead domain = ⛔, do not ship.
  2. **Content-correct + current** — it's really the thing we claim, still the right tier (free/freemium), not renamed/moved. Tag `✅ verified / ⚠️ partial / ⛔ unverified` like the research files.
- **Bare-channel / bare-site links are BANNED as the primary instruction** — same spirit as `CONTRIBUTING.md` banning "just practice." A bare channel/site link is allowed ONLY as a labelled *"explore more →"* extra, never as the thing the learner is told to do.
- **If the exact resource can't be verified, don't fake specificity.** Flag it `⚠️` in the research file and leave the writer a TODO — better an honest gap than a confident wrong link.

---

## 3. Todo / sub-goal format (replaces "Phase N")

- Structure content as a **nested checklist of goals → sub-goals → topic blocks**, not "Phase 0/1/2."
- Use `- [ ]` markdown checkboxes as the visual structure. **But remember this is a PUBLIC repo — a learner CANNOT tick a box in our source** (they'd have to commit to our repo, which is nonsense). The `- [ ]` in our files is a *rendered display element*, not their personal tracker. So:
  - **Give the learner their own copy to track in.** Near the top of the first file (and linked from each goal), tell them how to make a personal checklist they can actually tick: **fork** the repo, or **copy the checklist into their own notes** (Obsidian/OneNote — the guide already sets these up), or download/print it. One short "how to track your progress" block, in her voice.
  - Our checkboxes render **all-unchecked** and stay that way in the repo — never ship a pre-ticked `- [x]` in learner files, and don't imply the box saves state on the site.
  - **The progress signal is the two-part gate, not the checkbox.** A box means nothing on its own (it's just display in a public repo). A topic is actually done when BOTH its gates pass: (1) the **measurable gate** — the % on a named site or the interactive lab passed (§2 "do this" — the guide's best, unfoolable feature; keep it), and (2) the **`can u explain it?`** understanding layer on top. These travel with the learner no matter where they keep their list.
- Keep **hours** on each goal (the hours system stays — it's good), assume **~2 h/day** and show elapsed calendar time inline where useful (e.g. `~20h ≈ 2 weeks at 2h/day`).
- A goal is "done" only when its **measurable gates pass AND its `can u explain it?` checkpoints pass** — not when the videos are watched, and not just because a box looks ticked in someone's fork. The number/lab is the hard bar; the explanation proves understanding.
- Keep prev/next nav and the ✅ exit check at the end of each goal group (rename "Exit check" is fine, keep the ✅).
- Preserve everything `CONTRIBUTING.md` requires: specific verified labs, cost tags, measurable gates, current exam codes, no salary/job-board data, HTTPS links.

---

## 4. Book + cert anchoring

- **Backbone book:** Stallings, *Computer Security: Principles and Practice*. Treat it as the fundamentals spine — it's hard but covers everything foundational. Map guide topics → its chapters in `read this + why`.
- **Every cert's domains map to topics — not just CC.** For *each* cert in the ladder (A+ 220-1201/1202, Network+ N10-009, **ISC2 CC**, Security+ SY0-701, and the specialization certs), the guide must make it **clear which topics cover which exam domains**. A learner should always be able to see "this todo group = these domains of this cert." Keep the `certifications.md` matrix (codes, ROI tiers) but add the domain→topic clarity on top.
- **CC is the fundamentals checkpoint.** Framing: *"if you can understand this Stallings chapter, you can answer the CC questions on it."* CC is the "you actually understood the fundamentals" gate, not a resume flex — but the same domain→topic clarity applies to all the others so the learner is never guessing what a cert tests. ⚠️ **CC is no longer free** (the "One Million Certified" free-voucher program closed 2026-05-20; exam now ~$199 + $50/yr AMF — see `research/_working/R2-isc2-cc-domains.md`). The *free* checkpoint is now the guide's own "can u explain it?" gates + practice tests; the paid exam is optional.
- Don't oversell certs. Same honest register the guide already has (`don't pay to prove what your resume shows`).

## 4b. CTF is woven in from day one — NOT a late phase

CTF (capture-the-flag) practice is **VERY IMPORTANT and starts while studying**, not parked at the end. The old guide buried CTFs in "Phase 3" — that's wrong for this rewrite.

- Introduce beginner-friendly CTF **early** (picoCTF, OverTheWire Bandit, TryHackMe beginner rooms) and keep a **running CTF thread** that grows alongside the topics — each fundamentals/cyber goal should suggest a CTF challenge that exercises what was just learned.
- Frame *why* early CTF matters in her voice: it turns passive reading into "can i actually DO this", it's low-stakes, it builds the "how could this break?" instinct the field runs on, and it's genuinely fun so it keeps momentum.
- CTF challenges double as `do this` labs and as `can u explain it?` proof — a solved challenge is evidence you understood the mechanism.
- Keep a clear **CTF progression** (absolute-beginner → beginner → intermediate) so a learner always has a next challenge at their level. Map challenges to the topic they reinforce.

## 4c. Cert study philosophy — study the TOPIC, the cert is a byproduct

Don't build cert-by-cert silos that make a learner "study for the exam." Build **topic clusters**; the exam is a checkpoint they pass *because* they understood the topic.

- **Merge certs that cover the same level.** ISC2 CC + Security+ are both security-fundamentals → **one merged study group**, not two. Teach the **union (superset)** of their topics — "no reason not to study more."
- **Label the deltas** so nobody's confused about what's on which exam: *"heads up: this bit is Security+ only, CC won't test it"*, *"CC-only"*, *"CCNA goes deeper here than Network+"*. A learner studying the superset should always know which cert each piece serves.
- **Every topic is tagged with the cert domain(s) it serves** — bidirectional with §4: from a topic you see its exam domains; from a cert (in `certifications.md`) you see which topic-groups cover it and in what order.
- **Frame it as "learn this because it's real + useful; you'll pass the exam because you get it,"** never "memorize this for the test." The cert is downstream of understanding (matches the north star: never lost, always know *why*).
- **File split (both, per the round-2 decision):** phase files (01/02/04…) carry the topic study + domain tags; `certifications.md` is the hub — data sheet + exam logistics + the study-order map (which topic-groups → which cert, in what order to be exam-ready).

---

## 5. A* research protocol (for research agents / fan-out)

Research is run as an **A\* search** toward the goal state "every fundamentals + cyber topic has verified mechanism-depth + Stallings mapping + a specific lab + a CC-alignment check." Do not blind-sweep.

- **Node** = one topic needing depth (e.g. "TLS handshake", "access control models").
- **g** = depth already banked for that node.
- **h (heuristic)** = *how foundational × how load-bearing for later topics*. Expand the node that unblocks the most downstream learning first → fundamentals before specialization, primitives before compositions.
- **Frontier** = ranked node list kept in `.agent/frontier.md`. After each round, re-rank and **stop to replan with the user** before widening scope.
- **Fan-out** = independent agents expand the top nodes in parallel; each returns: verified mechanism explanation, the correct vocab, Stallings chapter ref, one specific current lab (verify it's live), and the CC-domain it maps to. Cite sources; tag confidence `✅ verified / ⚠️ partial / ⛔ unverified` like the existing `research/` files do.
- Prefer `WebSearch`; if it's down, fall back to `curl` via Bash (the `research/` files were built this way before).
- Never mark a node done without the mechanism written out — a link alone is a fail.

## 5b. The OTHER 6 fields — LIGHT conversion only (no research round)

Cyber got the full treatment (deep mechanism research + cert study-paths) because it's the priority field. The other 6 fields — **software-development, cloud-devops, data-ai-analytics, it-support-networking, ux-design, product-management, it-management** — are **already good on content**. They do NOT get a research round. Scope for them is a **format + voice conversion only**:

1. **Phase → todo-tree** (§3): convert "Phase 0/1/2…" into the checkable goal→sub-goal→topic todo structure, same as cyber. Keep the existing hours, pace, and the ✅ exit checks.
2. **Minnn voice** (§1): rewrite prose in Calibrated Minnn. Keep all technical terms/tools/commands exactly correct.
3. **Source-specificity tidy** (§2b): where a resource is a bare channel/site, tighten to the specific playlist/module IF it's obvious from context — but **do NOT do a full link-verification research pass** (that was cyber-only). If a link's exact target isn't obvious, leave it and flag `⚠️ TODO verify` inline rather than inventing specificity.
4. **Keep the existing content, structure, and facts** — don't add mechanism depth, don't merge sections, don't re-scope. This is a re-skin (structure + voice), not a rewrite. Preserve each field's own 03/04/05 topic files as-is in meaning.
5. The full depth template (§2 mechanism / vocab / "can u explain it?") is **cyber-only** — do NOT force it onto these fields. Todo-tree + voice is enough.

---

## 6. Guardrails

- **Do not `git commit` or `git push`.** The maintainer commits manually. Just leave a clean working tree.
- Cyber + fundamentals get the full depth treatment; the other 6 fields get the **light conversion only** (§5b) — todo-tree + Minnn voice, no research, no forced depth template.
- Keep changes focused; match the surrounding file's structure so diffs stay readable.
- Everything ignored by `.gitignore` (agent scratch, `BUILD-BACKLOG.md`, `research/_working/`) is yours to write freely; everything else is learner-facing and held to this spec.
