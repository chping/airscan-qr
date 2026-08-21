# Graph Report - airscan-qr  (2026-08-21)

## Corpus Check
- Corpus is ~5,049 words - fits in a single context window. You may not need a graph.

## Summary
- 77 nodes · 117 edges · 10 communities (9 shown, 1 thin omitted)
- Extraction: 81% EXTRACTED · 19% INFERRED · 0% AMBIGUOUS · INFERRED: 22 edges (avg confidence: 0.86)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Fountain Protocol
- jsQR Library
- Receive Reassembly
- Segmented Send Flow
- Deployment and Docs
- QR Scanning
- Legacy Sender Flow
- QRious Library
- Sender Formatting

## God Nodes (most connected - your core abstractions)
1. `handleFountainPacket` - 8 edges
2. `tick` - 7 edges
3. `processPacket` - 7 edges
4. `finalizeSegment` - 7 edges
5. `tick` - 7 edges
6. `d()` - 6 edges
7. `startFileSegment` - 6 edges
8. `startFileSegment` - 6 edges
9. `n()` - 5 edges
10. `c()` - 5 edges

## Surprising Connections (you probably didn't know these)
- `startFileSegment` --semantically_similar_to--> `startFileSegment`  [INFERRED] [semantically similar]
  index.html → sender.html
- `ASQ3 Fountain Protocol` --semantically_similar_to--> `ASQ3 Fountain Protocol`  [INFERRED] [semantically similar]
  index.html → sender.html
- `Sequential Segmented Transfer` --semantically_similar_to--> `Sequential Segmented Transfer`  [INFERRED] [semantically similar]
  index.html → sender.html
- `beginPacketStream` --semantically_similar_to--> `beginPacketStream`  [INFERRED] [semantically similar]
  index.html → sender.html
- `tick` --semantically_similar_to--> `tick`  [INFERRED] [semantically similar]
  index.html → sender.html

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **ASQ3 End-to-End Fountain Transfer** — index_beginpacketstream, index_tick, index_handlefountainpacket, index_processpacket, index_finalizesegment [INFERRED 0.95]
- **Shared Sender Implementation** — index_startfilesegment, index_beginpacketstream, index_tick, sender_startfilesegment, sender_beginpacketstream, sender_tick [INFERRED 0.95]
- **GitHub Pages Static Bundle** — _github_workflows_static_upload_artifact, index_airscan_qr_fountain, sender_airscan_qr_fountain_sender, readme_airscan_qr [EXTRACTED 1.00]

## Communities (10 total, 1 thin omitted)

### Community 0 - "Fountain Protocol"
Cohesion: 0.18
Nodes (16): ASQ3 Fountain Protocol, beginPacketStream, processPacket, tick, Utils.getDegree, Utils.PRNG, Utils.u2b, Utils.xor (+8 more)

### Community 1 - "jsQR Library"
Cohesion: 0.38
Nodes (9): a(), B(), c(), d(), i(), k(), l(), n() (+1 more)

### Community 2 - "Receive Reassembly"
Cohesion: 0.29
Nodes (11): finalizeRecv, finalizeSegment, formatSize, handleFountainPacket, In-Memory File Reassembly, renderRecvSegments, SHA-256 Segment Integrity, showRecvNotice (+3 more)

### Community 3 - "Segmented Send Flow"
Cohesion: 0.28
Nodes (9): Sequential Segmented Transfer, finishCurrentTransfer, newTransferId, renderSenderSegments, Sequential Segmented Transfer, setSenderLocked, sha256Hex, startFileSegment (+1 more)

### Community 4 - "Deployment and Docs"
Cohesion: 0.29
Nodes (8): Deploy Job, GitHub Pages Deployment, Upload Entire Repository Artifact, AirScan-QR Fountain Application, airscan-qr, Pure Localized Version, topcss AirScan-QR, AirScan-QR Fountain Sender

### Community 5 - "QR Scanning"
Cohesion: 0.33
Nodes (7): abandonReceive, clearReceiveSession, Multi-Region QR Scanning, scanLoop, scheduleScan, startScanner, startScreenScanner

### Community 6 - "Legacy Sender Flow"
Cohesion: 0.38
Nodes (7): finishCurrentTransfer, newTransferId, renderSenderSegments, setSenderLocked, sha256Hex, startFileSegment, startSending

### Community 7 - "QRious Library"
Cohesion: 0.70
Nodes (3): e(), i(), t()

## Knowledge Gaps
- **14 isolated node(s):** `GitHub Pages Deployment`, `AirScan-QR Fountain Application`, `SHA-256 Segment Integrity`, `Utils.u2b`, `Utils.b2u` (+9 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `handleFountainPacket` connect `Receive Reassembly` to `Fountain Protocol`, `Segmented Send Flow`, `QR Scanning`?**
  _High betweenness centrality (0.158) - this node is a cross-community bridge._
- **Why does `ASQ3 Fountain Protocol` connect `Fountain Protocol` to `Receive Reassembly`?**
  _High betweenness centrality (0.085) - this node is a cross-community bridge._
- **Why does `startFileSegment` connect `Legacy Sender Flow` to `Fountain Protocol`, `Segmented Send Flow`?**
  _High betweenness centrality (0.084) - this node is a cross-community bridge._
- **Are the 2 inferred relationships involving `handleFountainPacket` (e.g. with `ASQ3 Fountain Protocol` and `Sequential Segmented Transfer`) actually correct?**
  _`handleFountainPacket` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `tick` (e.g. with `ASQ3 Fountain Protocol` and `tick`) actually correct?**
  _`tick` has 2 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `tick` (e.g. with `tick` and `ASQ3 Fountain Protocol`) actually correct?**
  _`tick` has 2 INFERRED edges - model-reasoned connections that need verification._
- **What connects `GitHub Pages Deployment`, `AirScan-QR Fountain Application`, `SHA-256 Segment Integrity` to the rest of the system?**
  _14 weakly-connected nodes found - possible documentation gaps or missing edges._