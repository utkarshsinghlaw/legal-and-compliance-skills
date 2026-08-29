---
name: uk-compliance-readiness
description: Comprehensive UK compliance readiness evaluation for general business operations, data protection, and digital laws.
version: 1.2.0
author: Antigravity
metadata:
  tags: [compliance, uk, gdpr, legal, governance, business]
  required_tools: [search_web, read_url_content]
---

# UK Compliance Readiness Skill

## Trigger
- User asks for UK regulatory compliance checks (e.g., UK GDPR, Companies Act, CMA guidelines, FCA).
- Need to validate business policies, e-commerce workflows, data handling, or operational legalities for a UK-based entity.

## Negative Constraints (Guardrails)
- **NO Legal Advice**: Explicitly state that outputs are for informational/audit preparation purposes and do not constitute formal legal counsel.
- **NO Fabricated Regulations**: Do not hallucinate laws. All regulatory claims MUST be grounded in recent web searches from official `.gov.uk`, `ico.org.uk`, or equivalent official sources.

## How to use
1. **Context Gathering**: User provides the business policy, website terms, product workflow, or data framework to be evaluated.
2. **Live Research**: Agent MUST execute a web search targeting `site:gov.uk` OR `site:ico.org.uk` for the latest updates on the relevant topic.
3. **Core UK Framework Verification**:
   - *Data Protection (UK GDPR / DPA 2018)*: Check lawful basis of processing, data minimization, cookie consent (PECR), and cross-border data transfer rules.
   - *Consumer Protection (CMA / Consumer Rights Act)*: Validate refund policies, clear pricing, and prevention of unfair trading practices (e.g., fake reviews, hidden fees).
   - *Corporate Governance (Companies Act 2006)*: Verify necessary corporate disclosures (e.g., displaying company registration number, registered office address on websites/emails).
   - *Sector-Specific (if applicable)*: Identify if FCA (finance), MHRA (health), or ASA (advertising) guidelines apply and verify compliance.
4. **Evaluation**: Compare the user's context against these frameworks and live guidelines.
5. **Reporting**: Output a gap analysis report with direct citations (URLs) to official UK government sources.

## Worked Example
**User Input:**
"Evaluate our new e-commerce checkout flow and privacy policy for UK compliance."

**Agent Action:**
1. Uses `search_web` for "ecommerce cookie consent site:ico.org.uk" and "consumer rights act returns site:gov.uk".
2. Generates a report highlighting gaps in the user's workflow (e.g., pre-ticked consent boxes violating PECR, or failing to state the 14-day cooling-off period under UK distance selling regulations).

## Best for
- General UK Business compliance.
- UK GDPR / PECR data audits.
- CMA / E-commerce consumer rights validation.