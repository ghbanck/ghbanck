# Gustavo Henrique Banck

**Technical Artist | Production Tools | Pipeline Support | Asset Validation | Workflow-Control Systems**

I build production-facing tools, documentation, and workflow systems for artists, technical artists, and implementation teams.

My work sits between art production, technical constraints, content implementation, pipeline clarity, validation logic, and workflow reliability. I focus on turning ambiguous production problems into structured tools, safer handoff processes, repeatable validation logic, and clearer technical decisions.

A core part of my strength is risk-first production thinking: I tend to red-team workflows before trusting them.

I am not defined by a single DCC, engine, scripting language, or workflow domain. My strength is entering production systems, understanding their constraints, identifying hidden risk, and turning friction into clearer tools, safer workflows, validation logic, and traceable handoff.

The platform can change. The method stays consistent: understand the production problem, structure the input, protect the operation, validate the output, and make the result easier to repeat.


---

## Core Direction

I am currently expanding my tooling work across production environments, technical constraints, DCC workflows, and workflow-control systems.

My focus is not simply writing scripts for tools I already know. It is applying production systems thinking to workflows that need clearer input handling, classification, safety gates, validation, reporting, internal QA, documentation, and handoff clarity.

Current public and documented work includes:

* asset diagnostics, mesh review, and scene-density feedback;
* Maya scene organization, safe routing, and production handoff structure;
* evidence-gated AI workflow claims, output review, and public control-gate architecture;
* large-scale asset implementation, frontend consistency, and release-preparation workflows;
* production automation that reduced roughly one week of manual post-hardlock work to about one minute through metadata checks, structured validation, and safer release-preparation support;
* pipeline documentation that turns complex technical behavior into readable implementation plans, test checklists, and public-facing project structure.

The specific software or pipeline may be familiar or completely new. What matters is the production problem, the constraints around it, the risk of getting it wrong, and the structure needed to make the workflow reliable.

---

## Selected Work

### Public Projects

| Project                       | Type                                             | Focus                                                                                                                                              | Status                                |
| ----------------------------- | ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| **PolyCount Wizard**          | Public Production Tool / Documented Tooling Case | Mesh budget diagnostics, scene density review, object-level validation                                                                             | Public documentation / private source |
| **Maya Production Pipeliner** | Tooling Lab / Production Scaffold                | Maya scene organization, safety-aware routing, production handoff clarity                                                                          | Public scaffold / in development      |
| **MOI Control Gate**          | Public Architecture / Control-Gate Thesis        | Control-before-automation architecture for evidence boundaries, LLM output review, workflow trust, release boundaries, and epistemic drift control | Public architecture                   |
| **MOI Lite Demo**             | Public Demo / Façade Layer                       | Public-facing demonstration of MOI Lite’s evidence-gated demo layer; a small, sanitized slice of the private runtime’s control logic               | Public demo                           |

### Case Studies / Tooling Labs

| Project                               | Type                                       | Focus                                                                                                     | Status                                                      |
| ------------------------------------- | ------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Production Workflow Control Study** | Mindset Guide / Compact Study              | Pipeline reliability, workflow control, internal QA, validation, and handoff logic                        | Public case study                                           |
| **HS FE GuideTool**                   | Sanitized Internal Tool Case Study         | Frontend visual validation, framing consistency, canvas segmentation                                      | Public portfolio case                                       |
| **EOB Automation Tool**               | Sanitized Production Automation Case Study | Post-hardlock release preparation, metadata checks, structured validation, and implementation consistency | Reduced roughly one week of manual work to about one minute |
| **Edge QA Wizard**                    | Tooling Lab                                | Edge QA standardization, scalable asset review, project-wide technical consistency                        | In development                                              |
| **Remesher Wizard**                   | Tooling Lab                                | Mesh cleanup, controlled remesh workflows, topology review                                                | In development                                              |

---

## Featured Projects

### PolyCount Wizard

Production tool for mesh budget diagnostics, scene density review, and object-level validation.

Built to help artists and technical artists identify density issues, budget risk, modifier impact, and scene complexity with clearer visual feedback and more direct production signals.

The goal is not only to count polygons. The goal is to make technical review easier to read, easier to repeat, and easier to act on during production.

Public scope: documentation, visual breakdown, testing status, and production-facing presentation.

Private scope: source code and distributable builds unless prepared for public release.

<a href="https://github.com/ghbanck/PolyCount-Wizard">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/PolyCount-Wizard">
  <img src="https://img.shields.io/badge/PolyCount_Wizard-9AD7D2?style=for-the-badge" alt="PolyCount Wizard">
</a>

---

### Maya Production Pipeliner

Safety-aware Maya Python utility for scene organization and production handoff.

This project implements a working Maya-native runtime that turns messy scene
hierarchies into readable production handoff structure before deeper validation,
export, review, or downstream integration begins.

The public repository contains the implemented core runtime (scanner, classifier,
organizer, reporter, pipeline orchestrator, and minimal UI), defensive design
documentation, data contracts, and per-slice manual Maya validation evidence.

