# 🎤 Interview Prep — IT Support & Networking

> Technical + behavioral question bank for help-desk, NOC, desktop, junior network, and junior sysadmin roles.

[← Phase 5](05-job-hunt.md) · [Hub](README.md) · [Beyond Entry-Level →](beyond-entry.md)

---

## How support interviews actually run

IT Support is the one IT field where **soft skills can outweigh deep technical knowledge** at entry level. Help desk is a customer-service role that happens to involve computers. Most first-round interviews weigh these in roughly this order:

1. **Attitude & communication** — can you stay calm with a frustrated user?
2. **Process & judgment** — do you troubleshoot methodically, verify identity, document?
3. **Technical baseline** — DNS, DHCP, AD, basic Windows troubleshooting.

Networking-heavy roles (NOC, junior network tech) flip 2 and 3 — the technical bar is higher.

---

## The interview by role

| Role | What they screen hardest for |
|---|---|
| Help Desk T1 | Communication, patience, troubleshooting *process*, service attitude |
| Desktop Support | Hands-on hardware, imaging, OS troubleshooting, professionalism on-site |
| NOC Technician | Alert interpretation, OSI/networking depth, comfort with shift/on-call |
| Junior Network Tech | Subnetting, cabling, switch/router basics, willingness to do field work |
| Junior Sysadmin | AD/Entra, PowerShell, patching, backups, identity concepts |

---

## Scenario / roleplay questions (the ones that decide it)

These are the most common — interviewers care about your **process and communication**, not just the answer.

1. **"A user calls and can't log in. Walk me through what you do."**
   - Verify identity → ask what changed → check caps lock / correct username → check account lockout / expired password in AD → check for a wider outage → reset if needed → document → confirm resolution.
2. **"A user's computer is slow. How do you approach it?"**
   - Define "slow" (boot? one app? network?) → check resource usage (Task Manager) → recent changes / updates → malware → disk space → startup items → escalate if hardware.
3. **"A whole floor lost internet. What's your first move?"**
   - Scope it (one user vs many = network, not endpoint) → check switch/AP status → check for an outage ticket → ping gateway → escalate to network team with what you've ruled out.
4. **"A frustrated user is yelling. What do you do?"**
   - Stay calm, let them vent, acknowledge the impact, restate the problem, set expectations, follow through. Never match their energy.

> **The framework they want to hear:** *gather info → isolate the cause → test a fix → verify → document.* Say it out loud.

---

## Technical questions you will be asked

### Networking fundamentals
- **What happens when you type a URL and press Enter?** (DNS lookup → TCP/TLS → HTTP request → render — the classic.)
- **DNS vs DHCP — what does each do?** DNS resolves names→IPs; DHCP hands out IP/subnet/gateway/DNS automatically.
- **What's a default gateway?** The router a device sends traffic to when the destination is outside its subnet.
- **Private vs public IP?** RFC1918 ranges (10/8, 172.16/12, 192.168/16) vs internet-routable.
- **What does `ping` test? `tracert`/`traceroute`?** Reachability/latency vs the hop-by-hop path.
- **OSI model — name the layers / which layer is a switch vs router?** Switch = L2, router = L3.
- **Subnetting:** "How many usable hosts in a /24? a /26?" (254; 62.) Know the basic math.

### Windows / OS troubleshooting
- **A device won't get on the network — how do you diagnose?** Link light → `ipconfig` (got an IP? APIPA 169.254 = DHCP fail) → ping gateway → ping DNS → `nslookup`.
- **What's APIPA (169.254.x.x) telling you?** The client couldn't reach a DHCP server.
- **Safe Mode — when and why?** Driver/startup issues, malware removal.
- **What's in the event you'd check for a crash?** Event Viewer.

### Active Directory / identity
- **What is Active Directory?** Microsoft's directory service for authentication/authorization of users and devices in a domain.
- **AD vs Entra ID?** On-prem domain vs cloud identity (M365/Azure); hybrid joins them.
- **What's a Group Policy / GPO?** Centralized config/policy push to domain devices.
- **How do you reset a user's password / unlock an account?** AD Users & Computers or Entra admin center — know the click path.

### Ticketing & process
- **What's in a good ticket?** User, contact, clear problem statement, steps tried, priority, resolution/notes.
- **How do you prioritize 5 tickets at once?** Impact × urgency (one user vs whole site; exec vs routine), follow SLA.

---

## PowerShell (differentiator — sysadmin track)
- **What does `Get-Help` do?** Built-in documentation for cmdlets.
- **Write a one-liner to find disabled AD users / bulk-create users.** Even reading and explaining a script scores points.
- **`Get-Service`, `Get-Process`, `Restart-Service`** — know the verb-noun pattern.

---

## CCNA-level (junior network track)
- **VLAN — what and why?** Logical network segmentation on a switch.
- **Switch vs router vs firewall?** L2 forwarding vs L3 routing vs traffic filtering/policy.
- **What's NAT?** Translates private IPs to a public IP for internet access.
- **Static vs dynamic routing?** Manually configured vs learned via a protocol (OSPF/EIGRP).

---

## Behavioral (STAR format)

Structure every answer: **Situation → Task → Action → Result.**

- "Tell me about a time you helped a non-technical person with a tech problem."
- "Describe a time you dealt with an angry or frustrated customer."
- "A time you didn't know the answer — what did you do?" (They want: *I researched / escalated / followed up* — not *I guessed*.)
- "A time you juggled multiple priorities."
- "Why IT support? Where do you want to be in 2 years?" (Show the ladder: support → sysadmin/network/cloud.)

> **Honesty wins.** "I hadn't seen that before, so I checked our KB, then escalated with what I'd ruled out" beats pretending to know.

---

## Your questions for them (always ask 2–3)
- "What does the escalation path look like from T1?"
- "What ticketing system do you use?"
- "What does growth from this role look like — is there a path to sysadmin/network?"
- "What's the team's split between phone, remote, and on-site work?"

---

## Quick-prep checklist
- [ ] Can recite the troubleshooting framework out loud
- [ ] Can explain DNS, DHCP, default gateway, subnet in plain English
- [ ] Can walk through "can't log in" and "no internet on the floor" scenarios
- [ ] 4–5 STAR stories ready (frustrated user, didn't know answer, multitasking, helped someone, conflict)
- [ ] Know the click-path to reset a password in AD/Entra
- [ ] 2–3 questions ready to ask them
- [ ] Can name your home-lab project and what you learned

Next: [Beyond Entry-Level — Years 2+ →](beyond-entry.md)
