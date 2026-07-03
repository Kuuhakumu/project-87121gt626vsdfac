# goal 3: scripting, logs & CTF level-up meow (~100h)

> **goal:** get automation-literate, learn how defenders query logs, and turn CTF into your running practice hub.
>
> **pace:** ~100 hours total ~= 7 weeks at 2h/day. CTF is woven through the work, not saved for the end.
>
> **practice note:** this goal quietly strengthens the automation/logging knowledge that exams and SOC labs both assume, but the work is scripts, queries, logs, and CTF reps.

[<- Goal 2: Networking & Security Core](02-core.md) | [Back to hub](README.md) | [Next: Specialization Paths ->](04-specialization.md)

---

## read this first meow

scripting is not "become a software engineer."

for security, scripting means:

- read a script without panicking
- automate repeat work
- parse logs into useful fields
- call APIs to enrich indicators
- write small tools when the manual way is too slow

thats it. small tools, clear output, no mystery.
dw its not as scary as it looks qwq

also: CTF already started back in [Prep](00-prep.md), [Foundations](01-foundations.md), and [Core](02-core.md).
this file turns it into the **level-up hub** so u always know the next legal, safe thing to break.

---

## how to track your progress meow

the `- [ ]` boxes here are display-only in this public repo.
fork the repo, or copy this checklist into Obsidian/OneNote, if u want boxes u can actually tick.

the real progress signal is always:

1. **measurable gate** - a real script, solved lab, saved report, or solved CTF challenge.
2. **can u explain it?** - out loud or written, unaided, naming the mechanism.

both must pass before the topic is really done.
a checkbox alone doesnt mean anything meow

---

## the path (todo-tree)

- [ ] **Block 1 - Python for security** (~40h): sockets, files, APIs, `requests`, `re`, JSON/CSV, small scanners and parsers.
- [ ] **Block 2 - PowerShell for Windows security** (~15h): cmdlets, object pipeline, `Get-WinEvent`, remoting shape, Century wargame.
- [ ] **Block 3 - KQL for Microsoft Sentinel / Defender / ADX** (~8h): table pipelines over columnar log stores.
- [ ] **Block 4 - SPL for Splunk** (~7h): indexed event search, schema-on-read, `stats`, `eval`, `rex`, reports.
- [ ] **Block 5 - regex + log parsing** (~5h): finite-automaton pattern matching, capture groups, field extraction.
- [ ] **Block 6 - CTF level-up hub** (~25h running thread): beginner -> intermediate ladder, writeups, topic-to-challenge map.
- [ ] **exit check** - can build small tools, query logs, explain the pipeline, and keep a CTF/writeup habit without getting lost.

---

## why this exists meow

this goal is mostly skill-building.
it turns theory into "i can automate it, query it, parse it, and explain what happened."

that matters in every lane:

- Python glues tools together and makes scanning/parsing less manual.
- PowerShell is how Windows admins, defenders, and attackers all touch Windows systems.
- KQL and SPL are how SOC work turns raw logs into answers.
- regex is how messy text becomes fields u can search.
- CTF keeps the "can i actually do it?" thread alive while the tooling grows.

for now, learn the thing because its real mhm

---

## block 1 - Python for security (~40h)

### Python as security glue meow (~40h)

**the idea** - Python is the field's glue language: enough to read code, automate boring repeat tasks, and stitch tools together.

**how/why it actually works** - when a Python script "talks to the network," it is not magic.
`socket.socket(AF_INET, SOCK_STREAM)` asks the OS for a **socket** handle: one endpoint made from an IP address plus a port.
`connect((ip, port))` makes the kernel do the TCP three-way handshake: SYN -> SYN-ACK -> ACK.
after that, `send()` copies bytes into the kernel buffer, and TCP handles segmentation, retransmits, ordering, and timeouts.
a port scanner is just that loop repeated: connect works = open, reset = closed, no reply/timeout = filtered.
`requests.get()` is the same stack one layer up: open TCP/TLS, write HTTP, read status/headers/body, parse it for u.

