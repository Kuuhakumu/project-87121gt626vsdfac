# Shared Foundations — Hours 0–40

> **everyone starts here, no matter which field u pick.** these are the universal skills every IT career assumes u already have: how computers work, the command line, how the internet moves data, and how to actually learn technical material. do this *before* u commit to a field — by the end, the right path is usually obvious, and u havent lost anything if u change your mind meow

**Total: ~40 hours** (≈ 3–4 weeks at 2h/day). go at whatever pace fits your life — theres no deadline. everything here is **free** and **verified live (July 2026)**.

---

## how to track your progress meow

oki so u might notice all the `- [ ]` checkboxes below... heres the thing: **these boxes are display-only in this public repo** — u cant actually tick them here (youd have to commit to *our* repo which... doesnt make sense for your personal progress ;w;).

**so heres what to do instead:**
- **fork this repo** into your own GitHub account (button at the top) — then u can tick boxes in your fork and commit your progress there, or
- **copy the checklist into your own notes** — if youre using Obsidian or OneNote (we set those up in Block 4), just paste the checkbox tree into a page there and tick as u go, or
- **download/print it** — old school but it works meow

the `- [ ]` boxes in *this* repo are just the visual structure showing u the path. your *actual* progress is tracked by the **two-part gate system** that travels with u no matter where u keep your list:

1. **the measurable gate** (in each "do this" section) — real % on a named practice-test site, or a real interactive lab passed (like "clear Bandit 0–15" or "complete Week 1 problem set"). this is objective, unfoolable, external. either u hit the number or u didnt.

2. **the "can u explain it?" gate** (at the end of each topic) — proves u *understand why*, not just that u did the steps. out loud or written, unaided.

**both must pass** before a topic is really done. the measurable gate is the hard bar (it keeps u honest); the explain gate catches "i passed the quiz but couldnt tell u why it works" — which is exactly the gap this guide exists to close qwq

dw if that sounds intense — the gates are calibrated to hours-not-weeks, and the mechanism sections above each gate literally give u the map to pass the explain part. youve got this meow

---

## the path (todo-tree)

- [ ] **Block 1** — how computers actually work (~8h)
- [ ] **Block 2** — command line + operating system literacy (~12h)
- [ ] **Block 3** — how the internet works (~12h)
- [ ] **Block 4** — git, GitHub & how to learn (~8h)
- [ ] ✅ **Exit check** — pick your field

---

## Block 1 · How Computers Actually Work (~8h)

**the idea** — a running computer is a loop, not a magic box. the CPU repeats a fetch-decode-execute cycle; everything it touches lives in RAM (fast but clears on power loss), and gets loaded there from storage (slow but persistent).

**how it actually works** — lets talk about whats really happening when u "run a program", bc this is the bedrock everything else sits on:

A CPU repeats the **fetch–decode–execute cycle** from boot until shutdown:
1. **Fetch** — the **program counter (PC)** holds the memory address of the next instruction. that address is copied to the **memory address register (MAR)**, the value at that RAM address is pulled into the **memory data register (MDR)** and then the **current instruction register (CIR)**; the PC increments to point at the next instruction.
2. **Decode** — the **control unit** interprets the bits in the CIR: which operation, which operands/addresses.
3. **Execute** — the **ALU** (arithmetic logic unit) does the math/logic, or data is moved, or the PC is set to a new address (a jump/branch). then the loop repeats. modern CPUs overlap these steps via an **instruction pipeline** (next fetch starts before the previous execute finishes).

why RAM vs storage matters, physically: **RAM is volatile** — fast electrical cells the CPU can address directly, but they lose state when power is cut. **storage (SSD/HDD) is persistent** but far slower and *not* directly executable by the CPU. so "running a program" = the OS copies the programs instructions from storage into RAM, creates a **process** (its own address space + PC + registers state), and the CPU begins the fetch–decode–execute loop on those in-RAM instructions. that copy-into-RAM step is the entire reason more RAM lets u run more/bigger programs at once, and why an SSD mainly speeds *launch/load*, not raw compute. everything the CPU touches is ultimately **binary** — bits grouped into bytes — because the hardware is switches that are on/off (1/0).

dw if this feels abstract rn — the CS50 lab below makes it concrete meow

