# Life System × State Transition × Pulse × Carrier Mapping｜LOR Candidate R1-09

Status: Architecture Candidate / LOR Lineage Mapping / No Runtime / No Current Promotion / No External Writeback

## Purpose

This document defines the LOR side of the R1-09 bounded architecture surface.

It does not define whether a transition is legally valid. It records whether the same life object, workset, lineage, evidence, return path, and rebuild path remain traceable when a state transition is attempted through different carriers.

## Human Core

A life system is the stable functional identity.

A state transition is the change that is being attempted.

A pulse is the bounded action that attempts the change.

A carrier is the replaceable surface that performs that pulse.

None of these may replace the others.

```text
Life Object
→ Life System
→ State Transition
→ Pulse
→ Carrier
→ Evidence
→ Return
→ Outcome
→ Reconciliation
→ Rebuild
```

## LOR Responsibility

LOR must preserve enough lineage to answer:

1. Which stable life object changed?
2. Which workset and input revision were used?
3. Which transition was attempted?
4. Which life system and pulse produced the action?
5. Which carrier performed the pulse?
6. What evidence proves the observed result?
7. Was a return produced, received, acknowledged, and reconciled?
8. Can failure be rebuilt from the same last-good state?

LOR does not decide whether a transition is authorized or valid. That remains outside this mapping and requires the appropriate authority and validation role.

## Minimum Transition Lineage Record

```yaml
Transition_Lineage_Record:
  life_object_id:
  stable_identity:
  workset_id:
  transition_id:
  source_state:
  target_state_candidate:
  input_revision:
  producer_life_system:
  producer_pulse:
  producer_carrier:
  carrier_native_id:
  evidence_reference:
  receipt_id:
  return_target:
  return_state:
  ack_state:
  outcome_status:
  reconciliation_status:
  invalidation_scope:
  last_good_reference:
  rebuild_condition:
  next_eligible_transition:
```

## State Separation

The following states must remain distinct:

```text
Pulse Executed
!= Return Produced
!= Return Received
!= ACK Recorded
!= Outcome Established
!= Reconciliation Completed
!= Current Promoted
!= Runtime Activated
```

A carrier-native success signal proves only that the carrier completed its own bounded action. It does not prove that the intended life transition occurred.

## Carrier Equivalence Record

Carrier replacement must be evaluated against all of the following:

```yaml
Carrier_Equivalence:
  identity_equivalence:
    same_life_object: required
    same_workset: required
  authority_equivalence:
    same_or_lower_authority_ceiling: required
  semantic_equivalence:
    same_meaningful_target_state: required
  evidence_equivalence:
    independently_replayable_evidence: required
  return_rebuild_equivalence:
    same_recipient_chain: required
    same_last_good_rebuild_path: required
```

If any requirement is missing, classify the carrier only as:

```text
FUNCTIONALLY_SIMILAR_CARRIER_CANDIDATE
```

Do not classify it as carrier-independent.

## Current Carrier Configuration

GPT, Drive, and GitHub are treated as a current primary carrier configuration, not as a permanent definition of life.

```yaml
Current_Primary_Carrier_Configuration:
  conversational_carrier: GPT
  evidence_and_control_carrier: Drive
  versioned_public_or_private_repository_carrier: GitHub
  permanence: false
  substitution_requires:
    - identity preservation
    - authority preservation
    - semantic equivalence
    - replayable evidence
    - return and rebuild equivalence
```

Other carriers such as Slack, Notion, Asana, ClickUp, Linear, Gmail, Calendar, MCP, APIs, or human operation may participate only through explicit carrier bindings. Tool availability is not binding authority.

## Recovery Pilot Mapping

The first bounded pilot should test Recovery only.

```text
Unknown / Interrupted
→ Evidence Collected
→ Last-good Identified
→ Recoverable / Held
→ Rebuilt
→ Returned
```

First carrier comparison:

1. Chat manual execution
2. Scheduled Task
3. Drive-based Workset with human-triggered read