when a script parses a file, `open()` gives Python a file handle, bytes come off disk into a buffer, bytes decode into text, then string logic or `re` turns messy lines into fields.
security automation is usually this chain: parse -> filter -> count -> enrich -> output JSON/CSV.
thats why a tiny script can turn 10,000 auth lines into "these 5 IPs failed logon the most" meow

**words u gotta be able to say**

- **socket** - network endpoint, usually IP + port
- **file descriptor / handle** - OS reference to I/O resource
- **TCP three-way handshake** - SYN/SYN-ACK/ACK connection setup
- **open / closed / filtered** - scanner result meanings
- **stdlib vs PyPI** - built-in modules vs installed packages
- **`requests`** - Python HTTP client library
- **API / REST** - service interface over HTTP + JSON
- **IOC** - indicator of compromise
- **encoding** - bytes-to-text mapping
- **parsing** - messy input into structured fields

**study sources (pick what fits your style)**

- [Ryan John - "Python for Hackers FULL Course | Bug Bounty & Ethical Hacking"](https://www.youtube.com/watch?v=XWuP5Yf5ILI) - code-along course for sockets, `requests`, and small security tools. **free**
- [freeCodeCamp - "Full Ethical Hacking Course"](https://www.youtube.com/watch?v=3Kq1MIfTWCE) - broad explore-more path if u want the bigger offensive context around the scripts. **free**
- [RegexOne](https://regexone.com/) - use this when the `re` parts start looking like keyboard noise. **free**
- [regex101](https://regex101.com/) - live tester + explanation pane for debugging Python-style regex. **free**

**paid optional, not required:** [TCM Security - "Python 101 for Hackers"](https://academy.tcm-sec.com/p/python-101-for-hackers) is **paid** through TCM's membership. dont call it free, and dont buy it unless u specifically want that format.

**do this** - build two small tools in a GitHub repo:

1. a `socket`-based port scanner that scans ports **1-1024** on a target u own or have explicit permission to test, then writes open ports to CSV.
2. an auth-log parser that uses `re` to print the top 5 source IPs by failed-login count, then writes JSON or CSV.

**measurable gate:** both scripts run clean on fresh input, the repo has a README with usage examples, and the scanner never targets systems u dont own or have permission to test.

**CTF thread:** solve **OverTheWire Bandit level 24** from [Bandit](https://overthewire.org/wargames/bandit/) by scripting the repeated network interaction. then solve 3 **picoCTF / CyLab Security Academy** General Skills or scripting-style challenges at [cylabacademy.org](https://cylabacademy.org/) (catalog/login-driven). picoCTF is now hosted as CyLab Security Academy, but the name still matters because most writeups and teachers still call it picoCTF.

**can u explain it?** ✅ - unaided, explain what your scanner does when it hits an open port vs a closed port:
what function asks the OS for the socket, what packet handshake happens, what result your code sees, and why timeout does not mean the same thing as "closed."

---

## block 2 - PowerShell for Windows security (~15h)

### PowerShell object pipeline meow (~15h)

**the idea** - PowerShell is the automation language of Windows and Active Directory, so defenders and attackers both use it constantly.

**how/why it actually works** - the key thing is **objects, not text**.
Bash-style pipes usually pass strings, so every stage has to cut text back apart with `grep`, `awk`, or `sed`.
PowerShell pipes **.NET objects** with real properties and methods.
`Get-Process | Where-Object CPU -gt 100 | Select-Object Name, Id` filters on actual `.CPU` and `.Id` fields, not fragile column spacing.
cmdlets use a discoverable `Verb-Noun` pattern like `Get-WinEvent`, `Get-Service`, `Stop-Process`.
`Get-Member` shows what properties an object has, which is how u learn the next pipe stage.

remoting matters too: **WinRM / PSRemoting** lets `Invoke-Command` run a scriptblock on another host and return objects.
that is how admins manage many Windows systems, and also why attackers love PowerShell for living-off-the-land movement.
defenders answer that with script-block logging, AMSI, event logs, and tight privileges.
same tool, two sides, mhm

**words u gotta be able to say**

- **cmdlet** - `Verb-Noun` PowerShell command
- **object pipeline** - passes typed records, not raw text
- **property / method** - data / action on an object
- **`Get-Member`** - shows object properties and methods
- **`Get-WinEvent`** - queries Windows event logs
- **WinRM / PSRemoting** - remote command execution channel
- **script-block logging** - logs PowerShell code blocks
- **AMSI** - antimalware scanning interface
- **living off the land** - abusing built-in trusted tools

**study sources (pick what fits your style)**

- [Microsoft Learn - "Introduction to PowerShell"](https://learn.microsoft.com/en-us/training/modules/introduction-to-powershell/) - soft entry if PowerShell is new. **free**
- [Microsoft Learn - "Get started with Windows PowerShell"](https://learn.microsoft.com/en-us/training/paths/get-started-windows-powershell/) - verified 3-module path on command syntax, cmdlets, `Get-Help`, and discovery. **free**
- [Under the Wire - Century](https://underthewire.tech/century) - PowerShell wargame, like Bandit but inside a Windows/PowerShell shell over SSH. **free**

**do this** - finish the Microsoft Learn path, then write a script that pulls the last 20 failed logon records from the Security log:

- use `Get-WinEvent`
- filter for **Event ID 4625**
- project `TimeCreated`, source IP, and target account
- export to CSV or HTML

then clear **Under the Wire Century levels 0-10** unaided.

**measurable gate:** the script runs on a Windows machine where Security logs are available, the output file opens cleanly, and Century 0-10 are solved without copy-pasting a walkthrough.

**can u explain it?** ✅ - unaided, explain why piping objects is more reliable than text slicing, then explain why PowerShell is useful to both an admin and an attacker.

---

## block 3 - KQL for Microsoft Sentinel / Defender / ADX (~8h)

### KQL log hunting meow (~8h)

**the idea** - KQL is the read-only query language used to hunt through Microsoft security telemetry in Sentinel, Defender, and Azure Data Explorer.

**how/why it actually works** - KQL is a left-to-right **tabular pipeline**.
u start with a table like `SecurityEvent`, then each `|` operator takes a table in and emits a table out.
the common detection shape is `table | where suspicious condition | summarize count() by entity | sort | project useful columns`.
the backend is a **columnar, append-only store**, which means scanning one column across a huge number of log rows is fast.
that fits security telemetry perfectly because logs are mostly time-stamped events, and analysts usually ask "show me these rows in this time range, then count/group them."

KQL is read-optimized and does not mutate the audit trail.
thats exactly what u want in a SIEM: ask sharp questions, preserve evidence, dont change the data while investigating.

**words u gotta be able to say**

- **table** - typed rows and columns of events
- **operator** - one `|` pipeline stage
- **`where`** - filter rows
- **`project`** - choose output columns
- **`summarize`** - aggregate rows into counts/groups
- **`join`** - correlate two tables
- **columnar store** - stores/scans data by column
- **time-series telemetry** - timestamped event data
- **threshold detection** - alert when count crosses a line

**study sources (pick what fits your style)**

- [Microsoft Learn - "Write your first query with Kusto Query Language"](https://learn.microsoft.com/en-us/training/modules/write-first-query-kusto-query-language/) - beginner entry for `take`, `project`, `where`, `count`, and `sort`. **free**
- [Microsoft Learn - "Create queries for Microsoft Sentinel using KQL"](https://learn.microsoft.com/en-us/training/paths/sc-200-utilize-kql-for-azure-sentinel/) - SOC-focused path with 4 modules. **free**
- [Microsoft Learn - "Construct KQL statements for Microsoft Sentinel"](https://learn.microsoft.com/en-us/training/modules/construct-kusto-query-language-statements/) - exact first Sentinel KQL module if u want a smaller step. **free**
- [Kusto Detective Agency](https://detective.kusto.io/) - KQL puzzle cases with badges. **free**
- [KC7 - KQL 101](https://kc7cyber.com/go/take10) - beginner cyber investigation module using KQL/ADX. **free**

**do this** - complete the first-query module, then do one hands-on KQL game path:

- **option A:** solve Kusto Detective Agency onboarding + Case 1.
- **option B:** complete KC7 "KQL 101" + its first scenario.

in the sandbox, write a failed-logon query shaped like:

```kusto
SecurityEvent
| where EventID == 4625
| summarize count() by Account
| sort by count_ desc
```

adjust table/column names to the dataset u are using.

**measurable gate:** one KQL game path is solved, and u save one failed-logon style query where each pipe stage has a one-line comment explaining what it transforms.

**can u explain it?** ✅ - unaided, walk through each `|` stage in a failed-logon detection and explain why a columnar store makes this kind of query fast over huge logs.

---

## block 4 - SPL for Splunk (~7h)

### SPL search pipeline meow (~7h)

**the idea** - SPL is Splunk's search language: same broad idea as KQL, but in Splunk's indexed event world.

**how/why it actually works** - an SPL search begins by narrowing events, usually with `index=...`, a sourcetype, keywords, and a time range.
Splunk indexes ingested machine data by time and keywords, so the leading search cuts billions of events down to a working set.
then pipe commands transform that set: `stats` aggregates, `eval` computes fields, `rex` extracts fields with regex, `table` shapes output, `sort` orders it.

Splunk is **schema-on-read**.
that means fields can be extracted when u search, instead of requiring a perfect schema before logs arrive.
messy logs still become useful because `rex` or field extractions can say "this chunk is the client IP, this chunk is the status code."
that is why regex sits under SPL too.

**words u gotta be able to say**

- **SPL** - Splunk Search Processing Language
- **index** - searchable time/keyword event store
- **sourcetype** - label for a data format
- **schema-on-read** - fields parsed at search time
- **`stats`** - aggregate results
- **`eval`** - compute a field
- **`rex`** - regex field extraction
- **pipeline command** - one `|` transformation stage

**study sources (pick what fits your style)**

- [Splunk Search Tutorial](https://help.splunk.com/en/splunk-enterprise/get-started/search-tutorial/9.1/introduction/about-the-search-tutorial) - official hands-on tutorial with sample data, searches, reports, and dashboards. **free**
- explore more -> [Splunk Free Training Courses](https://www.splunk.com/en_us/training/free-courses/overview.html) - official free eLearning catalog. **free**
- [Splunk - "Intro to Splunk" eLearning](https://education.splunk.com/course/intro-to-splunk-elearning) - free but account-gated; use if u want a course wrapper. **free with account**
- [Splunk BOTS v3 dataset](https://github.com/splunk/botsv3) - open-source Boss of the SOC dataset for blue-team CTF practice. **free**

**do this** - complete the Search Tutorial's search + reporting sections.
on the tutorial data, write an SPL search that counts events by `status` or `clientip`, sorts descending, and saves as a report.

example shape:

```spl
index=main sourcetype=access_combined
| stats count by status
| sort -count
```

adjust index/sourcetype to the tutorial data u loaded.

**measurable gate:** the saved report opens in Splunk and the SPL query has a one-line note for what the base search, `stats`, and `sort` each do.

**CTF stretch:** load [Splunk BOTS v3](https://github.com/splunk/botsv3) and answer 5 investigation questions with your own SPL searches. this is stretch, not a blocker if ur still new to Splunk.

**can u explain it?** ✅ - unaided, explain what `index=` does before the first pipe, why `schema-on-read` is useful for messy logs, and how `rex` turns a raw log line into fields.

---

## block 5 - regex + log parsing meow (~5h)

### regex as the pattern engine meow (~5h)

**the idea** - regex is a small pattern language for finding and extracting text; it powers Python `re`, KQL `extract`, SPL `rex`, `grep -E`, and lots of detection logic.

**how/why it actually works** - a regular expression describes a set of strings.
the engine compiles the pattern into a **finite automaton**, then walks the input character by character, moving between states.
if the engine reaches an accepting state at the right point, it has a match.
thats why regex can scan huge logs efficiently: one forward pass can answer "does this line fit the pattern?"

the pieces are small but powerful:
character classes like `\d`, `\w`, `\s`, `[a-f]`; quantifiers like `*`, `+`, `?`, `{2,4}`; anchors like `^`, `$`, `\b`; alternation like `cat|dog`; and capture groups like `(?P<ip>...)`.
capture groups are the security part: they dont just say "matched," they pull out the IP, timestamp, username, hash, URL, or status code.
be careful with greedy `.*`; it grabs as much as possible and is the classic "why did my regex eat the whole line" bug ;w;

**words u gotta be able to say**

- **regex / pattern** - text-matching expression
- **finite automaton** - state machine used for matching
- **character class** - set of possible characters
- **quantifier** - how many repeats to match
- **anchor** - position constraint like start/end
- **capture group** - extracts a matched sub-piece
- **greedy vs lazy** - max vs minimum match
- **field extraction** - raw log -> named fields
- **tokenize** - split text into useful pieces

**study sources (pick what fits your style)**

- [RegexOne](https://regexone.com/) - step-by-step interactive lessons. **free**
- [regex101](https://regex101.com/) - live regex tester with token explanations and a match view. **free**
- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/) - use the grep/search levels as real noisy-text practice. **free**
- [Ryan John - "Python for Hackers FULL Course"](https://www.youtube.com/watch?v=XWuP5Yf5ILI) - revisit the parsing sections when u connect regex back to Python scripts. **free**

**do this** - finish all RegexOne lessons.
then on regex101, write one pattern with named capture groups that extracts:

- source IP
- timestamp
- HTTP status

from 5 different Apache/nginx-style access-log lines.
then re-implement the same extraction in Python `re` and output JSON.

**measurable gate:** all RegexOne lessons are complete, the regex101 pattern is green against 5 sample lines, and the Python script outputs valid JSON for those same lines.

**CTF thread:** solve the Bandit levels that force `grep`, `find`, `strings`, sorting, and pattern-hunting. these are tiny, but they make regex feel like a tool instead of a curse meow

**can u explain it?** ✅ - unaided, explain why `.*` is a bug magnet in log regex, and what a capture group gives u that a plain match does not.

---

## block 6 - CTF level-up hub meow (~25h running thread)

### why CTF stays beside the study meow

watching a video feels like learning, but its passive.
your brain can go "yeah yeah i get it" and then freeze when the terminal is staring back at u qwq

a CTF makes u actually do the thing.
u either get the flag or u dont.
its legal, sandboxed, and low-stakes, so u can build the real security instinct: "ok but how could this break?"

that instinct is the job.
so we dont save CTF for the end.
we keep a small challenge thread beside every topic and level it up slowly.

### the ladder: absolute beginner -> intermediate

stay on easy until easy is boring.
then climb one rung.
dont skip just because a harder platform looks cooler.

| Rung | when | do these |
|---|---|---|
| **0 - absolute beginner** | week 1 / terminal on-ramp | [OverTheWire Bandit 0-5](https://overthewire.org/wargames/bandit/) for SSH, `ls`, `cat`, hidden files, `file`, `find`; [picoCTF / CyLab Security Academy](https://cylabacademy.org/) General Skills beginner challenges. **free** |
| **1 - beginner** | Linux + networking + HTTP landing | [Bandit 6-20](https://overthewire.org/wargames/bandit/) for permissions, `grep`, `sort`, `uniq`, `nc`, SSH keys; picoCTF / CyLab General Skills + first Forensics + beginner Cryptography; [TryHackMe Linux Fundamentals 1](https://tryhackme.com/r/room/linuxfundamentalspart1), [2](https://tryhackme.com/r/room/linuxfundamentalspart2), [3](https://tryhackme.com/r/room/linuxfundamentalspart3), and [Intro to Networking](https://tryhackme.com/r/room/introtonetworking); [OverTheWire Natas 0-6](https://overthewire.org/wargames/natas/) for browser-only web basics. **free/freemium** |
| **2 - beginner to intermediate** | web + crypto + first exploitation | [PortSwigger SQL injection labs](https://portswigger.net/web-security/sql-injection) Apprentice level; [PortSwigger XSS labs](https://portswigger.net/web-security/cross-site-scripting) Apprentice level; [Natas 7-15](https://overthewire.org/wargames/natas/); [CryptoHack Introduction to CryptoHack](https://cryptohack.org/courses/intro/) + [Modular Arithmetic](https://cryptohack.org/courses/modular/) courses; [picoCTF / CyLab Security Academy](https://cylabacademy.org/) Web Exploitation + beginner Reverse Engineering; [TryHackMe OWASP Top 10](https://tryhackme.com/r/room/owasptop102021); [Hack The Box Starting Point](https://app.hackthebox.com/starting-point) Tier 0 as the first guided-box bridge. **free/freemium** |
| **3 - intermediate stretch** | after the guide, not required to proceed | [pwn.college Start Here](https://pwn.college/welcome/welcome/) -> [Program Security](https://pwn.college/program-security/program-security/); [OverTheWire Krypton](https://overthewire.org/wargames/krypton/), [Leviathan](https://overthewire.org/wargames/leviathan/), and [Narnia](https://overthewire.org/wargames/narnia/); [CryptoHack Symmetric Cryptography](https://cryptohack.org/courses/symmetric/) + [Public-Key Cryptography](https://cryptohack.org/courses/public-key/) courses; [Microcorruption](https://microcorruption.com/) for embedded reversing; [HTB Academy](https://academy.hackthebox.com/) tiered modules and non-Starting-Point Hack The Box machines as freemium explore-more. |

**picoCTF note:** use the name "picoCTF" in your notes because the ecosystem still does, but start from [CyLab Security Academy](https://cylabacademy.org/). CMU moved picoCTF into CyLab Security Academy, with the same beginner-friendly, free challenge style.
CyLab challenge entries are catalog/login-driven; use the named category and challenge examples instead of trusting unverified direct challenge URLs.

### topic -> challenge map

use this when u ask "ok what should i try now?"

| Study topic | go try this now | what it proves |
|---|---|---|
| Linux CLI basics | [Bandit 0-10](https://overthewire.org/wargames/bandit/) | navigation, files, permissions, pipes |
| Linux CLI intermediate | [Bandit 11-24](https://overthewire.org/wargames/bandit/) + [picoCTF / CyLab Security Academy](https://cylabacademy.org/) General Skills | `grep`, sorting, encoding, `strings`, `binwalk`, `nc`, SSH keys, light scripting |
| Networking | [picoCTF / CyLab Security Academy](https://cylabacademy.org/) General Skills network challenges like "Nice netcat..." + [TryHackMe Intro to Networking](https://tryhackme.com/r/room/introtonetworking) + [TryHackMe Wireshark: The Basics](https://tryhackme.com/r/room/wiresharkthebasics) | ports, TCP, DNS, packets, `nc`, PCAP reading |
| Web basics | [Natas 0-10](https://overthewire.org/wargames/natas/) -> [PortSwigger SQL injection](https://portswigger.net/web-security/sql-injection) + [XSS](https://portswigger.net/web-security/cross-site-scripting) Apprentice labs | HTTP, view-source, cookies, simple server-side logic |
| Web exploitation | [PortSwigger SQL injection](https://portswigger.net/web-security/sql-injection) + [XSS](https://portswigger.net/web-security/cross-site-scripting) Apprentice labs, then [Access control](https://portswigger.net/web-security/access-control) for IDOR-style logic | SQLi, XSS, request/response abuse |
| Crypto basics | [picoCTF / CyLab Security Academy](https://cylabacademy.org/) beginner Cryptography + [CryptoHack Introduction to CryptoHack](https://cryptohack.org/courses/intro/) + [Modular Arithmetic](https://cryptohack.org/courses/modular/) | encoding vs encryption, classical ciphers, modular arithmetic |
| Passwords / auth / hashing | Bandit credential/hash levels + [picoCTF / CyLab Security Academy](https://cylabacademy.org/) crack-the-hash style challenges + [TryHackMe Crack the Hash](https://tryhackme.com/r/room/crackthehash) | hashes, cracking workflow, auth evidence |
| Forensics / files | [picoCTF / CyLab Security Academy](https://cylabacademy.org/) beginner Forensics | `strings`, `binwalk`, `exiftool`, metadata, file carving, hidden data |
| Scripting | automate a repeated Bandit or [picoCTF / CyLab Security Academy](https://cylabacademy.org/) task; especially Bandit 24 | loops, sockets, parsing, solver scripts |
| PowerShell | [Under the Wire Century](https://underthewire.tech/century) | cmdlet discovery, object pipeline, Windows shell comfort |
| KQL / SOC logs | [Kusto Detective Agency](https://detective.kusto.io/) or [KC7 KQL 101](https://kc7cyber.com/go/take10) | table pipelines, log investigation, aggregation |
| SPL / SOC logs | [Splunk BOTS v3](https://github.com/splunk/botsv3) after the Search Tutorial | indexed search, `stats`, investigation reports |
| Reverse engineering | [picoCTF / CyLab Security Academy](https://cylabacademy.org/) beginner RE -> [Microcorruption](https://microcorruption.com/) -> [Leviathan](https://overthewire.org/wargames/leviathan/) | strings, basic binary reading, debugger mindset |
| Binary exploitation stretch | [pwn.college Program Security](https://pwn.college/program-security/program-security/) -> [Narnia](https://overthewire.org/wargames/narnia/) | memory bugs, exploit primitives |

### the anti-stall rules

- **20-30 min rule:** if a challenge gives u zero progress after ~25 minutes, read a hint or a writeup, learn the trick, and move on.
- **writeups from day one:** create a `ctf-writeups` repo with `problem -> analysis -> exploit -> fix/lesson`.
- **dont gate on a hard flag:** hard stretch challenges are pointers, not blockers.
- **always keep an easy one nearby:** end sessions on something solvable when u can. momentum matters, ig.

**do this** - create or continue a `ctf-writeups` repo.
by the end of this goal, publish **10 clean writeups** across at least 3 categories:

- at least 3 CLI/scripting writeups from Bandit, Century, or picoCTF / CyLab General Skills
- at least 2 web writeups from Natas or PortSwigger Apprentice labs
- at least 2 log/SOC writeups from Kusto Detective Agency, KC7, Splunk Search Tutorial, or BOTS
- the remaining 3 can be crypto, forensics, RE, or more of the above

**measurable gate:** 10 writeups exist, every writeup includes commands/queries/scripts used, and every writeup ends with one "what would prevent or detect this?" note.

**can u explain it?** ✅ - pick 3 writeups and explain them unaided:
what the system was supposed to do, what assumption broke, what exact action captured the flag, and what a defender would log, block, or monitor.

---

## exit check - done with Goal 3

- [ ] Python port scanner + auth-log parser are in GitHub with a README and clean output.
- [ ] PowerShell `Get-WinEvent` 4625 script exports CSV/HTML, and Century 0-10 are cleared.
- [ ] one KQL game path is solved, and u can explain a failed-logon query pipe by pipe.
- [ ] Splunk Search Tutorial report is saved, and u can explain `index=`, `stats`, and schema-on-read.
- [ ] RegexOne is complete, regex101 pattern passes 5 access-log lines, and the Python `re` version outputs JSON.
- [ ] `ctf-writeups` repo has 10 clean writeups across at least 3 categories.
- [ ] u know your next CTF rung, and it is not wildly above your current level.

**final can u explain it?** - unaided, tell this whole story:

> "i find suspicious failed logons in Windows logs, export them with PowerShell, parse/enrich them with Python, query the same pattern in KQL or SPL, use regex to extract the fields, and write a CTF-style report that explains what happened and how to detect it next time."

if u can do that, ur ready for [Specialization Paths](04-specialization.md).
if not, the noun u stumble on tells u exactly which block to redo.
dw, thats the whole point meow

---

[<- Goal 2: Networking & Security Core](02-core.md) | [Back to hub](README.md) | [Next: Specialization Paths ->](04-specialization.md)
