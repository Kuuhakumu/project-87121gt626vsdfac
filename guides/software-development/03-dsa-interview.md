# 🧮 Phase 3: Data Structures, Algorithms & Interview Prep

> **~100 hrs total** · your pace, no deadline
> Goal: solve coding-interview problems with a clear method, and understand the formats you'll face. Run this **in parallel** with Phase 4/5 — don't wait until you're "done" learning.

[← Phase 2](02-core.md) · [Hub](README.md) · [Next: Phase 4 →](04-specialization.md)

---

## How much DSA do you actually need?

Depends on where you apply:

- **Big tech / well-funded startups:** heavy LeetCode-style screens. DSA is the gate. Budget the full 100 hours.
- **Most mid-size & non-tech companies:** lighter algorithmic bar, more take-homes and practical questions. You still need the fundamentals, but not 300 LeetCode problems.

> **The honest truth:** DSA grinding is a *filter-passing* skill, not your day job. Don't let it eat time you should spend building a portfolio (which is what actually gets most juniors hired). Aim for competent, not competitive-programmer.

---

## Core data structures & complexity (~40 hrs)

**Cover, in this order:**
- **Big-O notation** — time & space complexity, why it matters. This underpins everything.
- **Arrays & strings** — the most-tested category. Two pointers, sliding window.
- **Hash tables / maps / sets** — extremely common; the answer to a huge share of "optimize this" questions.
- **Stacks & queues** — including when a problem is secretly a stack problem.
- **Linked lists** — traversal, reversal, cycle detection (fast/slow pointers).
- **Recursion** — the call stack, base cases, and the recursion tree.

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| DSA roadmap | [roadmap.sh/datastructures-and-algorithms](https://roadmap.sh/datastructures-and-algorithms) | Visual ordered syllabus, mark topics done | **Free** |
| Easy problem sets | [LeetCode](https://leetcode.com/) | Solve by category (Arrays → Hashing → Linked Lists) | Free tier (150+) |
| Patterns practice | [HackerRank](https://www.hackerrank.com/) | Problem-Solving track, by topic | Free |
| Mentored exercises | [Exercism](https://exercism.org/) | Practice with human feedback | **Free** |

**Practice gate:** can explain the Big-O of your solution, and solve most LeetCode **Easy** array/hashing problems in under 25 minutes.

---

## Trees, graphs & algorithmic patterns (~40 hrs)

**Cover:**
- **Binary trees** — traversals (inorder/preorder/postorder), BFS vs DFS, depth/height.
- **Binary search** — on arrays *and* on an answer space (the part people miss).
- **Graphs** — adjacency list/matrix, BFS/DFS traversal. (Dijkstra/advanced is usually beyond entry level.)
- **Sorting** — understand merge sort & quicksort conceptually; know your language's built-in sort.
- **Dynamic programming** — entry-level forms only: Fibonacci, climbing stairs, coin change. Recognize the pattern; don't fear it.
- **Heaps / priority queues** — appears for "top-K" style problems.

### The pattern-based approach

Don't memorize 300 problems — learn the ~15 recurring **patterns** (two pointers, sliding window, fast/slow pointers, BFS/DFS, binary search, backtracking, top-K heap, dynamic programming). Most interview questions are a pattern in disguise.

| Resource | What it gives you | Cost |
|---|---|---|
| [Coding Interview University](https://github.com/jwasham/coding-interview-university) | The canonical free self-study syllabus (used to land FAANG with no degree) | **Free** |
| [NeetCode](https://neetcode.io/) | Curated problem list grouped by pattern + video explanations | Free tier |
| [LeetCode](https://leetcode.com/) | Work the patterns; aim for ~100–150 quality problems over quantity | Free tier |

**Practice gate:** comfortable with tree BFS/DFS, can implement binary search correctly from memory, and recognize when a problem is sliding-window or two-pointer.

---

## Interview formats & mock practice (~20 hrs)

### The formats you'll face

| Format | Where it's common | How to prep |
|---|---|---|
| **Behavioral / HR screen** | Nearly universal, usually first | STAR-format stories (see [interview-prep.md](interview-prep.md)) |
| **Live coding (DSA)** | Big tech, many startups | Talk out loud, clarify before coding, test your code |
| **Take-home project** | Startups, mid-size | Treat as production: tests, README, clean commits |
| **Technical phone screen** | Common second round | Often a medium DSA problem + light system questions |
| **Pair programming** | Companies skeptical of LeetCode | Practice thinking aloud and collaborating |
| **Junior system design** | Some mid+ roles | "Design a URL shortener / a todo API" — keep it concrete |

### Practice the *performance*, not just the answer

What live coding really tests is **communication under mild pressure**: clarify the question, state your approach, narrate as you code, test edge cases. Practice this explicitly.

| Tool | What you do | Cost |
|---|---|---|
| [Pramp](https://www.pramp.com/) | Free peer-to-peer mock interviews | **Free** |
| [LeetCode](https://leetcode.com/) | Timed mock assessments | Free tier |
| [CodeSignal](https://codesignal.com/) | The assessment format many employers actually use | Free practice |

**Practice gate:** completed at least **3 mock interviews** (peer or self-recorded), and can walk through a medium problem out loud without freezing.

---

## A note on AI tools in interviews

You may use AI tools daily while learning — but **most live interviews ban them**, and take-homes expect you to understand every line. Practice solving problems *without* AI so the underlying skill is solid. The 2026 bar is explicitly "prove you understand what you wrote." See the [AI section in Phase 0](00-prep.md).

---

## Phase 3 exit checklist
- [ ] Can analyze time/space complexity of your own code
- [ ] Solve LeetCode Easy reliably, many Mediums with effort
- [ ] Know the ~15 core patterns and recognize them
- [ ] Completed 3+ mock interviews
- [ ] Can explain a take-home's design decisions out loud

Next: [Phase 4 — Specialization Paths →](04-specialization.md)
