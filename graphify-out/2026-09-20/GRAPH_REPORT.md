# Graph Report - outbound V0.1  (2026-09-20)

## Corpus Check
- 15 files · ~144,285 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 31 nodes · 25 edges · 9 communities (4 shown, 5 thin omitted)
- Extraction: 72% EXTRACTED · 28% INFERRED · 0% AMBIGUOUS · INFERRED: 7 edges (avg confidence: 0.81)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Physical Equipment & Markers
- Core System Architecture
- Delivery Status Workflow
- Warehouse Operations
- Product Catalog - Markers
- Handling Equipment
- Precision Markers
- Marker Variants
- Operations Team

## God Nodes (most connected - your core abstractions)
1. `Outbound Control Tower` - 9 edges
2. `Marker Types` - 4 edges
3. `Delivery Status Workflow` - 4 edges
4. `Cone Marker Allocation System` - 3 edges
5. `Warehouse Logistics Operations` - 3 edges
6. `Delivery Management System` - 2 edges
7. `Traffic Cone 30cm` - 2 edges
8. `Saucer Disc Topper` - 2 edges
9. `Hexagonal Pro HX Saucer 200mm` - 2 edges
10. `Picking Status` - 2 edges

## Surprising Connections (you probably didn't know these)
- `Jungheinrich VNA Reach Truck` --semantically_similar_to--> `Picking Status`  [INFERRED] [semantically similar]
  VNA.webp → Outbound Control Tower - DEMO.html
- `Warehouse Pick Label with Delivery Information` --references--> `Delivery Management System`  [INFERRED]
  pick label.jpg → Outbound Control Tower - DEMO.html
- `Jungheinrich EPT Electric Pallet Truck` --conceptually_related_to--> `Warehouse Logistics Operations`  [INFERRED]
  EPT.jpg → Outbound Control Tower - DEMO.html
- `VNA Reach Truck - Side View` --conceptually_related_to--> `Warehouse Logistics Operations`  [INFERRED]
  VNA 1.jpg → Outbound Control Tower - DEMO.html
- `Traffic Cone 30cm` --references--> `Mooffz Training Cones 30cm with Holes`  [EXTRACTED]
  Outbound Control Tower - DEMO.html → Mooffz.png

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Cone Marker System Components** — outbound_control_tower_demo_html_traffic_cone, outbound_control_tower_demo_html_saucer_disc, outbound_control_tower_demo_html_hexagonal_saucer [EXTRACTED 1.00]
- **Warehouse Equipment for Operations** — ept_jpg_jungheinrich_ept, vna_1_jpg_vna_reach_truck_side_view, vna_webp_jungheinrich_vna_reach_truck [INFERRED 0.80]
- **Delivery Status Workflow Progression** — outbound_control_tower_demo_html_status_lane_allocated, outbound_control_tower_demo_html_status_lane_picking, outbound_control_tower_demo_html_status_lane_packing [EXTRACTED 1.00]

## Communities (9 total, 5 thin omitted)

### Community 0 - "Physical Equipment & Markers"
Cohesion: 0.20
Nodes (10): Cawila Saucer Disc Cones - Classic M Set, Mooffz Training Cones 30cm with Holes, Color-Based Marker Identification System, Cone Marker Allocation System, Color Confusability Rules for Readability, Hexagonal Pro HX Saucer 200mm, Marker Types, Saucer Disc Topper (+2 more)

### Community 1 - "Core System Architecture"
Cohesion: 0.25
Nodes (8): Delivery Management System, Inventory Tracking and Reservation Logic, Live Multi-Screen Synchronization, Outbound Control Tower, Pick Label, Sevenum Warehouse, User Roles, Warehouse Pick Label with Delivery Information

### Community 2 - "Delivery Status Workflow"
Cohesion: 0.40
Nodes (5): Delivery Status Workflow, Allocated Status, Packing Status, Picking Status, Jungheinrich VNA Reach Truck

### Community 3 - "Warehouse Operations"
Cohesion: 0.67
Nodes (3): Jungheinrich EPT Electric Pallet Truck, Warehouse Logistics Operations, VNA Reach Truck - Side View

## Knowledge Gaps
- **17 isolated node(s):** `Pick Label`, `Allocated Status`, `Packing Status`, `User Roles`, `Sevenum Warehouse` (+12 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 20 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **5 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Outbound Control Tower` connect `Core System Architecture` to `Physical Equipment & Markers`, `Delivery Status Workflow`, `Warehouse Operations`?**
  _High betweenness centrality (0.554) - this node is a cross-community bridge._
- **Why does `Cone Marker Allocation System` connect `Physical Equipment & Markers` to `Core System Architecture`?**
  _High betweenness centrality (0.363) - this node is a cross-community bridge._
- **Are the 3 inferred relationships involving `Warehouse Logistics Operations` (e.g. with `Jungheinrich EPT Electric Pallet Truck` and `Outbound Control Tower`) actually correct?**
  _`Warehouse Logistics Operations` has 3 INFERRED edges - model-reasoned connections that need verification._
- **What connects `Pick Label`, `Allocated Status`, `Packing Status` to the rest of the system?**
  _17 weakly-connected nodes found - possible documentation gaps or missing edges._