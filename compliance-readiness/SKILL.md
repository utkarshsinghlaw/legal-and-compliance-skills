---
name: compliance-readiness
description: Generalized regulatory and compliance evaluator for cross-jurisdictional audits.
version: 2.0.0
author: Antigravity
metadata:
  tags: [compliance, legal, audit, grc]
  required_tools: [search_web, read_url_content]
---

# Compliance Readiness Skill

## Trigger
- User asks for general compliance verification against a specific law (e.g., CCPA, PDPB, HIPAA).
- User needs to validate internal policies against external frameworks.

## Negative Constraints
- **NO Legal Advice**: Outputs are for informational and audit preparation purposes only.
- **NO Hallucinated Laws**: Always verify specific clauses and requirements using live web searches.

## How to Use
1. **Identify Framework**: Determine the exact regulation or standard the user wants to audit against.
2. **Live Search**: Use `search_web` to retrieve current interpretations and guidelines for that framework.
3. **Gap Analysis**: Cross-reference the user's provided policy/context against the retrieved guidelines.
4. **Report**: Output a prioritized remediation list with citations.

## Worked Example
**User Input**: "Check our data deletion policy against California's CCPA."
**Agent Action**: Searches official CCPA guidelines regarding "Right to Delete". Identifies that the user's policy lacks a toll-free number for requests (a CCPA requirement). Outputs the gap and suggests remediation.