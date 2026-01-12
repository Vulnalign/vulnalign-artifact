# VulnAlign Artifact (Anonymous Submission)

This repository contains the code, sample data, and configuration files used to support the anonymous submission titled **VulnAlign**.  
The artifact demonstrates the dataset construction pipeline for:

- Linking CVEs to vulnerable and patched code
- Validating labels using static (rule-based) analysis
- Reconciling CWEs using ontology-aware reasoning

The repository is structured to allow reviewers to inspect the methodology and reproduce a small-scale version of the pipeline using the included samples.

---

## 📁 Repository Structure

```text
vulnalign-artifact/
│
├── CODE/
│   ├── mining/               # NVD mining, commit discovery, patch extraction
│   ├── validation/           # Static validation (Semgrep-based)
│   ├── ontology_scripts/     # CWE hierarchy reasoning and reconciliation
│   └── sanitize.py           # Utility script (formatting / cleanup)
│
├── DATA/
│   └── samples/              # Representative dataset snapshots (JSONL)
│
├── CONFIG/
│   ├── reproduce_config.json         # Parameters for sample reproduction
│   └── github_tokens.txt.example     # Template for optional GitHub tokens
│
├── SCRIPTS/
│   └── reproduce_results.sh          # Reproduces validation + ontology steps
│
├── OPEN_SCIENCE.md
├── REPRODUCIBILITY.md
└── README.md
