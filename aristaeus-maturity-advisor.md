<p align="center">
  <img src="aristaeus-agentic-ai-consulting-logo.png" alt="Aristaeus Agentic AI Consulting" width="200">
</p>

# Aristaeus Maturity Advisor

**Proprietary Claude Code Skill — Licensed by Aristaeus Agentic AI Consulting**

> Turn vulnerability findings into a quantified security program maturity score — mapped to NIST CSF and CIS Controls v8, updated continuously from live data.

## What it does

The Aristaeus Maturity Advisor is a Claude Code skill that transforms tactical security outputs — threat intelligence, exposure prioritization, and ATT&CK coverage maps — into strategic program maturity assessments. Instead of annual spreadsheet exercises, your maturity score updates every time the pipeline runs.

- **Framework Mapping** — automatically maps vulnerability findings, remediation activity, and detection coverage to NIST CSF functions (Identify, Protect, Detect, Respond, Recover) and CIS Controls v8 safeguards
- **Quantified Scoring** — produces a 0–100 maturity score per control family with weighted sub-scores based on implementation completeness, evidence strength, and coverage breadth
- **Gap Analysis** — identifies the specific controls where your current state diverges most from your target profile, ranked by risk-reduction potential
- **Investment Recommendations** — recommends the highest-leverage improvements with estimated effort, linking each recommendation to the findings that justify it
- **Target Profile Alignment** — supports custom target profiles so you can score against your organization's stated maturity goals, not a generic baseline

## How it works

Invoked as part of the Threat-to-Board pipeline (or standalone with exported data), the skill:

1. Ingests structured outputs from upstream agents (threat intel correlation, prioritized remediation queues, ATT&CK coverage heatmaps)
2. Runs a proprietary mapping engine that correlates findings to framework controls using evidence-weighted scoring — not simple keyword matching
3. Compares scored state against the configured target profile
4. Produces a structured maturity report with per-function scores, gap rankings, and actionable recommendations
5. Exports results in a format consumed by Aristaeus Program Intelligence for historical trending

The mapping engine is trained on thousands of real-world security program assessments conducted by Aristaeus consultants. It understands that "having a WAF" isn't the same as "mature web application protection" — it scores based on evidence of operational effectiveness, not just tool presence.

## Output Format

```
┌─────────────────────────────────────────────────┐
│  NIST CSF Maturity Summary — 2026-06-25         │
├─────────────────────────────────────────────────┤
│  IDENTIFY        ████████░░░░  67/100  (+3)     │
│  PROTECT         ██████░░░░░░  52/100  (+7)     │
│  DETECT          █████████░░░  78/100  (+1)     │
│  RESPOND         ███████░░░░░  58/100  (+5)     │
│  RECOVER         ████░░░░░░░░  34/100  (+2)     │
├─────────────────────────────────────────────────┤
│  OVERALL         ██████░░░░░░  58/100  (+4)     │
│  TARGET PROFILE                72/100           │
│  GAP                           14 points        │
└─────────────────────────────────────────────────┘

Top 3 Gaps (highest risk-reduction potential):
1. RC.RP — Recovery Planning: No tested recovery 
   procedures for critical assets identified in 
   ATT&CK mapping (→ +8 points if addressed)
2. PR.AC — Access Control: Credential hygiene gaps
   correlating with 34% of prioritized remediations
   (→ +5 points if addressed)  
3. DE.CM — Continuous Monitoring: ATT&CK technique
   coverage shows 12 unmonitored initial-access 
   techniques (→ +4 points if addressed)
```

## Licensing

The Aristaeus Maturity Advisor is available as an annual subscription with:

- **Standard** — NIST CSF mapping, monthly scoring, email support
- **Professional** — NIST CSF + CIS Controls v8, continuous scoring, Slack integration, quarterly strategy review with an Aristaeus consultant
- **Enterprise** — custom framework support, multi-business-unit scoring, dedicated account team, on-site workshops

## Platform Requirements

- Claude Code (any supported platform)
- Tenable One or Tenable.sc environment with API access
- Upstream agents configured (Daily Threat Intel, Remediation Priority, ATT&CK Mapper)

## Request Access

Contact Aristaeus Agentic AI Consulting to schedule a demo and discuss licensing:

- **Web:** [example/maturity-advisor](#)
- **Email:** partners@example
- **Schedule a demo:** [example/demo](#)

---

*Aristaeus Maturity Advisor is proprietary software licensed by Aristaeus Agentic AI Consulting. The open-source agents it consumes are independently maintained and available on the CyberAgents Exchange.*
