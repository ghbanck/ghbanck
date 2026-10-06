# Gustavo Henrique Banck

**Technical Art · Systems Architecture · Game Development Pipeline · Production Tools**

I work at the intersection of Technical Art, production pipelines, tools, and systems architecture in game development.

My focus is the technical layer between Art and Engineering: building tools, defining production workflows, and designing the interfaces, validation mechanisms, and shared foundations that make asset handoffs more explicit, reusable, and reliable.

I approach recurring production problems as systems problems. Rather than solving the same class of issue again through isolated scripts or manual procedures, I look for the responsibilities that can be made explicit, reusable, testable, and maintainable.

My background in art and content production gives me a practical view of pipeline engineering: infrastructure only creates value when it reduces friction for the people who use it.

---

## Direction

### Professional

Game development infrastructure that artists can trust:

* production pipelines built on shared foundations: data contracts, stable asset IDs, manifests, intake and validation gates;
* artist-facing tools that are non-destructive by design: staging first, dry run before mutation, undo, readable reports;
* runtime integration: the path from DCC output to engine-ready content;
* validation and automation in CI, so that a rule is checked by the pipeline instead of remembered by a person.

### Study

What I am studying and building now:

* **Texture-space tooling in Blender:** resampling, tangent-space normal maps and atlasing, through UV Carry;
* **Maya-native production tooling:** safety-aware scene organization and handoff, through Maya Production Pipeliner;
* **Pipeline architecture:** layered pipelines, data contracts, acceptance gates and decision registers;
* **2D animation and engine delivery:** frame decimation by optical flow, PNG and GIF sequences, Spine automation through its CLI, bitmap fonts for Godot;
* **Evidence-gated AI workflows:** what a workflow may trust before model output becomes action, and epistemic drift in LLMs, through MOI Control Gate and the article [Deriva Epistemológica em LLMs](https://www.linkedin.com/in/gustavo-banck/recent-activity/articles/);
* **Native Windows applications:** Direct3D 11 and DirectComposition rendering, layered windows, portable single-file releases.

Current focus: Technical Art · Production Pipelines · Tools Development · Systems Architecture · Runtime Integration · Validation & Automation

---

## Selected Work

### Public Projects

| Project                       | Type                                             | Focus                                                                                                                                              | Status                                |
| ----------------------------- | ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| **UV Carry**                  | Blender Add-on                                   | Move UVs. Carry Textures.: move, rotate or scale UV islands and the texture follows them, in every image of their materials                        | Lite free (GPL), UV Carry paid       |
| **PolyCount Wizard**          | Public Production Tool / Documented Tooling Case | Mesh budget diagnostics, scene density review, object-level validation                                                                             | Public documentation / private source |
| **Maya Production Pipeliner** | Tooling Lab / Production Scaffold                | Maya scene organization, safety-aware routing, production handoff clarity                                                                          | Public scaffold / in development      |
| **MOI Control Gate**          | Public Architecture / Control-Gate Thesis        | Control-before-automation architecture for evidence boundaries, LLM output review, workflow trust, release boundaries, and epistemic drift control | Public architecture                   |
| **MOI Lite Demo**             | Public Demo / Façade Layer                       | Public-facing demonstration of MOI Lite’s evidence-gated demo layer; a small, sanitized slice of the private runtime’s control logic               | Public demo                           |

### Desktop Projects

| Project                   | Type                               | Focus                                                                                         | Status         |
| ------------------------- | ---------------------------------- | --------------------------------------------------------------------------------------------- | -------------- |
| **GameOfLife Wallpaper**  | Windows Desktop App (Python)       | Conway's Game of Life as a live, drawable wallpaper behind the desktop icons, Direct3D 11      | Public release |
| **Vaporwave Toons**       | Windows Desktop App (C# / .NET)    | XPenguins' Vaporwave theme ported to Windows 10/11: toons that walk, climb and ride on windows | Public release |

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

### UV Carry

<p>
  <img alt="License: GPL-3.0-or-later" src="https://img.shields.io/badge/license-GPL--3.0--or--later-2ea44f">
  <img alt="Platform: Blender add-on" src="https://img.shields.io/badge/platform-Blender%20add--on-0078d4">
  <img alt="Blender version: 5.1" src="https://img.shields.io/badge/blender-5.1-e87d0d">
</p>

**Move UVs. Carry Textures.**

Blender add-on: move, rotate, scale or pack complete UV islands with Blender's own tools, press Ctrl+Enter, and every texture of their materials follows them, even into one atlas made from many materials.

Moving a UV island after texturing normally leaves the painted texture behind, and means baking or painting again. UV Carry remembers where the islands started, lets Blender move them as it always does, and does the texture work once, at Ctrl+Enter: each island's texels are read where it started and written where it ended, a move by whole texels is copied bit for bit, rotations and scales are resampled from the island's own texels only, and Ctrl+Z undoes the texels, the UVs and the materials together. Tangent-space normal maps keep their relief when an island turns, and Carry Into merges the islands of several materials into one atlas.

Tested with Blender 5.1.1 on Windows 11.

<a href="https://github.com/ghbanck/UV-Carry">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/UV-Carry">
  <img src="https://img.shields.io/badge/UV_Carry-9AD7D2?style=for-the-badge" alt="UV Carry">
</a>

#### UV Carry Lite

<p>
  <a href="https://github.com/ghbanck/UV-Carry-Lite/releases"><img alt="Release" src="https://img.shields.io/github/v/release/ghbanck/UV-Carry-Lite?include_prereleases&sort=semver&label=release&color=d29922"></a>
</p>

The free edition, GPL-3.0-or-later: carries of one or several islands, padding, undo and saving, without normal maps. Its public repository holds the add-on and its releases.

<a href="https://github.com/ghbanck/UV-Carry-Lite">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/UV-Carry-Lite/releases">
  <img src="https://img.shields.io/badge/Download_UV_Carry_Lite-9AD7D2?style=for-the-badge" alt="Download UV Carry Lite">
</a>

---

### PolyCount Wizard

<p>
  <a href="https://github.com/ghbanck/PolyCount-Wizard/blob/main/NOTICE.md"><img alt="License: all rights reserved" src="https://img.shields.io/badge/license-all%20rights%20reserved-6e7681"></a>
  <img alt="Platform: Blender" src="https://img.shields.io/badge/platform-Blender-0078d4">
  <a href="https://github.com/ghbanck/PolyCount-Wizard/blob/main/TESTING_STATUS.md"><img alt="QA: Blender 5.1.1" src="https://img.shields.io/badge/QA-Blender%205.1.1-8250df"></a>
  <a href="https://github.com/ghbanck/PolyCount-Wizard/blob/main/TESTING_STATUS.md"><img alt="Runtime QA: 27 pass, 0 fail" src="https://img.shields.io/badge/runtime%20QA-27%20pass%20%7C%200%20fail-3fb950"></a>
  <img alt="Source: private" src="https://img.shields.io/badge/source-private-6e7681">
</p>

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

<p>
  <a href="https://github.com/ghbanck/Maya-Production-Pipeliner/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-3fb950"></a>
  <img alt="Platform: Autodesk Maya" src="https://img.shields.io/badge/platform-Autodesk%20Maya-0078d4">
  <img alt="Python: mayapy" src="https://img.shields.io/badge/python-mayapy-3776ab">
  <img alt="Smoke validated: Maya 2027.1" src="https://img.shields.io/badge/smoke%20validated-Maya%202027.1-8250df">
  <img alt="Status: not release-ready" src="https://img.shields.io/badge/status-not%20release--ready-d29922">
</p>

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

<p>
  <a href="https://github.com/ghbanck/MOI-Control-Gate/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-3fb950"></a>
  <img alt="Repository: docs only" src="https://img.shields.io/badge/repository-docs%20only-8250df">
  <a href="https://github.com/ghbanck/MOI-Lite-Demo"><img alt="Related: MOI-Lite-Demo" src="https://img.shields.io/badge/related-MOI--Lite--Demo-0078d4"></a>
</p>

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

<p>
  <a href="https://github.com/ghbanck/MOI-Lite-Demo/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-3fb950"></a>
  <img alt="Python 3.10+" src="https://img.shields.io/badge/python-3.10%2B-3776ab">
  <img alt="Framework: FastAPI" src="https://img.shields.io/badge/framework-FastAPI-009688">
  <img alt="Mode: public demo" src="https://img.shields.io/badge/mode-public%20demo-8250df">
  <a href="https://github.com/ghbanck/MOI-Lite-Demo/actions/workflows/ci.yml"><img alt="CI" src="https://github.com/ghbanck/MOI-Lite-Demo/actions/workflows/ci.yml/badge.svg"></a>
</p>

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


## Desktop Projects

### GameOfLife Wallpaper

<p>
  <a href="https://github.com/ghbanck/GameOfLife-Wallpaper/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-3fb950"></a>
  <img alt="Platform: Windows 10 | 11" src="https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078d4">
  <img alt="Python 3.10+" src="https://img.shields.io/badge/python-3.10%2B-3776ab">
  <img alt="Renderer: Direct3D 11" src="https://img.shields.io/badge/renderer-Direct3D%2011-8250df">
  <a href="https://github.com/ghbanck/GameOfLife-Wallpaper/actions/workflows/ci.yml"><img alt="CI" src="https://github.com/ghbanck/GameOfLife-Wallpaper/actions/workflows/ci.yml/badge.svg"></a>
</p>

Conway's Game of Life running as a live Windows wallpaper, behind the desktop icons and never covering an application.

A draw mode toggled by hotkey or tray icon turns desktop clicks into cells while every other click still goes where it always did. Rendering runs on Direct3D 11 and DirectComposition, and the simulation pauses on its own when nobody can see it: covered desktop, full-screen apps, locked session, display off, or battery saver.

It ships with a ~4,800-pattern library from the Life Lexicon and LifeWiki, saved worlds, RLE / `.cells` / Life 1.06 import, eight palettes, alternative rules, and English and Portuguese UI. Distributed as a single portable `.exe`, with tests in CI.

<a href="https://github.com/ghbanck/GameOfLife-Wallpaper">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/GameOfLife-Wallpaper">
  <img src="https://img.shields.io/badge/GameOfLife_Wallpaper-9AD7D2?style=for-the-badge" alt="GameOfLife Wallpaper">
</a>

---

### Vaporwave Toons

<p>
  <a href="https://github.com/ghbanck/Vaporwave-Toons/blob/main/LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-3fb950"></a>
  <img alt="Platform: Windows 10 | 11" src="https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078d4">
  <img alt="Runtime: .NET Framework 4.8" src="https://img.shields.io/badge/runtime-.NET%20Framework%204.8-512bd4">
  <img alt="Renderer: layered windows" src="https://img.shields.io/badge/renderer-layered%20windows-8250df">
  <a href="https://github.com/ghbanck/Vaporwave-Toons/actions/workflows/build.yml"><img alt="Build" src="https://github.com/ghbanck/Vaporwave-Toons/actions/workflows/build.yml/badge.svg"></a>
  <a href="https://github.com/ghbanck/Vaporwave-Toons/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/ghbanck/Vaporwave-Toons?color=ff71ce&label=release"></a>
</p>

The Vaporwave theme for XPenguins, brought to Windows 10 and 11.

Eight toons drop onto the desktop, walk along title bars, climb window edges, ride windows as they move, and get squashed when a window is dragged onto them. The port adapts XPenguins' behavior to how Windows is actually used: maximized and snapped windows count as background, only a moving window squashes, and falling toons accelerate under gravity.

Written in C# on .NET Framework 4.8 as a single small `.exe`, with no installer, no admin rights, a tray menu for every option, and English and Portuguese UI.

<a href="https://github.com/ghbanck/Vaporwave-Toons">
  <img src="https://img.shields.io/badge/View_Repository-111111?style=for-the-badge" alt="View Repository">
</a>
<a href="https://github.com/ghbanck/Vaporwave-Toons">
  <img src="https://img.shields.io/badge/Vaporwave_Toons-9AD7D2?style=for-the-badge" alt="Vaporwave Toons">
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

## Links

* UV Carry: https://github.com/ghbanck/UV-Carry
* UV Carry Lite: https://github.com/ghbanck/UV-Carry-Lite
* ArtStation: https://www.artstation.com/ghbanck
* LinkedIn: https://www.linkedin.com/in/gustavo-banck
* GitHub: https://github.com/ghbanck
* PolyCount Wizard: https://github.com/ghbanck/PolyCount-Wizard
* Maya Production Pipeliner: https://github.com/ghbanck/Maya-Production-Pipeliner
* MOI Control Gate: https://github.com/ghbanck/MOI-Control-Gate
* MOI Lite Demo: https://github.com/ghbanck/MOI-Lite-Demo
* GameOfLife Wallpaper: https://github.com/ghbanck/GameOfLife-Wallpaper
* Vaporwave Toons: https://github.com/ghbanck/Vaporwave-Toons
* Production Workflow Control Study: https://www.artstation.com/artwork/XJyKXl
* HS FE GuideTool: https://www.artstation.com/artwork/nJaK04
* Email: [gustavohenriquebanck@gmail.com](mailto:gustavohenriquebanck@gmail.com)
