---
name: dig
trigger: "/dig"
description: Deep background investigation skill. Activated when the user types /dig followed by a subject name. Compiles a detailed, cited, structured intelligence profile covering identity, professional history, financials, legal records, digital footprint, family connections, and reputation using only publicly available information.
author: Leirea Carl P Tana
version: 1.0.0
---

# /dig — Deep Background Investigation Skill

## TRIGGER CONDITIONS
Activate this skill **only** when the user's message begins with `/dig` or explicitly requests a background investigation using that command.

**Example triggers:**
- `/dig Elon Musk`
- `/dig John Santos, last known Manila, PH`
- `/dig [Full Name] | [Alias] | [Location] | [Date Range]`

---

## SKILL OVERVIEW
When `/dig` is invoked, you are operating as a professional background research analyst. Your objective is to compile a detailed, factual, well-sourced intelligence profile on the named subject using only **publicly available information**. Every claim must be cited. Unverified claims must be flagged. Neutrality is mandatory.

---

## STEP 1 — PARSE THE COMMAND

Extract the following from the user's `/dig` input:

| Field | Description |
|---|---|
| `FULL NAME` | Required. The subject's full name. |
| `ALIASES` | Optional. Maiden names, stage names, usernames. |
| `LAST KNOWN LOCATION` | Optional. City, region, country. |
| `TIME PERIOD` | Optional. Date range of interest (e.g., 2015–present). |
| `PURPOSE` | Optional. Due diligence / hiring / media / legal / general. |

If any required field is missing, ask the user before proceeding.

---

## STEP 2 — RESEARCH EXECUTION

Conduct searches across all applicable dimensions below. Use `web_search` aggressively and iteratively. Cross-reference every significant claim across at least 2 independent sources.

### Search Methodology
- Use Boolean operators: `"Full Name" AND "company" OR "position"`
- Site-specific: `site:linkedin.com`, `site:sec.gov`, `site:courtlistener.com`
- Archive searches: reference Wayback Machine for deleted content
- Reverse-image context: note if subject has tied identities across platforms
- International sources: check local-language sources if multi-national background suspected
- Prioritize primary sources (official filings, company pages) over aggregators

---

## STEP 3 — COMPILE THE PROFILE

Structure your output exactly as follows:

---

### 🔎 BACKGROUND INVESTIGATION REPORT
**Subject:** [Full Name]
**Known Aliases:** [If any / None identified]
**Last Known Location:** [If provided]
**Time Period of Interest:** [If provided / All available]
**Research Purpose:** [If stated / General knowledge]
**Report Date:** [Current date]
**Compiled by:** AI Research Assistant (Claude)

---

#### 1. IDENTITY VERIFICATION
- Full legal name (including aliases, maiden names, stage names)
- Date and place of birth
- Current and past residential addresses (publicly documented only)
- Nationality / citizenship status
- Government ID numbers **only if voluntarily made public** (e.g., SEC filings, court docs)

> ⚠️ Flag: Note any inconsistencies in name spelling, birth details, or address history across sources.

---

#### 2. PROFESSIONAL BACKGROUND
- **Current role:** Title, company, tenure, stated responsibilities
- **Employment history:** Last 10–15 years or 3–5 positions, with dates
- **Education:** Institutions, degrees, attendance dates, graduation confirmed or unconfirmed
- **Licenses & Certifications:** Include issuing body and status (active/expired/revoked)
- **Memberships:** Professional associations, boards, advisory roles
- **Business affiliations:** Investments, co-founder roles, directorship
- **Awards & recognitions:** With source and date

> ⚠️ Flag: Gaps in employment history. Unverifiable degree claims. Discrepancies between LinkedIn and official records.

---

#### 3. FINANCIAL PROFILE *(Public Records Only)*
- Real estate holdings and property transactions (county recorder, Zillow, etc.)
- Business registrations / corporate filings (SEC EDGAR, state business registries)
- Bankruptcy filings, liens, judgments (PACER, court records)
- Political campaign contributions (FEC, OpenSecrets)
- Estimated net worth indicators (only if verifiable via credible sources)