The production problem behind the tool is simple: a Maya scene can become hard
to read before it becomes technically invalid. Final meshes, test assets,
references, cameras, lights, locators, rig-sensitive hierarchies, instanced
geometry, hidden objects, namespaces, duplicate short names, and previous tool
output can all coexist in ways that make handoff unclear.

The implemented workflow is:

1. scan scene facts;
2. classify objects into handoff routes;
3. build a route plan;
4. preserve unsafe or ambiguous content — referenced, instanced, and
   rig/deformer-sensitive nodes remain report-only and are never moved;
5. preview changes through a strictly non-mutating Dry Run;
6. Apply safe operations inside a single named undo chunk, with validated
   idempotent re-execution;
7. write traceable TXT/JSON reports.

Dry Run and Apply are implemented and validated through a validation-script
suite and a per-slice manual test checklist, covering mayapy runs and Maya
2027.1 smoke validation. Leaf reclassification after user edits is the
remaining open case, and the tool is intentionally not yet marked
release-ready.

This project also marks a deliberate return: I started my career in Maya in
2018 and worked with Maya rigs, imports, and exports in AAA production before
years of Blender-focused tooling. The Pipeliner applies that same safety,
validation, and handoff mindset back to Maya-native tooling at production depth.

<a href="https://github.com/ghbanck/Maya-Production-Pipeliner">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/Maya-Production-Pipeliner">
  <img src="https://img.shields.io/badge/Maya_Production_Pipeliner-9AD7D2?style=for-the-badge" alt="Maya Production Pipeliner">
</a>

---

### MOI Control Gate

Public architecture repository for control before automation.

MOI Control Gate documents the broader thesis behind my workflow-control work: AI systems are already entering real production contexts, but fluent generation is not the hard part anymore. The hard part is deciding what a workflow is allowed to trust before model output becomes action.

MOI Control Gate is about evidence boundaries, LLM output review, workflow reliability, human decision separation, release-boundary control, and epistemic drift control.

It is not a prompt pack, not a chatbot trick, and not a claim that a public runtime has been deployed. It is the public architecture layer for the method: a way to expose and constrain the behaviors that make AI workflows look complete before they are actually verified.

<a href="https://github.com/ghbanck/MOI-Control-Gate">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/MOI-Control-Gate">
  <img src="https://img.shields.io/badge/MOI_Control_Gate-9AD7D2?style=for-the-badge" alt="MOI Control Gate">
</a>

---

### MOI Lite Demo

Public façade for MOI Lite’s evidence-gated demo layer.

MOI Lite Demo is not the private functional runtime. It is a small public-facing demonstration of the response boundary behind MOI Lite: how a backend-backed workflow can refuse to treat unsupported claims, fluent answers, or declared approvals as operational truth.

The demo keeps the public concept simple:

```text
declared != verified != approved
```

A model can generate.
A workflow can look complete.
A person can approve an action.

MOI Lite Demo shows why those states must stay separated. It presents the evidence-gated behavior in public scope while keeping private runtime code, operational prompts, enforcement logic, traces, and production internals out of the repository.

In the broader architecture, MOI Lite Demo is the lightweight public slice. MOI Control Gate carries the larger control-system thesis.

<a href="https://github.com/ghbanck/MOI-Lite-Demo">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/MOI-Lite-Demo">
  <img src="https://img.shields.io/badge/MOI_Lite_Demo-9AD7D2?style=for-the-badge" alt="MOI Lite Demo">
</a>

---

## Mindset Guide / Pipeline Compact Study

### Production Workflow Control Study

Compact public case study presenting my production mindset: how I structure ambiguous pipeline problems, identify hidden risks before implementation, define safety boundaries, and turn workflow friction into clearer execution logic.

This case is my public-facing pipeline constitution: a concise guide to how I think across tools, production support, internal QA, validation, source-of-truth handling, and handoff systems.

<a href="https://www.artstation.com/artwork/XJyKXl">
  <img src="https://img.shields.io/badge/View_Case_Study-111111?style=for-the-badge" alt="View Case Study">
</a>
<a href="https://www.artstation.com/artwork/XJyKXl">
  <img src="https://img.shields.io/badge/Workflow_Control_Study-9AD7D2?style=for-the-badge" alt="Workflow Control Study">
</a>

---

## Production Tooling Case Studies

### HS FE GuideTool

Sanitized case study demonstrating my thinking behind an internal production tool created in a professional Epic Games context.

The tool focused on frontend visual validation, framing consistency, canvas segmentation, and repeatable presentation review workflows.

This case represents my approach to tooling: identify repeated manual judgment, convert it into a clearer visual system, and reduce inconsistency without removing the artist or implementer from the loop.

<a href="https://www.artstation.com/artwork/nJaK04">
  <img src="https://img.shields.io/badge/View_Portfolio_Case-111111?style=for-the-badge" alt="View Portfolio Case">
</a>
<a href="https://www.artstation.com/artwork/nJaK04">
  <img src="https://img.shields.io/badge/HS_FE_GuideTool-9AD7D2?style=for-the-badge" alt="HS FE GuideTool">
</a>

---

### EOB Automation Tool

Sanitized production automation case study based on end-of-build workflow support.

