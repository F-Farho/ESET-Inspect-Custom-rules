# ESET Inspect Custom Rules

A personal collection of custom detection rules created for **ESET Inspect**.

The goal of this repository is to keep custom rules organized, searchable by rule name, and easy to review, reuse, and maintain over time.

## Disclaimer

> **This is a personal and independent project.**
>
> This repository is **not an official ESET project** and is not affiliated with, endorsed by, sponsored by, maintained by, or supported by **ESET, spol. s r.o.** or any of its affiliates.
>
> The rules in this repository are provided **as-is**, without warranty of any kind. They may require adaptation to your environment and may produce false positives or unexpected results.
>
> **Always review and test rules in a controlled environment before deploying them to production.**


## Rule Naming

Each rule should be stored as a separate XML file using a descriptive name based on the detection purpose.

Example:

```text
rules/AI-Agent-Reading-Credential-Files[XX1234]
rules/MCP-Configuration-Created-or-Modified[XX1234]
rules/Local-LLM-Exposed-to-Network[XX1234abc]
the XX stands for author initials, abc is the rule sub-version
```

Rules can be browsed directly in the `rules/` directory by filename; the README does not need to be updated for every new rule.

## Rule Information

Where applicable, each rule should include:

- Rule name
- Short detection description
- MITRE ATT&CK technique or sub-technique
- Detection logic
- Recommended analyst actions

Additional context, tuning notes, known false positives, or testing information can be documented alongside the rule when useful.

## Usage

Review the XML before importing it into ESET Inspect. Detection logic should be validated against the ESET Inspect version and telemetry available in the target environment.

Rules should be considered starting points rather than universally production-ready detections.

## Submitting a Custom Rule

If you have a custom rule you would like to share the community with, use the provided [`rules/template.xml`](rules/template.xml) as the starting format and replace the placeholder values with the rule-specific metadata and detection logic.

## Contributions

This repository primarily contains rules developed and maintained as part of this personal detection-engineering work. Suggestions and improvements can be reviewed individually.

---

**ESET** and **ESET Inspect** are trademarks or registered trademarks of ESET, spol. s r.o. Their use here is solely for identification of product compatibility and does not imply affiliation or endorsement.