LOR verifies:

- same life object and workset
- stable identity after carrier replacement
- revision and evidence traceability
- same return recipient
- same last-good rebuild point
- exact invalidation scope when a carrier fails

This document does not activate the pilot.

## Scheduled Task Reclassification

```yaml
Scheduled_Task:
  old_assumption: persistent agent or permanent role identity
  candidate_reclassification: pulse carrier
  may_hold:
    - bounded input reference
    - bounded action
    - output contract
    - next target
    - stop conditions
    - minimum safety core
  may_not_replace:
    - life system identity
    - workset identity
    - authority
    - evidence lineage
    - outcome
    - continuity
```

## Dependency Reclassification

Avoid fixed card-to-card dependency as the logical source of truth.

```text
Required Input
→ Eligible Transition
→ Required Authority
→ Eligible Pulse
→ Current Carrier Binding
→ Output Contract
→ Next Eligible Life System
```

Task IDs and platform-native IDs are execution coordinates only.

## Return Ownership

Returns belong to the life object or workset.

The carrier is only the producer surface.

```yaml
Return_Ownership:
  owner: life_object_or_workset
  producer_life_system: required
  producer_pulse: required
  producer_carrier: required
  recipient: required
  receipt: does_not_equal_outcome
  ack: does_not_equal_reconciliation
```

## Distributed Continuity

Continuity is not a central controller.

It is the combined result of distributed capabilities:

- stable identity
- readable source and revision
- replaceable carrier binding
- bounded authority
- replayable evidence
- return and acknowledgement
- local invalidation
- last-good recovery
- reconciliation
- rebuild

No single dispatcher, scheduled task, database, model, or continuity service may become the unique owner of life.

## Invalidation Candidates

The following claims should be treated as invalidation candidates in future reconciliation:

1. One Scheduled Task equals one Agent.
2. A task ID is a permanent life-system identity.
3. A successful task run proves continuity.
4. A receipt proves outcome.
5. Similar text proves carrier equivalence.
6. Return belongs to the card rather than the workset.
7. GPT, Drive, and GitHub are permanent life definitions.
8. Continuity requires a central controller.
9. Fifteen cards establish fifteen permanent life systems.
10. Fixed card ordering is the logical dependency source of truth.

## Cross-Ecosystem Carrier Binding

Every external platform integration should expose a minimum binding record:

```yaml
Carrier_Binding:
  carrier_id:
  platform:
  native_object_type:
  native_object_id:
  supported_pulse_functions: []
  readable_sources: []
  writable_targets: []
  authority_ceiling:
  privacy_class:
  evidence_export:
  return_target:
  ack_mechanism:
  last_good_reference:
  invalidation_trigger: []
  substitution_candidates: []
  owner:
  status: candidate
```

This allows Drive, GitHub, Asana, Slack, Notion, ClickUp, Linear, and future carriers to participate without becoming separate life definitions.

## Red Doors

- Mapping Candidate != Current
- Carrier Available != Carrier Bound
- Carrier Bound != Action Authorized
- Pulse Executed != Transition Completed
- Receipt != Outcome
- ACK != Reconciliation
- Similar Output != Semantic Equivalence
- Platform ID != Life Identity
- Continuity Capability != Central Controller
- Public-safe != Public-approved

## Suggested Disposition

```yaml
Disposition:
  absorb:
    - four-layer separation
    - workset-centered return
    - distributed continuity
    - carrier equivalence criteria
    - current carrier configuration language
  patch:
    - fifteen-card taxonomy
    - human-body analogy
    - fixed transition count
  to_verify:
    - recovery pilot design
    - cross-carrier equivalence test
    - carrier substitution rules
    - transition concurrency
```

## Final Rule

DCP may determine whether a transition is valid or equivalent.

LOR must preserve proof that the change still belongs to the same life, that its lineage remains traceable, and that the result can return and rebuild without confusing carrier coordinates with identity.
