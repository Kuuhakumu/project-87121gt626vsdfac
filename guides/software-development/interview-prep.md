# 🎤 Interview Prep — Software Development

A question bank for entry-level SWE interviews. Covers the four rounds you'll actually face: **coding/DSA, language & web fundamentals, a practical/take-home, and behavioral.** See [Phase 3](03-dsa-interview.md) for how to *practice* coding rounds — this file is the question bank.

[← Hub](README.md) · [Phase 3: DSA & Interviews](03-dsa-interview.md)

---

## The rounds at a glance

| Round | What it tests | How to prep |
|---|---|---|
| Recruiter screen | Motivation, basics, communication | Know your resume cold; have a 60-sec intro |
| Coding / DSA | Problem-solving on data structures & algorithms | LeetCode patterns (Phase 3) |
| Technical / fundamentals | Language + web knowledge depth | This file + your projects |
| Take-home / practical | Real-world coding, clean structure | Ship something small and clean |
| Behavioral | Teamwork, communication, judgment | STAR stories (below) |

---

## 1. Coding round — how to behave (not just solve)

Interviewers are scoring *how you think*, not just whether you get the right answer:

1. **Clarify** — restate the problem, ask about input size, edge cases, constraints.
2. **Examples** — walk a small example by hand.
3. **Approach out loud** — state your plan and its Big-O *before* coding.
4. **Code while narrating** — explain as you type.
5. **Test** — walk through your code with the example, check edge cases.
6. **Optimize** — discuss how to improve time/space.

> Silence is the #1 killer. A talking candidate who doesn't finish often beats a silent one who does.

---

## 2. Language & fundamentals questions

### JavaScript / TypeScript
- What's the difference between `let`, `const`, and `var`?
- Explain `==` vs `===`.
- What is a closure? Give a use case.
- What is the event loop? Explain `async`/`await` vs callbacks vs Promises.
- What does `this` refer to, and how does it change?
- What problem does TypeScript solve? What are generics?
- Explain `map`, `filter`, `reduce`.

### Python
- List vs tuple vs set vs dict — when do you use each?
- What is a list comprehension? Give an example.
- Mutable vs immutable types — why does it matter?
- What are `*args` and `**kwargs`?
- How does Python handle scope (LEGB)?
- What is a decorator?

### Web fundamentals (any stack)
- What happens when you type a URL and press Enter? (DNS → TCP → HTTP → render — go as deep as you can)
- Explain the HTTP request/response cycle. Common status codes (200, 301, 400, 401, 403, 404, 500)?
- GET vs POST vs PUT vs PATCH vs DELETE?
- What is REST? What makes an API RESTful?
- What is CORS and why does it block requests?
- Cookies vs localStorage vs sessionStorage?
- Client-side vs server-side rendering — trade-offs?
- What is the DOM?

### Databases
- SQL vs NoSQL — when would you choose each?
- What is a JOIN? Explain INNER vs LEFT JOIN.
- What is an index and why does it speed up queries? What's the cost?
- What is a primary key vs a foreign key?
- What is a transaction? What does ACID mean?
- How do you prevent SQL injection? (parameterized queries / prepared statements)

### Git & tooling
- Difference between `git merge` and `git rebase`?
- How do you resolve a merge conflict?
- What is a pull request and what happens during code review?
- What goes in a `.gitignore` and why?

---

## 3. Practical / take-home

Common formats:
- "Build a small app/API that does X" (24–72 hrs)
- "Here's a buggy repo — fix it"
- "Add a feature to this existing codebase"

**What they look at:**
- Does it work and meet the requirements?
- Is the code readable and organized?
- Did you write tests?
- Is there a clear README (how to run it, decisions you made)?
- Git history that tells a story.

> Don't over-engineer. A clean, tested, working solution to exactly what was asked beats a sprawling half-finished framework.

---

## 4. Behavioral questions (STAR format)

Answer with **S**ituation → **T**ask → **A**ction → **R**esult. Prepare 5–6 stories from projects, study, work, or open source that you can flex to many questions.

**Common prompts:**
- Tell me about yourself. *(60-second story: where you came from, what you build, what you want next.)*
- Tell me about a project you're proud of. *(Have one ready — architecture, your decisions, what was hard.)*
- Describe a bug that took a long time to solve. How did you approach it?
- Tell me about a time you had to learn something new quickly.
- Describe a disagreement with a teammate. How did you handle it?
- Tell me about a time you failed or shipped something broken.
- How do you handle feedback on your code?
- Why software development? Why this company?

**Questions to ask them (always have 2–3):**
- What does a typical day look like for a junior here?
- How is code reviewed and shipped?
- What does growth/mentorship look like for juniors?
- What's the biggest challenge the team is facing?

---

## 5. The AI-tools question (new in 2026)

You may be asked how you use AI tools. The strong answer shows **judgment**, not avoidance or over-reliance:

- "I use Copilot/Cursor for boilerplate and first drafts, but I review every line — I've caught it generating subtly wrong logic and outdated APIs."
- Be ready to **explain any code in your portfolio**. "The AI wrote it" is a disqualifier. Understanding it is the skill.

---

## Quick-hit rapid fire

Things you should be able to answer in one sentence:
- Time complexity of binary search? *(O(log n))*
- Hash map average lookup? *(O(1))*
- What data structure for LIFO? *(stack)* FIFO? *(queue)*
- Difference between an array and a linked list?
- What is recursion? What's a base case?
- What is Big-O notation measuring?

---

## Final advice

- **Practice out loud.** Use [Pramp](https://www.pramp.com/) for free peer mock interviews.
- **Explain your projects** until it's effortless — most interviews lean on them.
- **It's a skill, not a verdict.** Interviewing improves with reps. Rejections are normal; keep going.

Good luck. → [Back to the hub](README.md)
