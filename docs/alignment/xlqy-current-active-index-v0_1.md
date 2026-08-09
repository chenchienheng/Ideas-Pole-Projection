# XLQY Current Active Index v0.1

Status: Candidate / Current Active Index / Cleanup Branch / No Runtime / No External Writeback
Use As: current active map for QHA/LOR workface reading, public-boundary review, and cleanup planning
Do Not Use As: approved truth, live control home, release approval, merge approval, or closeout

## Core

This index lists the currently active XLQY workface files for QHA reading. Older role drafts and return packets should later be marked `ACTIVE / REFERENCE / SUPERSEDED / MOVE_CANDIDATE / ARCHIVE_CANDIDATE`.

XL10 is the public generic schema and coordination home. Live current state, private source context, complete window returns, and native evidence stay in their authorized carriers and are referenced rather than mirrored here.

## Active Current

```yaml
XLQY_Current_Active:
  alignment:
    - "docs/alignment/xlqy-internal-alignment-map-v0_1.md"
    - "docs/alignment/xlqy-current-active-index-v0_1.md"
    - "docs/alignment/xl10-tri-carrier-public-boundary-v0_1.md"
  dispatch:
    - "docs/dispatch/qha-daily-dispatch-template-v0_1.md"
    - "docs/dispatch/qha-lor-chain-experiment-dispatch-2026-07-07-v0_1.md"
  circulation_protocol:
    - "docs/circulation/qha-mutual-circulation-schedule-v0_1.md"
    - "docs/protocols/lor-mutual-read-and-promote-protocol-v0_1.md"
  identity:
    - "docs/identity/xuanling-qha-self-addressing-rule-v0_1.md"
  returns:
    - "docs/returns/qinyi-lor-signal-return-template.md"
    - "docs/returns/missing-return-hook-request-template-v0_1.md"
  audit:
    - "docs/audit/aki-return-audit-spec-v0_1.md"
    - "docs/audit/public-safe-output-checklist-v0_1.md"
  build_packets:
    - "docs/build-packets/hazumi-build-packet-coretri-ocf-v0_1.md"
  role_maps:
    - "docs/role-maps/qha-nutrient-absorption-role-map-v0_1.md"
  context:
    - "docs/context/qinyi-mainchat-lor-return-routing-v0_1.md"
```

## Current Repository Boundary

```yaml
Current_Role:
  - generic coordination schema home
  - reusable task and return templates
  - public-safe audit and bounded-build patterns

Not_Current_Role:
  - private live-control home
  - complete working-return mirror
  - company or customer data carrier
  - runtime or deployment repository
```

Read `docs/alignment/xl10-tri-carrier-public-boundary-v0_1.md` before promoting any newer content into this Active Index.

## File-Level Review Queue

The following recent content families require exact-path inspection before they are treated as active public material:

- personal decision
- music case
- social window
- learning returns derived from protected sources
- M365 or company-adjacent build cards

Each item must be classified separately as generic, de-identified, public-safe, and public-approved. These states are not interchangeable.

## Superseded / Reference Pending

Older Qinyi/Hazumi/Aki role labels, legacy multi-window schedule notes, and long return packets must be reviewed later and marked `ACTIVE / REFERENCE / SUPERSEDED / MOVE_CANDIDATE / ARCHIVE_CANDIDATE`.

## Red Doors

- Current Active != Approved Truth
- Active Index != Complete Inventory
- Generic Pattern != Original Source
- De-identified != Public-approved
- Role Map != Final Authority
- Build Packet != Runtime
- Audit Note != Closeout
- Dispatch != Approval
- GitHub Commit != Current Operational State

## Final Rule

QHA should read this index before expanding XLQY details. Role windows should be manually expanded only when QHA or Vitas assigns them. XL10 versions selected generic coordination methods; it does not replace the authorized live working carrier.

## R1-05 Legacy Reader Shield

Shield state: `READER_SHIELD_NATIVE_APPLIED_PR_BRANCH`  
Scope: `cleanup/r1-current-role-index-20260714` only. The default branch is unchanged. This section grants no merge, Current, Canon, runtime, release, deletion, identity, or authority promotion.

| Reader question | Branch-scoped answer |
|---|---|
| 1. Which generation is this? | `STATUS.md` and `current_files.txt` belong to the shared pre-role-differentiation snapshot generation. This repository's target role is **Coordination / Return Projection candidate**. |
| 2. Is it Current now? | **No.** Legacy bodies are historical evidence. This role index is still a candidate on an unmerged cleanup branch. |
| 3. What was its historical function? | A shared architecture, coordination, registry, runtime-spine, and manifest baseline before repository-native role differentiation. |
| 4. Which meaning remains valid? | Historical provenance, the material names recorded at that revision, and bounded relation evidence remain readable. |
| 5. Which assumptions are no longer valid? | Completeness, one shared Current role, live runtime/control authority, same identity, Git ancestry, Canon, and deletion readiness. |
| 6. Where is the successor? | Reader-routing successor: this role index plus the public-boundary file for branch reading; no identity successor is asserted. This is not an identity-successor claim. |
| 7. What should a reader read first? | this role index, then `docs/alignment/xl10-tri-carrier-public-boundary-v0_1.md`. For exact inventory, inspect the selected branch/commit tree rather than `current_files.txt`. |
| 8. What must it not be treated as? | A current control plane, complete current manifest, runtime truth, authority registry, Canon, or permission to merge, retire, or delete. |

### Snapshot lineage ceiling

The initial 179-file generation is an exact full-content snapshot of the bounded XL00 source revision. `FULL_CONTENT_SNAPSHOT_OF` does not mean same identity or Git ancestry.

### Stale manifest disposition

Bounded comparison found 49 repository-native additions and `current_files.txt` coverage of `0/49`. Proposed native disposition on this branch: `HISTORICAL_MANIFEST / READER_ROUTING_SUPERSEDED_CANDIDATE`; regenerate, replace, or retire remains an OCF/W7 owner decision.

The legacy file is retained unchanged in this branch. Its historical content is not retired, and physical deletion remains prohibited.

### Return and re-entry boundary

A new reader can recover the repository role, claim ceiling, first-read pointer, and write boundary from this index plus the shield at `STATUS.md`. Re-entry remains `PARTIAL` until the role PR is independently reviewed and merged or otherwise dispositioned by the native owner; `current_files.txt` direct-path shielding and complete native-addition disposition remain open.
