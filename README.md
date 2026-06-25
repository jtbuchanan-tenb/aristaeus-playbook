<p align="center">
  <img src="aristaeus-agentic-ai-consulting-logo.png" alt="Aristaeus Agentic AI Consulting" width="280">
</p>

<h1 align="center">Threat-to-Board Playbook</h1>

<p align="center">
  <strong>From live threat data to board-ready maturity reporting — in one automated pipeline.</strong>
</p>

<p align="center">
  <a href="#">View on CyberAgents Exchange</a> &bull;
  <a href="#">Request a Demo</a> &bull;
</p>

---

## Overview

The Threat-to-Board Playbook delivers a continuously-updated security program maturity score with board-ready reporting, powered by live threat intelligence and exposure data mapped against NIST CSF and CIS Controls v8.

It chains together three open-source agents from the [CyberAgents Exchange](#) with two proprietary Aristaeus offerings to build a complete pipeline from raw vulnerability data to executive deliverables.

## Agent Chain

| # | Agent | Source | Purpose |
|---|-------|--------|---------|
| 1 | [Daily Threat Intelligence Briefing](#) | Exchange | Gather threat landscape, correlate against your environment |
| 2 | [Remediation Priority & Impact Agent](#) | Exchange | Prioritize what to fix by exploitation status and attack paths |
| 3 | [Tenable ATT&CK Mapper](#) | Exchange | Map findings to MITRE ATT&CK techniques |
| 4 | [Aristaeus Maturity Advisor](aristaeus-maturity-advisor.md) | Vendor | Score maturity against NIST CSF / CIS Controls v8 |
| 5 | [Aristaeus Program Intelligence](aristaeus-program-intelligence.md) | Vendor | Historical trending, peer benchmarks, executive reports |
| 6 | CISO Review & Board Briefing | Manual | Human review and delivery |

## Quick Start

```bash
# 1. Install open-source agents (requires Claude Code)
claude install-skill https://github.com/smjennings/threat-intel-daily
claude install-skill https://github.com/smjennings/Remediation_Priority-Impact_Agent
claude mcp add tenable-attack-mapper -- python -m tenable_attack_mapper

# 2. Contact Aristaeus for proprietary components
#    → Contact Aristaeus for licensing

# 3. Run the pipeline
claude "/threat-intel-daily"
claude "/fix-today"
# ... Maturity Advisor and Program Intelligence activate automatically
```

## What's in This Repo

| File | Description |
|------|-------------|
| [`playbook.md`](playbook.md) | CyberAgents Exchange listing (submit to `playbooks/` directory) |
| [`aristaeus-maturity-advisor.md`](aristaeus-maturity-advisor.md) | Product page for the proprietary maturity scoring skill |
| [`aristaeus-program-intelligence.md`](aristaeus-program-intelligence.md) | Product page for the proprietary executive reporting MCP server |

## About Aristaeus

Aristaeus Agentic AI Consulting helps security teams operationalize AI-driven program management. We build agentic workflows that turn operational security data into strategic decisions.

- **Web:** [aristaeus.ai](#)
- **Email:** partners@example
- **CyberAgents Exchange:** [exchange.tenable.com](#)

---

<p align="center">
  <sub>This playbook is listed on the <a href="#">Tenable CyberAgents Exchange</a>.</sub>
</p>
