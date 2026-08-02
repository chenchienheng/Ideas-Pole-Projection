# Cross-Ecosystem Carrier Federation Contract｜Candidate R0-01

Status: Candidate / Generic Coordination Schema / No Runtime / No External Writeback / No Platform Enrollment

## Purpose

This contract defines a common carrier-facing interface for ecosystems such as Drive, GitHub, Asana, Slack, Notion, ClickUp, Linear, Gmail, Calendar, MCP, APIs, and future platforms.

It does not connect, authorize, or synchronize any platform by itself.

Its purpose is to prevent every platform from inventing a separate identity, state model, return format, and completion claim.

## Human Core

The ecosystem gains value only when each platform can participate in the same life chain without becoming a separate source of truth.

Each carrier must therefore answer the same questions:

1. What stable life object does this native object represent?
2. Which transition or pulse may it carry?
3. What may it read or write?
4. What evidence can it return?
5. How is receipt distinguished from outcome?
6. Where does the result return?
7. How can the chain rebuild if this carrier disappears?

## Common Federation Chain

```text
Source
→ Stable Identity
→ Transition Contract
→ Pulse
→ Carrier Binding
→ Native Action
→ Evidence
→ Return
→ ACK
→ Outcome
→ Reconciliation
→ Rebuild
```

No carrier may skip Identity, Authority, Evidence, Return, or Rebuild merely because its native workflow reports success.

## Minimum Carrier Adapter Contract

```yaml
Carrier_Adapter_Contract:
  adapter_id:
  platform:
  native_object_type:
  native_object_id:

  identity_binding:
    life_object_id:
    workset_id:
    alias_policy:
    path_is_identity: false

  transition_binding:
    eligible_transition_ids: []
    supported_pulse_functions: []
    source_state_visibility: []
    target_state_claim_ceiling:

  source_boundary:
    readable_sources: []
    readable_revision_rule:
    forbidden_sources: []

  authority_boundary:
    authority_source:
    authority_ceiling:
    human_gate_required:
    lease_or_claim_rule:

  action_boundary:
    allowed_actions: []
    forbidden_actions: []
    stop_conditions: []

  evidence_contract:
    native_receipt_type:
    exportable_evidence:
    digest_or_revision_support:
    replay_method:

  return_contract:
    return_target:
    ack_mechanism:
    outcome_confirmation:
    reconciliation_target:

  recovery_contract:
    last_good_reference:
    retry_policy:
    duplicate_prevention:
    invalidation_triggers: []
    substitution_candidates: []

  privacy_boundary:
    privacy_class:
    redaction_required:
    public_safe_is_public_approved: false

  owner:
  status: candidate
```

## Platform Projection Examples

These examples are non-authoritative projections only.

### Drive

May carry:

- source documents
- control sheets
- bounded worksets
- receipts
- revision and pointer evidence

Must not imply:

- a filename is identity
- a folder is authority
- latest modified time is Current

### GitHub

May carry:

- versioned generic schemas
- candidate branches
- reviewable diffs
- immutable commit coordinates

Must not imply:

- commit equals Current operational state
- merged equals Runtime
- public repository equals public approval

### Asana / ClickUp / Linear

May carry:

- workset projection
- owner and next-action projection
- bounded status visibility
- return-request tasks

Must not become:

- the sole life identity registry
- the source of authority by assignment alone
- proof of outcome because a task is marked complete

### Slack

May carry:

- pulse notification
- human-readable decision surface
- bounded ACK or return request
- escalation signal

Must not become:

- a durable source of truth by message existence
- an authority grant by reaction or emoji
- a reconciliation record without an explicit binding

### Notion

May carry:

- human-readable architecture projection
- knowledge and procedure view
- linked decision records

Must not become:

- Current merely because a page is labeled canonical
- evidence authority without source lineage
- a mirror of protected source material without permission

### Gmail / Calendar

May carry:

- event-triggered pulse
- delivery receipt
- schedule rhythm
- human confirmation request

Must not imply:

- email delivery equals action completion
- calendar occurrence equals outcome
- reminder equals authority

### MCP / API

May carry:

- native reads and writes
- structured evidence
- machine-verifiable receipts

Must not imply:

- tool availability equals permission
- schema compatibility equals semantic equivalence
- successful response equals reconciliation

## Shared Status Semantics

Platform-native status labels must map into shared semantics rather than overwrite them.

```yaml
Shared_Status_Semantics:
  observed:
    meaning: native object or signal exists
  prepared:
    meaning: bounded input and action are assembled
  executed:
    meaning: native carrier action completed
  returned:
    meaning: return was emitted
  acknowledged:
    meaning: recipient acknowledged exact return
  outcome_established:
    meaning: required evidence proves target-state candidate
  reconciled:
    meaning: result was integrated into the receiving lineage
  held:
    meaning: transition cannot legally continue
  invalidated:
    meaning: declared scope no longer qualifies
```

A platform may use different native labels, but its adapter must state the mapping explicitly.

## Cross-Platform Synchronization Rule

Synchronization does not mean copying every object into every platform.

It means preserving a minimum shared envelope:

```text
Life Object ID
Workset ID
Transition ID
Source Revision
Authority Ceiling
Current State
Return Target
Evidence Reference
Reconciliation State
```

Each carrier stores only the projection needed for its role.

## Anti-Centralization Rule

No integration hub, dispatcher, database, task manager, or chat platform may become the sole owner of:

- identity
- authority
- evidence
- return
- continuity

A federation hub may route and compare bindings. It may not silently become the life source.

## Enrollment Gate

Before any platform is enrolled as an active carrier, the following must be reviewed:

1. Native object and revision behavior
2. Read and write permission boundary
3. Evidence export and replay capability
4. ACK semantics
5. Duplicate prevention
6. Failure and retry behavior
7. Privacy and public-safety boundary
8. Substitution and exit path
9. Human decision surface
10. Owner and authority source

Until then, the platform remains:

```text
CARRIER_CAPABILITY_CANDIDATE
```

not an active carrier binding.

## Red Doors

- Platform Connected != Carrier Enrolled
- Carrier Enrolled != Action Authorized
- Native Complete != Outcome Established
- Notification Sent != ACK
- Task Closed != Reconciled
- Mirrored Data != Shared Identity
- Central Dashboard != Source of Life
- Tool Available != Permission
- Public-safe != Public-approved

## Suggested Rollout Order

```text
1. Stabilize Drive / GitHub / GPT bindings
2. Validate Recovery across three bounded carriers
3. Add one task-management carrier projection
4. Add one communication carrier projection
5. Compare evidence, ACK, return, and rebuild behavior
6. Expand only after equivalence is demonstrated
```

This contract does not authorize the rollout.

## Final Rule

The purpose of federation is not to make every platform contain everything.

It is to let each platform carry a bounded projection of the same life chain while stable identity, authority, evidence, return, reconciliation, and rebuild remain recoverable across carrier replacement.
