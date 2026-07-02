# Goal 1: foundations - first language, CLI, Git meow

> **~140h total** - your pace, no deadline.
> goal: real fluency in one language, comfort in the terminal, and Git as second nature.
> this is the floor everything else sits on.

[Previous: Goal 0](00-prep.md) - [Hub](README.md) - [Next: Goal 2](02-core.md)

---

- [ ] **choose one learning spine** (~5h setup)
- [ ] **core programming in your first language** (~70h)
- [ ] **command line + Git/GitHub** (~30h)
- [ ] **ship your first tiny projects** (~40h)
- [ ] **exit check** - language fluency, terminal comfort, Git reps, 2+ small repos

## choose one learning spine

pick **one** structured path and stick with it. dont hop between five tutorials every time one gets hard qwq.

| Path | Best for | Format | Cost |
|---|---|---|---|
| [The Odin Project](https://www.theodinproject.com/) | Full-stack JS or Ruby, local-first | Project-based, builds to GitHub | **Free** |
| [freeCodeCamp](https://www.freecodecamp.org/) | Browser-based start, JS/Python/SQL | ~300 challenges + projects | **Free** |
| [CS50x (Harvard)](https://cs50.harvard.edu/x/) | Strongest CS fundamentals | Lectures + problem sets (C -> Python -> SQL -> JS) | **Free** + free cert |
| [Full Stack Open](https://fullstackopen.com/en/) | Modern JS after basics | React/Node/REST, free certificate | **Free** |
| [Boot.dev](https://www.boot.dev/) | Backend (Python -> Go) | In-browser, gamified | Freemium |

CS50x is the strongest fundamentals on-ramp even if u plan web. the C weeks make memory and the call stack less mysterious later.

## core programming in your first language (~70h)

master these **before** a framework:

- [ ] variables and data types
- [ ] operators, conditionals, loops
- [ ] functions and scope
- [ ] arrays/lists, objects/dictionaries, strings
- [ ] error handling (`try`/`catch` or language equivalent)
- [ ] reading and writing files
- [ ] importing modules/packages
- [ ] debugging with stack traces, a debugger, or deliberate `print`/`console.log`
- [ ] regex basics with [regex101](https://regex101.com/)

then learn the beginner-to-hireable habits:

- [ ] break a problem into functions
- [ ] read errors before changing code randomly
- [ ] use clear names and small functions
- [ ] avoid copy-paste duplication when a function would do

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| Full curriculum | [freeCodeCamp](https://www.freecodecamp.org/learn) | ~300 in-browser challenges, JS or Python | Free |
| Language track | [Exercism](https://exercism.org/) | Exercises in 70+ languages with free human mentorship | Free |
| Kata practice | [Codewars](https://www.codewars.com/) | Bite-sized puzzles, read others solutions after | Free |
| Beginner challenges | [Edabit](https://edabit.com/) | Gamified micro-challenges before LeetCode | Freemium |

**practice gate:** solve a Codewars 7-6 kyu kata without a tutorial, and write a 50-line program from scratch, like a CLI calculator or text-based game.

## command line + Git/GitHub (~30h)

not optional. gaps here are red flags in interviews.

- [ ] **CLI:** `cd`, `ls`/`dir`, `pwd`, `mkdir`, `cp`, `mv`, `rm`, `cat`, `less`, `grep`, pipes, redirection, `ssh`, environment variables.
- [ ] **Git:** `init`, `add`, `commit`, `push`/`pull`, branches, merges, merge conflicts, `.gitignore`, pull requests, forks.
- [ ] **Git vs GitHub:** know the tool vs the hosted service.

### labs

| Lab | Platform | What u do | Cost |
|---|---|---|---|
| [Learn Git Branching](https://learngitbranching.js.org/) | Web | ~50 visual puzzles: commit, branch, merge, rebase | **Free** |
| [GitHub Skills](https://skills.github.com/) | GitHub | Guided courses inside real repos | **Free** |
| [The Missing Semester](https://missing.csail.mit.edu/) | MIT | Shell, vim, git, debugging - the stuff school skips | **Free** |
| [OverTheWire - Bandit](https://overthewire.org/wargames/bandit/) | Web | SSH into real Linux boxes, learn CLI by solving puzzles | **Free** |

**practice gate:** create a repo, branch, open a PR, resolve a merge conflict, and explain what a commit is without looking it up.

## ship your first tiny projects (~40h)

stop consuming and start building. two small projects, both on GitHub with a README.

- [ ] **CLI tool:** to-do manager, unit converter, password generator, file organizer.
- [ ] **small data script:** read a CSV, transform it, output a summary or chart.
- [ ] **text-based game:** hangman, tic-tac-toe, quiz.
- [ ] **simple API client:** fetch from a public API and display results.

each repo needs:

- [ ] `README.md`: what it does, how to run it, what u learned
- [ ] clean commit history, not one giant `final` commit
- [ ] `.gitignore`

these arent your portfolio centerpieces. they prove u can finish and ship. portfolio projects come in [Goal 5](05-portfolio.md).

## exit check

- [ ] fluent in one language: functions, errors, data structures without a tutorial
- [ ] comfortable in the terminal
- [ ] Git/GitHub is second nature: branch, PR, conflict resolution
- [ ] 2+ small projects on GitHub with READMEs
- [ ] can read a stack trace and debug methodically

[Next: Goal 2 - Core Web & Data Skills](02-core.md)