**words u gotta be able to say:**
- **CPU** — the chip that executes instructions in a fetch/decode/execute loop
- **fetch–decode–execute cycle** — the CPUs core repeat-loop per instruction
- **program counter (PC)** — register holding the address of the next instruction
- **register** — tiny ultra-fast storage inside the CPU (PC, MAR, MDR, CIR, etc.)
- **control unit** — decodes the instruction and directs the rest of the CPU
- **ALU** — arithmetic logic unit; does the actual math/logic
- **RAM (volatile)** — fast, directly-addressable memory that clears on power loss
- **storage / SSD / HDD (persistent)** — slower memory that survives power off
- **process** — a program loaded into RAM and running, with its own memory + register state
- **bit / byte** — smallest unit (1/0) / group of 8 bits
- **binary** — base-2; how all data/instructions are physically represented
- **clock speed / core** — cycles per second / independent execution unit

**study sources (pick what fits your style):**
- [CS50x Week 0–1](https://cs50.harvard.edu/x/) — the single best free "how computing works" intro; browser IDE, audit free. Week 0 = logic in Scratch, Week 1 = your first C program (this is also the lab below)
- [CrashCourse Computer Science playlist](https://www.youtube.com/playlist?list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo) — episodes 1–10 for the big-picture history + concepts; friendly, animated. **free**
- [Branch Education — "How does a CPU work?"](https://www.youtube.com/@BranchEducation) + "How do SSDs work?" — 3D animations showing the physical hardware; makes the fetch-execute cycle visual. **free**

**do this** — [CS50x Week 0–1](https://cs50.harvard.edu/x/) — browser IDE, no install. build logic in Scratch (Week 0), then write + run your first compiled C program (Week 1) so u *see* source → compile → a running process. ✅ verified live 2026-07-01

**measurable gate:** complete the **Week 1 problem set** (submit at least one working C program). this is the objective bar — either u built + ran a program or u didnt meow

**can u explain it?** ✅ — out loud or written, unaided (no notes, no guide open): *"Trace one instruction through fetch, decode, execute — name which register holds the next address. then explain why a program must be copied from storage into RAM before the CPU can run it, and what makes RAM different from an SSD."*

if u can do the measurable gate but stumble here, thats the signal to re-read the mechanism section above — the bar is "i understand the chain and can say why each piece exists," not "i memorized the words" qwq

---

## Block 2 · Command Line + Operating System Literacy (~12h)

**the idea** — the shell is a program that reads a line, parses it, and asks the OS kernel to do the work. learning to chain commands together (pipes, redirects, permissions) is how u actually control a system — and its the universal tool every IT field uses.

**how it actually works** — when u type `ls -l /etc` and press Enter: the shell splits the line into a **command + arguments**, resolves `ls` by searching each directory in your **`PATH`** environment variable, then calls the kernel to **`fork`** a new process and **`exec`** the `ls` binary into it. `ls` runs, writes to **standard output (stdout)**, and exits with a numeric **exit code** (0 = success).

the power comes from three OS mechanisms the shell wires together:
- **Streams & pipes** — every process has stdin/stdout/stderr. a **pipe `|`** connects one processs stdout to the nexts stdin (`grep`, `sort`, `wc` chain into a data pipeline); **redirects** `>`/`>>` send stdout to a file instead of the screen.
- **The filesystem is a tree** — one root `/`, **absolute paths** start at `/`, **relative paths** start from your current directory (`pwd`), `~` = home. everything (devices, config) is a file under it.
- **Permissions** — each file has read/write/execute bits for owner/group/other, shown as `rwxr-xr-x`. `chmod 755` sets them via **octal** (r=4, w=2, x=1 → 7=rwx, 5=r-x). this is *the* access-control primitive an attacker abuses or a defender hardens, which is why its fundamentals-critical.

`sudo` runs one command as **root** (the all-powerful uid 0); `ps`/`top` list processes; `kill` sends a signal to one by PID. dw this clicks faster once u start the Bandit lab below — real puzzles make it stick better than watching meow

**words u gotta be able to say:**
- **shell** — program that reads commands and asks the kernel to run them
- **kernel** — core of the OS that actually talks to hardware
- **PATH** — env var listing dirs the shell searches for a command
- **stdin / stdout / stderr** — a processs input / normal output / error output streams
- **pipe `|`** — connect one commands stdout to the nexts stdin
- **redirect `>` `>>`** — send output to a file (overwrite / append)
- **absolute vs relative path** — from `/` vs from current dir; `~` = home
- **permissions / `chmod` / octal (755, 644)** — read/write/execute bits per owner/group/other
- **process / PID / `kill`** — a running program / its id / send it a signal
- **root / `sudo`** — superuser / run one command with its privileges
- **environment variable** — named value the shell passes to programs
- **package manager (`apt`/`brew`/`winget`)** — installs software + dependencies

**study sources (pick what fits your style):**
- [The Missing Semester (MIT) — Lecture 1 (The Shell)](https://missing.csail.mit.edu/2020/course-shell/) + [Lecture 2 (Shell Tools)](https://missing.csail.mit.edu/2020/shell-tools/) — genuinely the best CLI intro; text + video, with exercises. **free**
- [Linux Journey](https://linuxjourney.com/) — self-paced interactive text lessons on command line, file system, permissions. **free**
- [Professor Messer — CompTIA A+ 220-1102 playlist, OS sections](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/220-1102-training-course/) — covers Windows + Linux OS basics; CompTIA-focused but solid fundamentals. **free**
- [NetworkChuck — "you need to learn Linux RIGHT NOW!!"](https://www.youtube.com/watch?v=ROjZy1WbCIA) — energetic 30min walkthrough of essential commands. **free**

**do this** — [OverTheWire — Bandit, Levels 0–15](https://overthewire.org/wargames/bandit/) — SSH into a real Linux box and solve each level with `ssh`, `ls`, `cat`, `find`, `grep`, `base64`, etc. real target, real skills. ✅ verified live 2026-07-01

this is also your **first CTF experience** — capture-the-flag puzzles where u find a hidden "flag" (password) to unlock the next level. theyre genuinely fun and theyre how the industry actually practices, so starting here means ur building the right instincts from day one meow

**measurable gate:** clear **levels 0–15 unaided.** that single run proves genuine CLI competence (nav, files, search, permissions, ssh). either u solved them or u didnt — this is the hard bar.

**can u explain it?** ✅ — out loud or written, unaided: *"Type `cat notes.txt | grep TODO | wc -l` — explain what each `|` does to the data, what stdout is, and what `chmod 640 notes.txt` would let the owner vs others do."*

if u can clear Bandit 0–15 but stumble here, re-read the streams/pipes/permissions part above. both gates must pass qwq

---

## Block 3 · How the Internet Works (~12h)

**the idea** — typing a URL kicks off a fixed sequence: name→IP lookup, handshake to connect, encryption handshake to secure it, then the actual request/response — each step exists for a reason.

**how it actually works** — lets trace what happens when u press Enter on **`https://example.com`**, bc every piece of this shows up in security/cloud/dev work later:

1. **DNS resolution** — the name means nothing to the network; routing needs an IP. the OS asks a **recursive resolver**, which (if uncached) walks the hierarchy: **root** nameserver → **TLD** nameserver (`.com`) → **authoritative** nameserver for `example.com`, which returns the **A record** (IPv4) or **AAAA** (IPv6). results are **cached** with a **TTL** so its fast next time.

2. **TCP three-way handshake** — before any data, the client and server establish a reliable, ordered connection on **port 443**: **SYN → SYN-ACK → ACK**. this synchronizes sequence numbers so lost/reordered packets can be detected and retransmitted — TCP gives *reliability* that IP alone doesnt.

3. **TLS handshake** — now they secure the channel. client sends **ClientHello** (supported cipher suites, random); server replies **ServerHello** + its **digital certificate**. the client validates the cert against a trusted **certificate authority (CA)** — this authenticates *that the server is really example.com* and stops an impostor. they then agree on a shared **symmetric session key** (in TLS 1.3 via an ephemeral Diffie-Hellman key exchange, one round trip). all further traffic is encrypted+authenticated with that key. thats *why* HTTPS stops a **man-in-the-middle** from reading (confidentiality) or silently altering (integrity) the traffic. dw this clicks more when u hit the crypto block in cybersecurity meow

4. **HTTP request/response** — over the encrypted channel the browser sends `GET / HTTP/1.1` (a **method** + path + **headers**); the server returns a **status code** (200 OK, 404, 500) + headers + the HTML body.

5. **render** — the browser parses HTML, fetches referenced CSS/JS/images (often reusing the connection), builds the DOM, and paints the page.

underneath, everything is **packets** routed hop-by-hop by IP; the **OSI/TCP-IP layers** just name who does what (app=HTTP, transport=TCP/port, network=IP, etc.). ports let one machine run many services (80 HTTP, 443 HTTPS, 22 SSH, 53 DNS, 25 SMTP).

**words u gotta be able to say:**
- **DNS / recursive resolver / root / TLD / authoritative** — name→IP lookup and its hierarchy
- **A / AAAA / CNAME / MX record** — IPv4 / IPv6 / alias / mail-server records
- **TTL / cache** — how long a DNS answer is reused
- **IP address / IPv4 / IPv6 / public vs private** — the numeric address of a host
- **port** — numeric channel id so one host runs many services (443, 80, 22, 53, 25)
- **TCP three-way handshake (SYN/SYN-ACK/ACK)** — sets up a reliable connection
- **packet** — the unit data is chopped into and routed
- **TLS handshake / ClientHello / cipher suite** — negotiating a secure channel
- **certificate / certificate authority (CA)** — proves the servers identity
- **symmetric session key** — shared secret that encrypts the actual traffic
- **man-in-the-middle (MITM)** — attacker between u and the server
- **confidentiality / integrity** — cant-read / cant-alter guarantees of TLS
- **HTTP method / status code / header** — GET/POST / 200-404-500 / metadata
- **OSI model / TCP-IP model** — layered map of network responsibilities

**study sources (pick what fits your style):**
- [Professor Messer — Network+ N10-009 playlist, "Network Concepts" section](https://www.professormesser.com/network-plus/n10-009/n10-009-video/n10-009-training-course/) — OSI model, TCP/IP, DNS, ports explained clearly; exam-focused but excellent fundamentals. **free**
- [PowerCert Animated Videos — "OSI Model Explained"](https://www.youtube.com/watch?v=vv4y_uOneC0) + ["TCP/IP Model Explained"](https://www.youtube.com/watch?v=OTwp3xtd4dg) + ["DNS Explained"](https://www.youtube.com/watch?v=mpQZVYPuDGU) — short (5–10min), visual, gets the concepts across fast. **free**
- [howdns.works](https://howdns.works/) — friendly comic walkthrough of DNS resolution; makes the root→TLD→authoritative chain concrete. **free**
- [TryHackMe — "Wireshark: The Basics" room](https://tryhackme.com/room/wiresharkthebasics) — load real packet captures, filter traffic, see TCP handshakes + HTTP live (freemium, this specific room is free). **freemium**

**do this** — run these two commands in your own terminal (works on Linux/Mac/WSL; Windows users can use Git Bash or WSL):
- `curl -v https://example.com` — watch the whole chain happen live (DNSd IP, TCP connect to :443, TLS negotiation, GET request, 200 OK response)
- `dig example.com` — see the A record DNS returns

zero signup needed, u literally watch steps 1–4 happen in real time. ✅ verified live 2026-07-01

**measurable gate:** run both commands successfully and **annotate the `curl -v` output line-by-line** — mark which lines are DNS, which are TCP handshake, which are TLS negotiation, which are the HTTP request/response. save this annotated copy (youll need it for the explain gate). this is the objective bar — either u can map the output or u cant meow

**can u explain it?** ✅ — this is the SECOND gate, on top of the measurable one above (both must pass). the annotated curl output proves u can *map* it; this proves u *understand why*:

out loud or written, unaided: *"Narrate every step from pressing Enter on `https://example.com` to the page appearing — DNS resolution → TCP SYN/SYN-ACK/ACK → TLS handshake (what the certificate proves, what the session key does) → HTTP GET/200 → render. say **why** TLS stops a man-in-the-middle."*

if u can do the measurable gate but stumble here, re-read the mechanism section above — the bar is "i understand the chain and can say why each piece exists" qwq

---

## Block 4 · Git, GitHub & How to Learn (~8h)

**the idea** — Git is how the whole industry tracks work and collaborates; GitHub is your public portfolio (its what gets u hired, especially without a degree). and knowing *how to learn* technical material is the meta-skill that determines whether ull finish any of these guides.

**how it actually works (Git)** — Git is a **content-addressed snapshot store**, not a diff tracker. key mechanism: every time you commit, Git basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. and everything in Git is checksummed before it is stored using a **SHA-1 hash** — so the same content = same hash, and any tampering changes the hash → **integrity**.

so the flow has a precise meaning:
- Your files live in the **working directory**. `git add` copies a files current version into the **staging area (index)** — "marked to go into the next commit snapshot."
- `git commit` writes a new **commit object**: a snapshot of the staged tree + author/message + a pointer to its **parent commit**. its identity is a SHA-1 hash of its contents. the chain of parent pointers *is* your history.
- A **branch** is just a lightweight movable pointer to a commit; committing advances it. **HEAD** points at your current branch. **merging** two branches replays their histories to a common **base**; a **merge conflict** is Git saying "both branches changed the same lines — a human must choose."
- A **remote** (e.g. GitHub) is another copy of the repo. `git push` uploads your new commit objects; `git pull` = `fetch` + `merge` others commits. because every commit carries its parent + hash, distributed copies can always be reconciled.

**how to learn (the meta-skill)** — memory strengthens by **active retrieval** and **spaced repetition** — recalling a fact just before youd forget it resets the forgetting curve (why Anki works for ports/commands). **active > passive** because doing a lab forces retrieval + error-correction that watching cant. the **build-to-learn loop** (learn → immediately apply in a tiny project → document) converts fragile recognition into durable recall; rebuilding a tutorial *without* following along is the test that u actually encoded it (escaping "tutorial hell"). dw this is the pattern this whole guide already uses — the two-gate system is literally active retrieval meow

**words u gotta be able to say:**
- **repository (repo)** — the tracked project + its full history
- **working directory / staging area (index)** — your live files / whats queued for the next commit
- **commit** — an immutable snapshot + parent pointer, named by its hash
- **SHA-1 hash / checksum** — content fingerprint giving Git its integrity
- **branch / HEAD** — movable pointer to a commit / pointer to your current branch
- **merge / merge conflict** — combine histories / when the same lines diverged
- **remote / `push` / `pull` / `clone`** — another copy / upload / download+merge / copy a repo
- **`add` / `commit` / `init`** — stage / snapshot / start a repo
- **pull request (PR)** — proposed merge on GitHub, reviewable
- **README / Markdown** — the repos front page / its lightweight markup
- **spaced repetition / active recall** — retrieve-before-forgetting; the study mechanism
- **build-to-learn / tutorial hell** — apply-immediately loop / passive-copy trap

**study sources (pick what fits your style):**
- [GitHub Skills](https://skills.github.com/) — interactive guided exercises inside GitHub itself (real repos, real PRs); "Introduction to GitHub" is the starting module. **free**
- [The Odin Project — Git Basics](https://www.theodinproject.com/lessons/foundations-git-basics) — text-based walkthrough with exercises; also covers the why behind version control. **free**
- [freeCodeCamp — "Git and GitHub for Beginners - Crash Course" (YouTube)](https://www.youtube.com/watch?v=RGOj5yH7evk) — 1hr video covering the essentials with live demos. **free**
- [Learn Git Branching](https://learngitbranching.js.org/) — visual interactive game (this is also the lab below); makes branches + merges click. **free**

for the "how to learn" part:
- [Anki](https://apps.ankiweb.net/) — free spaced-repetition flashcard app; use it for memorizing ports, commands, acronyms
- [Obsidian](https://obsidian.md/) — free markdown note-taking app with graph view; perfect for building a searchable second brain

**do this** — [Learn Git Branching](https://learngitbranching.js.org/) — visual, interactive: u type real `git commit`/`branch`/`merge`/`rebase` and *watch* the commit graph + branch pointers move — makes the "branch = pointer, commit = snapshot with a parent" mechanism concrete. ✅ verified live 2026-07-01

**measurable gate:** complete the main sequence (Introduction + Ramping Up sections), AND have a **GitHub account with ≥1 repo that has a real README**, and be able to `git add`/`commit`/`push` from the CLI without looking it up. these are the objective bars — either u did them or u didnt meow

**can u explain it?** ✅ — out loud or written, unaided: *"Explain what `git add` then `git commit` actually stores (staging → a hashed snapshot with a parent pointer), why two identical file states produce the same hash, and what a branch really is. then: what makes a merge conflict, and why is `push` safe across many copies?"*

if u can do the measurable gate but stumble here, re-read the mechanism section above. both must pass qwq

---

## ✅ exit check — youre done with foundations. now choose.

by now u can use a terminal, u understand how computers and the internet work, and u have a GitHub account. youve probably also noticed which blocks u actually *enjoyed*:

- **loved the CLI puzzles and "how could this break?"** → [Cybersecurity](../guides/cybersecurity/)
- **loved building logic in CS50** → [Software Development](../guides/software-development/)
- **loved networking + wanting things to run reliably** → [Cloud & DevOps](../guides/cloud-devops/) or [IT Support & Networking](../guides/it-support-networking/)
- **loved finding patterns in data** → [Data, AI & Analytics](../guides/data-ai-analytics/)
- **loved helping and explaining** → [IT Support & Networking](../guides/it-support-networking/)
- **cared most about how it *feels* to use** → [UI/UX Design](../guides/ux-design/)
- **liked deciding *what* to build and *why*, and coordinating people** → [Product Management](../guides/product-management/) *(usually a second job, not a first)*

still torn? take the [Career-Match Quiz](career-quiz.md) or re-read [what each field actually is](what-is-each-field.md).

> **whichever u pick, none of this time was wasted.** every field guide builds directly on these four blocks — they assume u can already do everything above meow

---

*Back to: [Start Here](README.md) · [What Each Field Is](what-is-each-field.md) · [Career Quiz](career-quiz.md)*
