# Contributing to IT Career Guides

Thank you for your interest in improving these guides! Contributions from the community help keep content accurate, relevant, and comprehensive.

## How to Contribute

### 1. Report Issues

Found something wrong? Open an issue:

**Broken Links**
- Use the "Broken Link" issue template
- Include the guide name and section
- Provide the broken URL

**Outdated Content**
- Certification prices changed
- Exam codes updated
- Platform features changed
- Lab/tool tiers changed (free → paid)

**Suggest Resources**
- Better free alternatives
- New interactive labs
- Updated courses
- Community resources

### 2. Content Standards

All contributions must meet these standards:

#### Interactive Labs
- **Specific, not vague:** "Complete TryHackMe 'Network Services' room" not "learn networking"
- **What learner does:** Describe the actual task ("Deploy 3-tier app with docker-compose")
- **Cost transparency:** Free / Freemium ($X/mo) / Paid ($X one-time)
- **Verification:** Test the lab yourself before adding

#### Certifications
- **Current exam codes:** CompTIA updates yearly
- **Accurate pricing:** USD + EUR, verified within 30 days
- **ROI context:** Is it baseline, differentiator, or nice-to-have?
- **Domain weights:** Include % breakdown from official objectives

#### Salary Data — Do NOT add
- **No salary figures.** Guides intentionally omit pay numbers — they go stale fast and vary wildly by country, city, and sector. Don't add salary tables or ranges.
- **No job-board lists.** Boards are mostly local; use region-agnostic "how to find and target roles" guidance instead (employer *types*, company-direct, referrals, communities).
- Point readers to pulling their own current, local data at negotiation time rather than citing a number in the guide.

#### Practice Gates
- **Measurable thresholds:** "85%+ on practice exams" not "feel ready"
- **Source specified:** Which practice test platform?
- **Fresh attempts:** Not memorized questions

### 3. Style Guide

**Tone:**
- Direct and practical
- No motivational fluff
- Technical accuracy over accessibility

**Formatting:**
- Use markdown tables for comparisons
- Include mermaid diagrams for roadmaps
- Link to official sources
- HTTPS links only

**Structure:**
- Follow Phase 0-5 template
- Hour-based timelines with pace variants
- Every major topic → interactive lab

### 4. Research Methodology

When adding new content, document your research:

**Job Market Data:**
- Scrape 50+ job postings minimum
- Track skill frequency
- Note required vs preferred qualifications

**Certification Analysis:**
- Official exam objectives PDF
- Current pricing from provider
- Community pass rates (Reddit, Discord)

**Lab Verification:**
- Create account and test
- Check free tier limitations
- Verify sandbox quality

### 5. What NOT to Contribute

❌ **Affiliate links** without disclosure  
❌ **Paid-only resources** without free alternatives  
❌ **Vague guidance** ("just practice coding")  
❌ **Personal opinions** without data  
❌ **Outdated cert codes** (check official sites)  
❌ **Salary figures** (see the no-salary policy above)  

### 6. Pull Request Process

1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b fix/broken-link-security-plus`
3. **Make focused changes:** One topic per PR
4. **Test all links:** Verify they return HTTP 200
5. **Update "Last verified" dates** in your section
6. **Write clear commit messages:** "Update Security+ exam code to SY0-701"
7. **Submit PR** with description of changes

### 7. Review Process

Maintainers will check:
- Content accuracy
- Source credibility
- Formatting consistency
- Link health
- No promotional content

Expect feedback within 1 week. Large changes may take longer.

### 8. Regional Adaptations

We welcome localized versions:

**Role-targeting guidance:**
- Region-specific employer *types* and where they cluster
- Regional communities/Discord/meetups
- How to pull your own current, local pay data at negotiation time (the no-salary policy still applies — point readers to live sources, don't hard-code numbers)

**Certification Availability:**
- Exam center locations
- Regional pricing (VAT included)
- Language options

**Legal/Compliance:**
- GDPR for EU
- Local data protection laws

### 9. Translation

Want to translate a guide?

1. Create `guides/[field]/README.[lang].md`
2. Translate all content
3. Adapt regional role-targeting guidance
4. Keep certification codes unchanged
5. Update links to localized resources

Supported languages:
- English (en) — Original
- Spanish (es)
- Portuguese (pt)
- French (fr)
- German (de)

### 10. Code of Conduct

- Be respectful and constructive
- Focus on facts, not opinions
- No gatekeeping ("you'll never get a job without X")
- No spam or self-promotion
- No discrimination

### 11. Recognition

Contributors are recognized:
- GitHub commit history
- CONTRIBUTORS.md file
- Shoutouts in releases

Significant contributions may receive:
- Co-maintainer status
- Early access to new guides
- Recognition in README

---

## Questions?

Open a discussion thread or email the maintainers.

**Thank you for helping others break into IT careers!** 🚀
