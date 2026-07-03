# contributing to IT career guides

Contributions keep the guides accurate, current, and useful.

## how to contribute

### 1. report issues

Found something wrong? Open an issue:

**broken links**
- Use the "Broken Link" issue template
- Include the guide name and section
- Provide the broken URL

**outdated content**
- Certification prices changed
- Exam codes updated
- Platform features changed
- Lab/tool tiers changed (free → paid)

**suggest resources**
- Better free alternatives
- New interactive labs
- Updated courses
- Community resources

### 2. content standards

All contributions must meet these standards:

#### interactive labs
- **Specific, not vague:** "Complete TryHackMe 'Network Services' room" not "learn networking"
- **What learner does:** Describe the actual task ("Deploy 3-tier app with docker-compose")
- **Cost transparency:** Free / Freemium ($X/mo) / Paid ($X one-time)
- **Verification:** Test the lab yourself before adding

#### certifications
- **Current exam codes:** CompTIA updates yearly
- **Accurate pricing:** USD + EUR, verified within 30 days
- **ROI context:** Is it baseline, differentiator, or nice-to-have?
- **Domain weights:** Include % breakdown from official objectives

#### salary data - do not add
- **No salary figures.** Guides intentionally omit pay numbers because they go stale fast and vary wildly by country, city, and sector. Don't add salary tables or ranges.
- **No job-board lists.** Boards are mostly local; use region-agnostic "how to find and target roles" guidance instead (employer *types*, company-direct, referrals, communities).
- Point readers to pulling their own current, local data at negotiation time rather than citing a number in the guide.

#### practice gates
- **Measurable thresholds:** "85%+ on practice exams" not "feel ready"
- **Source specified:** Which practice test platform?
- **Fresh attempts:** Not memorized questions

### 3. style guide

**Tone:**
- Direct and practical
- No motivational fluff
- Technical accuracy with plain explanations
- For learner-facing rewrite work, follow `AGENTS.md` for Minnn voice and todo-tree structure

**Formatting:**
- Use markdown tables for comparisons
- Include mermaid diagrams for roadmaps
- Link to official sources
- HTTPS links only

**Structure:**
- Follow the goal/todo-tree structure in `AGENTS.md`
- Hour-based timelines with pace variants
- Every major topic → interactive lab

### 4. research methodology

When adding new content, document your research:

**job market data:**
- Scrape 50+ job postings minimum
- Track skill frequency
- Note required vs preferred qualifications

**certification analysis:**
- Official exam objectives PDF
- Current pricing from provider
- Community pass rates (Reddit, Discord)

**lab verification:**
- Create account and test
- Check free tier limitations
- Verify sandbox quality

### 5. what not to contribute

- Affiliate links without disclosure
- Paid-only resources without free alternatives
- Vague guidance ("just practice coding")
- Personal opinions without data
- Outdated cert codes (check official sites)
- Salary figures (see the no-salary policy above)

### 6. pull request process

1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b fix/broken-link-security-plus`
3. **Make focused changes:** One topic per PR
4. **Test all links:** Verify they return HTTP 200
5. **Update "Last verified" dates** in your section
6. **Write clear commit messages:** "Update Security+ exam code to SY0-701"
7. **Submit PR** with description of changes

### 7. review process

Maintainers will check:
- Content accuracy
- Source credibility
- Formatting consistency
- Link health
- No promotional content

Expect feedback within 1 week. Large changes may take longer.

### 8. regional adaptations

We welcome localized versions:

**Role-targeting guidance:**
- Region-specific employer *types* and where they cluster
- Regional communities/Discord/meetups
- How to pull your own current, local pay data at negotiation time. The no-salary policy still applies: point readers to live sources, don't hard-code numbers.

**certification availability:**
- Exam center locations
- Regional pricing (VAT included)
- Language options

**legal/compliance:**
- GDPR for EU
- Local data protection laws

### 9. translation

Want to translate a guide?

1. Create `guides/[field]/README.[lang].md`
2. Translate all content
3. Adapt regional role-targeting guidance
4. Keep certification codes unchanged
5. Update links to localized resources

Supported languages:
- English (en) - original
- Spanish (es)
- Portuguese (pt)
- French (fr)
- German (de)

### 10. code of conduct

- Be respectful and constructive
- Focus on facts, not opinions
- No gatekeeping ("you'll never get a job without X")
- No spam or self-promotion
- No discrimination

### 11. recognition

Contributors are recognized:
- GitHub commit history
- CONTRIBUTORS.md file
- Shoutouts in releases

Significant contributions may receive:
- Co-maintainer status
- Early access to new guides
- Recognition in README

---

## questions?

Open a discussion thread or email the maintainers.
