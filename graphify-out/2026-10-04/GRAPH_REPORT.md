# Graph Report - outbound V0.1  (2026-09-22)

## Corpus Check
- 15 files · ~175,777 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 175 nodes · 156 edges · 25 communities (13 shown, 12 thin omitted)
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `f94d2dbc`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Cawila Saucer Disc Cones - Classic M Set
- Warehouse Pick Label with Delivery Information
- Jungheinrich VNA Reach Truck
- Jungheinrich EPT Electric Pallet Truck
- Cawila Marker Cones Product Display
- Jungheinrich EPT - Elevated View
- Precision Saucer Discs in Multiple Colors
- Precision Hexagonal Topper - Red
- VNA Operator in Warehouse
- CLAUDE.md
- Test-Driven Development
- Code Simplification
- Frontend UI Engineering
- Git Workflow and Versioning
- Code Review and Quality
- Debugging and Error Recovery
- The Triage Checklist
- Core Principles
- Writing Good Tests
- The Five-Axis Review
- Review Process
- Accessibility (WCAG 2.1 AA)
- Mooffz Training Cones 30cm with Holes
- Precision Pro HX Saucer Cones Product Page
- VNA Reach Truck - Side View

## God Nodes (most connected - your core abstractions)
1. `Code Review and Quality` - 19 edges
2. `Git Workflow and Versioning` - 15 edges
3. `Test-Driven Development` - 15 edges
4. `Frontend UI Engineering` - 13 edges
5. `Debugging and Error Recovery` - 12 edges
6. `Code Simplification` - 9 edges
7. `The Triage Checklist` - 7 edges
8. `Core Principles` - 7 edges
9. `Writing Good Tests` - 7 edges
10. `The Five-Axis Review` - 6 edges

## Surprising Connections (you probably didn't know these)
- None detected - all connections are within the same source files.

## Hyperedges (group relationships)
- **Warehouse Equipment for Operations** — ept_jpg_jungheinrich_ept, vna_1_jpg_vna_reach_truck_side_view, vna_webp_jungheinrich_vna_reach_truck [INFERRED 0.80]

## Communities (25 total, 12 thin omitted)

### Community 9 - "CLAUDE.md"
Cohesion: 0.29
Nodes (5): Architecture, Commands, Delivery status pipeline, graphify, What this is

### Community 10 - "Test-Driven Development"
Cohesion: 0.09
Nodes (22): Browser Testing with DevTools, Common Rationalizations, Decision Guide, Discover the Stack First, Overview, Red Flags, Security Boundaries, See Also (+14 more)

### Community 11 - "Code Simplification"
Cohesion: 0.09
Nodes (21): 1. Preserve Behavior Exactly, 2. Follow Project Conventions, 3. Prefer Clarity Over Cleverness, 4. Maintain Balance, 5. Scope to What Changed, Code Simplification, Common Rationalizations, Language-Specific Guidance (+13 more)

### Community 12 - "Frontend UI Engineering"
Cohesion: 0.10
Nodes (19): Avoid the AI Aesthetic, Color, Common Rationalizations, Component Architecture, Component Patterns, Design System Adherence, File Structure, Frontend UI Engineering (+11 more)

### Community 13 - "Git Workflow and Versioning"
Cohesion: 0.10
Nodes (19): Branch Naming, Branching Strategy, Change Summaries, Common Rationalizations, Feature Branches, Git Workflow and Versioning, Handling Generated Files, Keep a changelog written for humans (+11 more)

### Community 14 - "Code Review and Quality"
Cohesion: 0.11
Nodes (17): Change Descriptions, Change Sizing, Code Review and Quality, Common Rationalizations, Dead Code Hygiene, Dependency Discipline, Handling Disagreements, Honesty in Review (+9 more)

### Community 15 - "Debugging and Error Recovery"
Cohesion: 0.13
Nodes (14): Build Failure Triage, Common Rationalizations, Debugging and Error Recovery, Error-Specific Patterns, Instrumentation Guidelines, Overview, Red Flags, Runtime Error Triage (+6 more)

### Community 16 - "The Triage Checklist"
Cohesion: 0.29
Nodes (7): Step 1: Reproduce, Step 2: Localize, Step 3: Reduce, Step 4: Fix the Root Cause, Step 5: Guard Against Recurrence, Step 6: Verify End-to-End, The Triage Checklist

### Community 17 - "Core Principles"
Cohesion: 0.29
Nodes (7): 1. Commit Early, Commit Often, 2. Atomic Commits, 3. Descriptive Messages, 4. Keep Concerns Separate, 5. Size Your Changes, Core Principles, Trunk-Based Development (Recommended)

### Community 18 - "Writing Good Tests"
Cohesion: 0.29
Nodes (7): DAMP Over DRY in Tests, Name Tests Descriptively, One Assertion Per Concept, Prefer Real Implementations Over Mocks, Test State, Not Interactions, Use the Arrange-Act-Assert Pattern, Writing Good Tests

### Community 19 - "The Five-Axis Review"
Cohesion: 0.33
Nodes (6): 1. Correctness, 2. Readability & Simplicity, 3. Architecture, 4. Security, 5. Performance, The Five-Axis Review

### Community 20 - "Review Process"
Cohesion: 0.33
Nodes (6): Review Process, Step 1: Understand the Context, Step 2: Review the Tests First, Step 3: Review the Implementation, Step 4: Categorize Findings, Step 5: Verify the Verification

### Community 21 - "Accessibility (WCAG 2.1 AA)"
Cohesion: 0.40
Nodes (5): Accessibility (WCAG 2.1 AA), ARIA Labels, Focus Management, Keyboard Navigation, Meaningful Empty and Error States

## Knowledge Gaps
- **143 isolated node(s):** `Overview`, `When to Use`, `1. Correctness`, `2. Readability & Simplicity`, `3. Architecture` (+138 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 150 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **12 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Code Review and Quality` connect `Code Review and Quality` to `The Five-Axis Review`, `Review Process`?**
  _High betweenness centrality (0.025) - this node is a cross-community bridge._
- **Why does `Test-Driven Development` connect `Test-Driven Development` to `Writing Good Tests`?**
  _High betweenness centrality (0.025) - this node is a cross-community bridge._
- **Why does `Git Workflow and Versioning` connect `Git Workflow and Versioning` to `Core Principles`?**
  _High betweenness centrality (0.020) - this node is a cross-community bridge._
- **What connects `Overview`, `When to Use`, `1. Correctness` to the rest of the system?**
  _143 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Test-Driven Development` be split into smaller, more focused modules?**
  _Cohesion score 0.08695652173913043 - nodes in this community are weakly interconnected._
- **Should `Code Simplification` be split into smaller, more focused modules?**
  _Cohesion score 0.09090909090909091 - nodes in this community are weakly interconnected._
- **Should `Frontend UI Engineering` be split into smaller, more focused modules?**
  _Cohesion score 0.1 - nodes in this community are weakly interconnected._