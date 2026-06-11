# 📁 Phase 1: Foundations — First Language, CLI & Git

> **~140 hrs total** · your pace, no deadline
> Goal: real fluency in one language, comfort in the terminal, and Git as second nature. This is the bedrock everything else sits on.

[← Phase 0](00-prep.md) · [Hub](README.md) · [Next: Phase 2 →](02-core.md)

---

## How to work this phase

Pick **one** structured path as your spine and stick with it. Don't hop between five tutorials — pick one and finish it.

| Path | Best for | Format | Cost |
|---|---|---|---|
| [The Odin Project](https://www.theodinproject.com/) | Full-stack JS (or Ruby), local-first | Project-based, builds to GitHub | **Free** |
| [freeCodeCamp](https://www.freecodecamp.org/) | Browser-based start, JS/Python/SQL | ~300 challenges + projects | **Free** |
| [CS50x (Harvard)](https://cs50.harvard.edu/x/) | Strongest CS fundamentals | Lectures + problem sets (C→Python→SQL→JS) | **Free** + free cert |
| [Full Stack Open](https://fullstackopen.com/en/) | Modern JS after basics | React/Node/REST, free certificate | **Free** |
| [Boot.dev](https://www.boot.dev/) | Backend (Python→Go) | In-browser, gamified | Freemium |

> **CS50x is the single best fundamentals on-ramp** even if you plan to do web. The C weeks teach you what memory and the call stack actually are — knowledge that makes every later language click.

---

## Core programming in your first language (~70 hrs)

Whichever language you chose, master these **before** touching a framework:

**Cover:** variables & data types, operators, conditionals, loops, functions, scope, arrays/lists, objects/dictionaries, strings & string methods, error handling (try/catch), reading & writing files, importing modules, and basic debugging (reading stack traces, using a debugger or `print`/`console.log` deliberately).

**Then the concepts that separate beginners from hireable:**
- How to break a problem into functions
- Reading errors and debugging methodically (not random changes)
- Writing readable code: naming, small functions, no copy-paste duplication
- **Regex basics** — [regex101](https://regex101.com/) (free, interactive)

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| Full curriculum | [freeCodeCamp](https://www.freecodecamp.org/learn) | ~300 in-browser challenges, JS or Python | Free |
| Language track | [Exercism](https://exercism.org/) | Exercises in 70+ languages with **free human mentorship** | Free |
| Kata practice | [Codewars](https://www.codewars.com/) | Bite-sized puzzles, read others' solutions after | Free |
| Beginner challenges | [Edabit](https://edabit.com/) | Gamified micro-challenges before LeetCode | Freemium |

**Practice gate:** you can solve a Codewars 7–6 kyu kata without a tutorial, and write a 50-line program (e.g. a CLI calculator or a text-based game) from scratch.

---

## The command line & Git/GitHub (~30 hrs)

Not optional. Gaps here are red flags in interviews.

**CLI cover:** navigation (`cd`, `ls`/`dir`, `pwd`), file ops (`mkdir`, `cp`, `mv`, `rm`), viewing files (`cat`, `less`), `grep`, pipes & redirection, `ssh` basics, environment variables.

**Git cover:** `init`, `add`, `commit` (with good messages), `push`/`pull`, branching, merging, **resolving merge conflicts**, `.gitignore`, pull requests, forking. Understand the difference between Git (the tool) and GitHub (the host).

### Labs

| Lab | Platform | What you do | Cost |
|---|---|---|---|
| [Learn Git Branching](https://learngitbranching.js.org/) | Web | ~50 visual puzzles: commit, branch, merge, rebase | **Free** |
| [GitHub Skills](https://skills.github.com/) | GitHub | Guided courses inside real repos (PRs, Actions) | **Free** |
| [The Missing Semester](https://missing.csail.mit.edu/) | MIT | Shell, vim, git, debugging — the "stuff school skips" | **Free** |
| [OverTheWire — Bandit](https://overthewire.org/wargames/bandit/) | Web | SSH into real Linux boxes, learn CLI by solving puzzles | **Free** |

**Practice gate:** you can create a repo, branch, open a PR, resolve a merge conflict, and explain what a commit is — all without looking it up.

---

## Apply it — your first real projects (~40 hrs)

Stop consuming and start building. Two small projects, both on GitHub with a README.

**Project ideas (pick 2):**
- A **CLI tool**: a to-do manager, a unit converter, a password generator, a file organizer
- A **small data script**: read a CSV, transform it, output a summary or chart
- A **text-based game**: hangman, tic-tac-toe, a quiz
- A **simple API client**: fetch from a free public API (weather, GitHub, pokémon) and display results

**Each repo must have:**
- A `README.md`: what it does, how to run it, what you learned
- Clean commit history (not one giant "final" commit)
- A `.gitignore`

> These won't be your portfolio centerpieces — they prove you can finish and ship. The portfolio projects come in [Phase 5](05-portfolio.md).

---

## Phase 1 exit checklist
- [ ] Fluent in one language: can write functions, handle errors, manipulate data structures without a tutorial
- [ ] Comfortable in the terminal
- [ ] Git/GitHub is second nature (branch, PR, conflict resolution)
- [ ] 2+ small projects on GitHub with READMEs
- [ ] Can read a stack trace and debug methodically

Next: [Phase 2 — Core Web & Data Skills →](02-core.md)