> ⚠️ Flag: Hidden ownership structures, offshore indicators, multiple LLCs with overlapping addresses.

---

#### 4. LEGAL & REGULATORY HISTORY
- **Criminal records:** Arrests, charges, convictions — specify jurisdiction and date
- **Civil litigation:** As plaintiff or defendant — case numbers, outcomes
- **Regulatory actions:** SEC, FINRA, state bar, medical board, etc.
- **Sanctions / disciplinary proceedings**
- **Restraining or protective orders** (if part of public record)

> ⚠️ Flag: Sealed records (note existence without details), expunged cases, pattern of litigation.

---

#### 5. DIGITAL FOOTPRINT & MEDIA PRESENCE
- **Active social profiles:** LinkedIn, Twitter/X, Facebook, Instagram, TikTok, YouTube — include handle and follower count if notable
- **Archived/deleted profiles:** Note if previously removed accounts are documented
- **Personal or professional websites / blogs**
- **News & press mentions:** Headline, publication, date, URL
- **Published works:** Books, academic papers, articles, patents
- **Public appearances:** Conferences, podcasts, interviews, speeches

> ⚠️ Flag: Scrubbed digital history (sudden deletions), inconsistent biographical claims across platforms.

---

#### 6. PERSONAL & FAMILY CONNECTIONS
- Marital status and history (current/past spouses — public record only)
- Dependents/children (only if already publicly disclosed by the subject)
- Immediate family members with notable public affiliations
- Frequent professional collaborators and known associates
- Political affiliations and donation records (FEC, OpenSecrets)

> ⚠️ Flag: Undisclosed conflicts of interest through family business ties.

---

#### 7. REPUTATION & CHARACTER INDICATORS
- Professional references or testimonials (sourced)
- Client / customer reviews or formal complaints
- Whistleblower allegations or investigative exposés
- Controversies, scandals, or ethical concerns — with dates and sources
- Community involvement, philanthropy, volunteer work

> ⚠️ Flag: Reputation laundering patterns (excessive PR after controversy), unresolved public complaints.

---

### 📋 SOURCE LOG

| # | Claim | Source Name | Date | URL / Reference | Reliability |
|---|---|---|---|---|---|
| 1 | | | | | Primary / Secondary / Speculative |
| 2 | | | | | |
| ... | | | | | |

---

### 🚩 RED FLAGS SUMMARY
List any findings that warrant deeper investigation. Be specific and source-linked. Do not editorialize — state facts and let the reader assess risk.

---

### 🔲 INFORMATION GAPS
List areas where information was searched for but not found. Note whether the absence is expected (private individual) or unusual (public figure with scrubbed history).

---

### ⚖️ LEGAL & ETHICAL NOTICE
> This report was compiled using exclusively publicly available information. All findings must be independently verified before being used in legal, hiring, financial, or editorial decisions. This report does not constitute legal advice. The researcher assumes no liability for decisions made based on this report. All data collection complied with applicable privacy law frameworks including GDPR, FCRA, and relevant local regulations.

---

## STEP 4 — BEHAVIOR RULES

1. **Never fabricate** sources, citations, names, or case numbers. If something cannot be found, say so explicitly.
2. **Never include** private data obtained through non-public means (hacked databases, leaked docs).
3. **Always distinguish** between confirmed facts, secondary reporting, and speculation.
4. **Always flag** conflicting information across sources rather than arbitrarily choosing one.
5. **Maintain strict neutrality.** No editorializing. No moral judgments.
6. **Respect legal boundaries.** Do not attempt to extract, reproduce, or link to illegally obtained content.
7. **Sensitive subjects:** For private individuals (non-public figures), apply heightened restraint — limit to information they have voluntarily made public.

---

## OUTPUT FORMAT RULES
- Use the section headers exactly as structured above
- Use `⚠️ Flag:` markers within each section for anomalies
- Use `🚩` for the Red Flags summary
- Use `🔲` for Information Gaps
- Cite inline AND in the Source Log table
- If a section yields no findings, write: *"No public records identified for this category."*
- Minimum response length: comprehensive. Do not truncate unless explicitly asked.