Built to reduce repetitive post-hardlock implementation work during release preparation by automating metadata checks, structuring validation steps, and improving consistency across final asset setup tasks.

The tool reduced roughly one week of manual post-hardlock work to about one minute by converting repeated release-preparation actions into a faster, more structured automation flow.

This case represents my approach to production automation: identify repeated manual production friction, automate the parts where the logic is clear, preserve review where human judgment matters, and make the final output easier to verify.

---

## Tooling Lab / In Development

### Edge QA Wizard

Production QA tool for standardizing edge review, edge treatment, and geometry validation across a full project.

Designed to support predefined QA rules, consistent review signals, and scalable asset review workflows, helping artists and technical artists apply the same technical standard across multiple assets instead of reviewing edge issues case by case.

### Remesher Wizard

Production-oriented mesh cleanup and remeshing assistant for controlled topology review.

Designed as a workflow support tool for testing cleanup behavior, reviewing topology conditions, and reducing repetitive manual mesh preparation steps.

---

## Production Background

Former Fortnite asset implementation experience supporting high-volume live-service content delivery, asset setup, presentation consistency, troubleshooting, and workflow improvement.

Selected production impact:

* Supported Fortnite cosmetic implementation and pipeline improvement work across 7 live-service seasons in Unreal Engine
* Contributed to implementation, validation, fixing, and maintenance of high-volume cosmetic assets from internal and external sources
* Resolved a release-critical backlog of roughly 500 pickaxe presentation issues in less than one week under hard production deadline
* Created HS FE GuideTool to standardize frontend framing validation, canvas segmentation, and visual presentation checks
* Created EOB automation tooling to reduce repetitive post-hardlock setup work and improve implementation consistency during release preparation
* Proposed a single-source-of-truth pipeline direction connecting upstream production inputs to final Unreal outputs through validation, ID synchronization, structured data generation, and output logging

Broader production experience includes technical art, 3D asset production, scene assembly, technical integration, Unity and Unreal workflows, QA support, documentation, and cross-discipline collaboration.

---

## Tooling Philosophy

I do not treat tools as isolated scripts.

A useful production tool should reduce ambiguity, communicate state clearly, prevent avoidable errors, and support repeatable decisions.

My current tooling work is built around a few principles:

* understand the production problem before building the feature;
* learn the pipeline deeply enough to respect its constraints;
* identify hidden failure modes before they become expensive bugs;
* separate raw input, classification, execution, validation, and handoff;
* protect sensitive or ambiguous data instead of forcing unsafe automation;
* keep reports and test checklists close to the implementation;
* design tools that help artists move faster without lowering the technical bar.

This is why my tooling work is not limited to one environment. The specific platform, toolset, language, or pipeline can change, but the production method stays consistent: clarify the input, protect the operation, validate the result, and make the handoff traceable.

---

## Internal Quality Method

A major part of my work is internal QA before implementation.

My default approach is to red-team the workflow before trusting the tool. I look for hidden failure modes early: ambiguous input, unsafe automation, unclear ownership, repeated execution, fragile handoff, stale data, unverified output, and edge cases that can become expensive only after production pressure exposes them.

For example, before implementing a Maya scene organization tool, I mapped risks around references, instanced geometry, rig-sensitive hierarchies, display-layer visibility, long-name mutation, repeated execution, heavy-scene UI behavior, and report accuracy.

That is the standard I bring to production tooling: I do not wait for a bug to prove the risk exists. I look for the edge case, document it, and design the tool so the failure is harder to trigger.

---

## Current Direction

I am currently organizing independent tools into public documentation, case studies, GitHub repositories, and portfolio-ready releases.

Main areas of interest:

### Technical Art and Production Tools

- Technical Art
- Tools and Pipeline
- Asset Implementation
- Content Validation
- Workflow Automation
- Production UX for artists
- Production tooling across unfamiliar pipelines

### Scene, Asset, and Handoff Systems

- Scene organization and handoff systems
- Asset diagnostics
- Mesh review
- Scene-density feedback
- Edge QA standardization
- Controlled remesh workflows
- Reporting and test checklists

### Workflow Control and Validation Systems

- Workflow-control architecture
- Source-of-truth and validation systems
- Evidence-gated AI workflow design
- LLM output review and epistemic drift control
- Human decision separation
- Release-boundary control

---

## Links

* ArtStation: https://ghbanck.artstation.com
* LinkedIn: https://www.linkedin.com/in/gustavo-banck
* GitHub: https://github.com/ghbanck
* PolyCount Wizard: https://github.com/ghbanck/PolyCount-Wizard
* Maya Production Pipeliner: https://github.com/ghbanck/Maya-Production-Pipeliner
* MOI Control Gate: https://github.com/ghbanck/MOI-Control-Gate
* MOI Lite Demo: https://github.com/ghbanck/MOI-Lite-Demo
* Production Workflow Control Study: https://www.artstation.com/artwork/XJyKXl
* HS FE GuideTool: https://www.artstation.com/artwork/nJaK04
* Email: [gustavohenriquebanck@gmail.com](mailto:gustavohenriquebanck@gmail.com)
