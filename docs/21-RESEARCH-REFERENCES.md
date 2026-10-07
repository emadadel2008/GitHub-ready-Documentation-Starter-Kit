# 21 - Research References

This kit is an original, lightweight set of guidance and starter templates. The sources below were reviewed to identify complementary practices; this repository does not reproduce their full templates or require their tools. Use the linked source for its complete method, licensing, and implementation details.

| Source | Relevant practice considered | How this kit applies it |
|---|---|---|
| [arc42 architecture template](https://github.com/arc42/arc42-template) | Structured architecture documentation, quality requirements, risks, and glossary. | Quality-attribute scenarios and a separate risk register are optional additions to this kit's HLD workflow. |
| [Architecture Decision Record resources](https://github.com/architecture-decision-record/architecture-decision-record) | ADR concepts and multiple levels of decision-record detail. | A full ADR and a lightweight ADR template are available; select based on decision significance. |
| [adr-tools](https://github.com/npryce/adr-tools) | CLI support for creating numbered ADRs and marking records as superseded. | Listed as an optional aid in the documentation lifecycle guide. |
| [PagerDuty incident response documentation](https://github.com/PagerDuty/incident-response-docs) | Incident preparation, response, and after-action learning. | A reusable, blameless postmortem template and learning guide complement the existing live troubleshooting and runbook material. |
| [Diátaxis documentation framework](https://github.com/evildmp/diataxis-documentation-framework) | Organizing documentation by reader need: tutorials, how-to guides, reference, and explanation. | Included as a complementary content-classification lens, not a required restructure. |
| [C4-PlantUML](https://github.com/plantuml-stdlib/C4-PlantUML) | Text-based C4 architecture diagrams and reusable notation. | Mentioned as an optional diagrams-as-code alternative to Mermaid. |
| [Structurizr](https://github.com/structurizr/structurizr) | Modeling software architecture as text and deriving multiple views from one model. | Mentioned as an optional alternative when multiple consistent views justify additional tooling. |

## Selection Notes

- Practices were included when they address a gap in this kit and can be used without adopting a specific vendor or tool.
- Tooling is optional; Mermaid and Markdown remain suitable for many projects.
- Quality targets and risk scores must come from stakeholders and evidence; examples in templates do not set project targets.
- Review the linked sources directly before adopting their tools, process requirements, or templates in a production environment.
