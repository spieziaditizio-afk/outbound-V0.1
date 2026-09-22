# Graph Report - outbound V0.1  (2026-09-20)

## Corpus Check
- 2 files · ~145,162 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 38 nodes · 31 edges · 10 communities (5 shown, 5 thin omitted)
- Extraction: 77% EXTRACTED · 23% INFERRED · 0% AMBIGUOUS · INFERRED: 7 edges (avg confidence: 0.81)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `32b1ee44`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- Marker Types
- Outbound Control Tower
- Delivery Status Workflow
- Warehouse Logistics Operations
- Cawila Marker Cones Product Display
- Jungheinrich EPT - Elevated View
- Precision Saucer Discs in Multiple Colors
- Precision Hexagonal Topper - Red
- VNA Operator in Warehouse
- CLAUDE.md

## God Nodes (most connected - your core abstractions)
1. `Outbound Control Tower` - 9 edges
2. `Marker Types` - 4 edges
3. `Delivery Status Workflow` - 4 edges
4. `Cone Marker Allocation System` - 3 edges
5. `Warehouse Logistics Operations` - 3 edges
6. `Architecture` - 2 edges
7. `Hexagonal Pro HX Saucer 200mm` - 2 edges
8. `Saucer Disc Topper` - 2 edges
9. `Traffic Cone 30cm` - 2 edges
10. `Color-Based Marker Identification System` - 2 edges

## Surprising Connections (you probably didn't know these)
- `Jungheinrich VNA Reach Truck` --semantically_similar_to--> `Picking Status`  [INFERRED] [semantically similar]
  VNA.webp → Outbound Control Tower - DEMO.html
- `Warehouse Pick Label with Delivery Information` --references--> `Delivery Management System`  [INFERRED]
  pick label.jpg → Outbound Control Tower - DEMO.html
- `Jungheinrich EPT Electric Pallet Truck` --conceptually_related_to--> `Warehouse Logistics Operations`  [INFERRED]
  EPT.jpg → Outbound Control Tower - DEMO.html
- `VNA Reach Truck - Side View` --conceptually_related_to--> `Warehouse Logistics Operations`  [INFERRED]
  VNA 1.jpg → Outbound Control Tower - DEMO.html
- `Hexagonal Pro HX Saucer 200mm` --references--> `Precision Pro HX Saucer Cones Product Page`  [EXTRACTED]
  Outbound Control Tower - DEMO.html → precision 2.png

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Delivery Status Workflow Progression** — outbound_control_tower_demo_html_status_lane_allocated, outbound_control_tower_demo_html_status_lane_picking, outbound_control_tower_demo_html_status_lane_packing [EXTRACTED 1.00]
- **Cone Marker System Components** — outbound_control_tower_demo_html_traffic_cone, outbound_control_tower_demo_html_saucer_disc, outbound_control_tower_demo_html_hexagonal_saucer [EXTRACTED 1.00]
- **Warehouse Equipment for Operations** — ept_jpg_jungheinrich_ept, vna_1_jpg_vna_reach_truck_side_view, vna_webp_jungheinrich_vna_reach_truck [INFERRED 0.80]

## Communities (10 total, 5 thin omitted)

### Community 0 - "Marker Types"
Cohesion: 0.20
Nodes (10): Cawila Saucer Disc Cones - Classic M Set, Mooffz Training Cones 30cm with Holes, Color-Based Marker Identification System, Cone Marker Allocation System, Color Confusability Rules for Readability, Hexagonal Pro HX Saucer 200mm, Marker Types, Saucer Disc Topper (+2 more)

### Community 1 - "Outbound Control Tower"
Cohesion: 0.25
Nodes (8): Delivery Management System, Inventory Tracking and Reservation Logic, Live Multi-Screen Synchronization, Outbound Control Tower, Pick Label, Sevenum Warehouse, User Roles, Warehouse Pick Label with Delivery Information

### Community 2 - "Delivery Status Workflow"
Cohesion: 0.40
Nodes (5): Delivery Status Workflow, Allocated Status, Packing Status, Picking Status, Jungheinrich VNA Reach Truck

### Community 3 - "Warehouse Logistics Operations"
Cohesion: 0.67
Nodes (3): Jungheinrich EPT Electric Pallet Truck, Warehouse Logistics Operations, VNA Reach Truck - Side View

### Community 9 - "CLAUDE.md"
Cohesion: 0.29
Nodes (5): Architecture, Commands, Delivery status pipeline, graphify, What this is

## Knowledge Gaps
- **21 isolated node(s):** `What this is`, `Commands`, `Delivery status pipeline`, `graphify`, `Cawila Saucer Disc Cones - Classic M Set` (+16 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 25 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **5 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Outbound Control Tower` connect `Outbound Control Tower` to `Marker Types`, `Delivery Status Workflow`, `Warehouse Logistics Operations`?**
  _High betweenness centrality (0.362) - this node is a cross-community bridge._
- **Why does `Cone Marker Allocation System` connect `Marker Types` to `Outbound Control Tower`?**
  _High betweenness centrality (0.237) - this node is a cross-community bridge._
- **Are the 3 inferred relationships involving `Warehouse Logistics Operations` (e.g. with `Jungheinrich EPT Electric Pallet Truck` and `Outbound Control Tower`) actually correct?**
  _`Warehouse Logistics Operations` has 3 INFERRED edges - model-reasoned connections that need verification._
- **What connects `What this is`, `Commands`, `Delivery status pipeline` to the rest of the system?**
  _21 weakly-connected nodes found - possible documentation gaps or missing edges._