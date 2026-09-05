# Model-to-Window Ownership Map — Historical Failure Memory

**Lifecycle:** HISTORICAL_LINEAGE_ONLY  
**Normal Reader:** false  
**Current routing / ownership effect:** none

This file records a first-generation attempt to stabilize model behavior by assigning model families to permanent runtime windows and requiring each invocation to declare an `owner_window`.

That rule is superseded. Model, provider, agent, tool, chat, work surface, repository, or window does not own a capability merely by name or placement.

## Retained learning

The predecessor attempted to reduce drift by fixing model-to-window bindings. It helped reveal the real requirements that should be preserved without permanent ownership:

- capability fit;
- scope and affected responsibility;
- authority / rights;
- resource and disclosure boundary;
- evidence and return target;
- mismatch detection and re-resolution.

## Current successor

```text
Need
→ Stable Identity / affected slice
→ required Capability
→ eligible Provider / Actor / Carrier
→ Authority / Rights / Disclosure / Resource Gate
→ action or HOLD
→ Evidence / Return
→ Receiver / Rebuild / Exit
```

Provider substitution is lawful when the required capability and all applicable gates are preserved. No fixed ChatGPT, Codex, Jules, Gemini, model-family, or numbered-window lane is implied.

## Regression trigger

If a normal workflow again requires a model to belong permanently to a named window, or treats the model/window name as ownership or authority, classify that as predecessor resurrection.

Full predecessor mapping remains recoverable through Git history for audit and regression only.
