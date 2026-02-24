# RFO Compliance Plugin

This is a Claude Code plugin that analyzes codebases for NIST 800-53 Rev5 compliance controls and pushes structured findings to the RFO (Risk Force Orchestrator) backend.

## Installation

```
/plugin marketplace add riskforce/rf-o-compliance-plugin
/plugin install rf-o-compliance@riskforce
```

## Authentication

Authentication is handled automatically via OAuth. On first use, Claude Code will open a browser window for you to log in to your RFO account. No API key configuration is needed.

## Usage

Use the `/rf-o-compliance:assess-control` skill to assess controls:
- Assess a specific control: mention the control ID (e.g. "assess SC-02")
- Assess a family: mention the family (e.g. "assess all AC controls")
- Assess all code-assessable controls: say "assess all controls"

The plugin will analyze the codebase, generate evidence-backed findings, and push them to your RFO system via API.
