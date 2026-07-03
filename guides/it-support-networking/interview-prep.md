# interview prep - IT support & networking meow

> technical + behavioral question bank for help desk, NOC, desktop, junior network, and junior sysadmin roles.

[Job Hunt](05-job-hunt.md) - [Hub](README.md) - [Beyond Entry-Level](beyond-entry.md)

---

- [ ] **know how support interviews run**
- [ ] **practice scenario questions**
- [ ] **drill technical basics**
- [ ] **prepare PowerShell / CCNA extras if relevant**
- [ ] **prepare STAR stories**
- [ ] **ask good questions**
- [ ] **finish quick prep checklist**

## how support interviews run

entry support interviews often weigh:

- [ ] attitude and communication
- [ ] process and judgment
- [ ] technical baseline: DNS, DHCP, AD, Windows troubleshooting

networking-heavy roles raise the technical bar. help desk still weighs calm communication heavily.

## interview by role

| Role | What they screen hardest |
|---|---|
| Help Desk T1 | communication, patience, troubleshooting process |
| Desktop Support | hardware, imaging, OS troubleshooting, on-site professionalism |
| NOC Technician | alerts, OSI/networking, shift/on-call comfort |
| Junior Network Tech | subnetting, cabling, switch/router basics |
| Junior Sysadmin | AD/Entra, PowerShell, patching, backups |

## scenario questions

- [ ] user cant log in: verify identity, check changes, username/caps, lockout/expired password, outage, reset, document, confirm.
- [ ] computer is slow: define slow, check Task Manager, changes/updates, malware, disk, startup, hardware escalation.
- [ ] whole floor lost internet: scope it, check switch/AP, outage ticket, ping gateway, escalate with ruled-out facts.
- [ ] frustrated user yelling: stay calm, acknowledge impact, restate problem, set expectations, follow through.

framework: gather info -> isolate cause -> test fix -> verify -> document.

## technical questions

### networking

- [ ] what happens when typing a URL?
- [ ] DNS vs DHCP?
- [ ] default gateway?
- [ ] private vs public IP?
- [ ] `ping` vs `tracert`/`traceroute`?
- [ ] OSI layers; switch vs router layer?
- [ ] hosts in `/24` and `/26`?

### Windows / OS

- [ ] device wont get network - diagnose
- [ ] APIPA `169.254.x.x`
- [ ] Safe Mode use cases
- [ ] Event Viewer for crashes

### Active Directory / identity

- [ ] what is Active Directory?
- [ ] AD vs Entra ID?
- [ ] what is a GPO?
- [ ] password reset / unlock click path

### ticketing and process

- [ ] what goes in a good ticket?
- [ ] prioritize 5 tickets at once

## PowerShell differentiator

- [ ] what does `Get-Help` do?
- [ ] explain a one-liner for disabled AD users or bulk user creation
- [ ] know `Get-Service`, `Get-Process`, `Restart-Service`

## CCNA-level extras

- [ ] VLAN - what and why?
- [ ] switch vs router vs firewall?
- [ ] NAT?
- [ ] static vs dynamic routing?

## behavioral prompts

use STAR: Situation -> Task -> Action -> Result.

- [ ] helped a non-technical person
- [ ] angry or frustrated customer
- [ ] didnt know the answer
- [ ] juggled multiple priorities
- [ ] why IT support? where in 2 years?

honesty wins. "i checked KB, escalated with what i ruled out, and followed up" beats pretending.

## questions to ask them

- [ ] what does escalation path from T1 look like?
- [ ] what ticketing system do u use?
- [ ] what growth path exists to sysadmin/network?
- [ ] whats the split between phone, remote, and on-site work?

## quick-prep checklist

- [ ] can recite troubleshooting framework
- [ ] can explain DNS, DHCP, default gateway, subnet
- [ ] can walk through "cant log in" and "no internet on the floor"
- [ ] 4-5 STAR stories ready
- [ ] know AD/Entra password reset path
- [ ] 2-3 questions ready
- [ ] can name home-lab project and what u learned

[Beyond Entry-Level - Years 2+](beyond-entry.md)
