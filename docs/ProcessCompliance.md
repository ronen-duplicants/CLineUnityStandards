# Process Compliance Checklist for Effect Implementation

## AI/Implementor Process Compliance Checklist (MANDATORY FOR EVERY PHASE)

```diff
+ ALL AGENTS (AI & HUMAN) MUST COMPLETE THIS CHECKLIST BEFORE ANY CODE CHANGES.
+ FAILURE TO FOLLOW THIS PROCESS IS NON-NEGOTIABLE AND WILL RESULT IN REJECTED CHANGES.
```

**Before ANY code is written or changed, the implementor MUST:**

1. **Pause and reflect** – count to 10 before taking action.
2. **Get full context for the phase** – review all related .md files, debug logs, and UnityDocumentationReferences.md.
3. **Analyze all code files thoroughly** – read all relevant scripts, shaders, and assets for the phase.
4. **List all assumptions and uncertainties** – document any unclear requirements, API ambiguities, or version-specific risks.
5. **Explicitly state confidence score (1-10)** for the planned implementation.
6. **Cross-reference all API usage** with UnityDocumentationReferences.md and validate code samples for the current Unity/URP version.
7. **Update the debug log and planning docs** with findings, issues, and resolutions before proceeding.
8. **Request explicit approval** before making any code or structural changes.

### Pre-Implementation API Review Table (to be filled out before coding):

| API/Feature                | Version Confirmed | Code Sample Validated | Notes/Uncertainties                |
|----------------------------|-------------------|----------------------|------------------------------------|
| RenderGraph AddComputePass | [Yes/No]          | [Yes/No]             |                                    |
| ComputeBufferHandleMode    | [Yes/No]          | [Yes/No]             |                                    |
| SetRenderFunc<T>           | [Yes/No]          | [Yes/No]             |                                    |
| [Other APIs as needed]     |                   |                      |                                    |

### Known Issues & Troubleshooting Table:

| Issue/Challenge            | Description/Context                | Resolution/Workaround              | Documentation Updated (Y/N) |
|----------------------------|------------------------------------|------------------------------------|-----------------------------|
| Type inference for AddComputePass | Can't infer T in AddComputePass | Use explicit type, update docs     | [ ]                         |
| ComputeBufferHandleMode missing   | Not found in current context    | Check Unity version, update docs   | [ ]                         |
| [Other issues as they arise]      |                               |                                    | [ ]                         |

## Critical Process Rules

```diff
+ ALL AGENTS (AI & HUMAN) MUST PAUSE AND REQUEST EXPLICIT APPROVAL BEFORE IMPLEMENTATION.
+ NO CODE OR STRUCTURAL CHANGES WITHOUT WRITTEN APPROVAL.
```

## Phase Implementation Checklist

For each phase, all agents (AI or human) must complete this checklist:

### Pre-Implementation
- [ ] Analyze all code files thoroughly 
- [ ] Get full context for the phase
- [ ] Write or update .MD implementation plan
- [ ] State confidence score (1-10)
- [ ] List all assumptions and uncertainties
- [ ] Pause and reflect - count to 10
- [ ] Request explicit approval before implementation
- [ ] Await written approval from stakeholder

### During Implementation
- [ ] Update EffectDebugLog.md after each significant step
- [ ] Notify stakeholder before any major change or milestone
- [ ] Rate confidence (1-10) before saving any file
- [ ] Rate confidence (1-10) after saving, and after any rejection
- [ ] Validate each step before proceeding to the next

### Phase Completion
- [ ] Update EffectDebugLog.md with final phase status
- [ ] Verify all acceptance criteria are met
- [ ] Rate confidence (1-10) on phase completion
- [ ] Call out explicitly when phase is ready for check-in
- [ ] Request approval before proceeding to the next phase

## Compliance Record Template (Add to EffectDebugLog.md for each phase)

```markdown
## Process Compliance Record

### Phase X: [Phase Name]

| Compliance Step | Status | Date | Confidence (1-10) | Notes |
|----------------|--------|------|-------------------|-------|
| Analyzed code thoroughly | ✅/❌ | YYYY-MM-DD | | |
| Full context gathered | ✅/❌ | YYYY-MM-DD | | |
| MD plan written/updated | ✅/❌ | YYYY-MM-DD | | |
| Approval requested | ✅/❌ | YYYY-MM-DD | | |
| Approval received | ✅/❌ | YYYY-MM-DD | | |
| Debug log maintained | ✅/❌ | YYYY-MM-DD | | |
| Milestones flagged | ✅/❌ | YYYY-MM-DD | | |
| Phase completion called out | ✅/❌ | YYYY-MM-DD | | |
```

## Unity 2023 URP 17 Best Practices Checklist

For each implementation phase, ensure these URP 17 best practices are followed:

- [ ] Resource cleanup properly handled in `Dispose()`
- [ ] ScriptableRendererFeature lifecycle methods used correctly
  - [ ] `SetupRenderPasses()` for configuration
  - [ ] `AddRenderPasses()` only for enqueuing
- [ ] SRP Batcher compatible parameter setting
- [ ] BufferHandleMode correctly specified in RenderGraph
- [ ] No `GetData()` calls during rendering (use AsyncGPUReadback)
- [ ] Camera inputs properly configured with `ConfigureInput()`
- [ ] Counter buffers explicitly reset before dispatch
- [ ] C# and HLSL struct alignments exactly match

## Additional Documentation

See these documents for detailed information:
1. Executive Summary
2. Planning Document
3. Implementation Guide
4. Debug Log Format Requirements
5. Unity Documentation References

**Remember: Process discipline is non-negotiable at every stage.**
