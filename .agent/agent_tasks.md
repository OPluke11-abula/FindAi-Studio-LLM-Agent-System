# LAS Agent Tasks — Developer Beta Productization Track

> Active track: **Developer Agent Control Plane**
> Product goal: A developer connects a repository, approves a bounded plan, observes coding agents, verifies evidence, and receives a Draft PR.
> Roles: **Codex implements, ChatGPT reviews, Luke supervises.**

---

## Operating Rules

- [ ] Use 3–5 medium execution batches per productization phase.
- [ ] Do not create Phase 78 or any unapproved parallel roadmap.
- [ ] Do not expand scope without explicit approval.
- [ ] Do not claim tests, CI, performance, cost, or evidence that was not actually observed.
- [ ] Do not auto-merge.
- [ ] Preserve human approval before execution, scope expansion, and merge.
- [ ] Preserve local-first and fail-closed security defaults.
- [ ] Reuse existing LAS runtime, memory, governance, broker, budget, and audit components.
- [ ] Avoid duplicate orchestration subsystems.
- [ ] Keep one canonical Mission model and one canonical evidence model.
- [ ] Every phase requires focused tests, full regression, Draft PR, CI convergence, review, merge, main verification, and cleanup.
- [ ] Do not modify `.agent/memory/consensus_registry.json` unless Luke explicitly requests it.

---

# Productization P1 — Product Contract and UX Foundation

## P1.1 Product and domain contract

- [ ] Define `RepositoryProfile`.
- [ ] Define `Mission`.
- [ ] Define `MissionPolicy`.
- [ ] Define `ExecutionPlan` and `PlanTask`.
- [ ] Define `AgentAssignment`.
- [ ] Define `ScopePolicy`.
- [ ] Define `ScopeExpansionRequest`.
- [ ] Define `ApprovalGate`.
- [ ] Define `EvidenceRecord`.
- [ ] Define `VerificationGate`.
- [ ] Define `MissionCostSummary`.
- [ ] Define `DraftPullRequestDelivery`.
- [ ] Document compatibility and versioning rules.

## P1.2 Mission state machine

- [ ] Implement normal mission states.
- [ ] Implement exceptional mission states.
- [ ] Implement legal-transition validation.
- [ ] Implement deterministic illegal-transition errors.
- [ ] Record transition audit evidence.
- [ ] Test all valid and invalid transitions.

## P1.3 API and frontend contracts

- [ ] Define system readiness contract.
- [ ] Define repository profile contract.
- [ ] Define mission creation contract.
- [ ] Define plan generation and approval contracts.
- [ ] Define execution-control contracts.
- [ ] Define mission event-stream contract.
- [ ] Define scope-decision contract.
- [ ] Define verification-summary contract.
- [ ] Define Draft PR delivery contract.
- [ ] Verify backend/frontend type consistency.

## P1.4 Viewer foundation

- [ ] Add Missions top-level navigation.
- [ ] Add Review top-level navigation.
- [ ] Add Knowledge top-level navigation.
- [ ] Add System top-level navigation.
- [ ] Add mission status header.
- [ ] Add shared loading state.
- [ ] Add shared empty state.
- [ ] Add shared blocked state.
- [ ] Add shared offline state.
- [ ] Add shared error state.
- [ ] Add permission state.
- [ ] Establish responsive and accessibility baseline.

## P1.5 P1 verification and delivery

- [ ] Run focused state and schema tests.
- [ ] Run API contract tests.
- [ ] Run Viewer build and route smoke tests.
- [ ] Run desktop and mobile design review.
- [ ] Run full repository verification.
- [ ] Open Draft PR.
- [ ] Converge CI and review comments.
- [ ] Merge only after ChatGPT review and Luke approval.

---

# Productization P2 — Mission Orchestration Backend

## P2.1 Repository connection and inspection

- [ ] Support local repository paths.
- [ ] Support GitHub repository references.
- [ ] Detect base branch and repository identity.
- [ ] Detect dirty working tree.
- [ ] Detect languages and frameworks.
- [ ] Detect test commands.
- [ ] Detect CI workflows.
- [ ] Detect protected paths and architecture documents.
- [ ] Create isolated worktree safely.

## P2.2 Durable mission persistence

- [ ] Persist requirements.
- [ ] Persist repository identity.
- [ ] Persist mission policy and scope.
- [ ] Persist plan and assignments.
- [ ] Persist state transitions.
- [ ] Persist approvals and decisions.
- [ ] Persist execution events.
- [ ] Persist verification evidence.
- [ ] Persist Draft PR metadata.
- [ ] Recover mission after runtime restart.

## P2.3 Planning and approval

- [ ] Implement bounded repository inspection.
- [ ] Generate execution plan.
- [ ] Record expected files and dependencies.
- [ ] Record risk and required verification.
- [ ] Require plan approval before execution.
- [ ] Support plan revision and rejection.

## P2.4 Execution control

- [ ] Assign agent ownership.
- [ ] Enforce allowed paths.
- [ ] Enforce protected paths.
- [ ] Implement pause.
- [ ] Implement cancellation.
- [ ] Implement scope-expansion requests.
- [ ] Enforce provider and cost budgets.
- [ ] Stream mission and task events.
- [ ] Enforce no-auto-merge policy.

## P2.5 Evidence and recovery

- [ ] Record commands and exit codes.
- [ ] Record test results.
- [ ] Record changed files and scope status.
- [ ] Record architecture impact.
- [ ] Record provider calls, retry, and cost.
- [ ] Record failures and recoveries.
- [ ] Verify restart and partial recovery.

## P2.6 P2 verification and delivery

- [ ] Run dirty-worktree tests.
- [ ] Run scope and protected-path tests.
- [ ] Run pause and cancellation tests.
- [ ] Run recovery tests.
- [ ] Run approval and permission tests.
- [ ] Run provider and budget tests.
- [ ] Run API integration tests.
- [ ] Run no-auto-merge tests.
- [ ] Run full repository verification.
- [ ] Open Draft PR.
- [ ] Converge CI and review comments.
- [ ] Merge only after ChatGPT review and Luke approval.

---

# Productization P3 — Golden Path Viewer

## P3.1 System Check

- [ ] Show runtime health.
- [ ] Show Git readiness.
- [ ] Show GitHub authentication.
- [ ] Show provider configuration.
- [ ] Show workspace permissions.
- [ ] Show Ollama availability.
- [ ] Show security posture.
- [ ] Provide actionable remediation.

## P3.2 Connect Repository

- [ ] Support local path and GitHub reference.
- [ ] Show repository profile.
- [ ] Show base branch.
- [ ] Show dirty-state warning.
- [ ] Show frameworks, tests, CI, and constraints.

## P3.3 Define Mission

- [ ] Add requirement input.
- [ ] Add allowed-path policy.
- [ ] Add protected-path policy.
- [ ] Add dependency policy.
- [ ] Add database and CI modification permissions.
- [ ] Add commit, push, and Draft PR permissions.
- [ ] Add Conservative preset.
- [ ] Add Balanced preset.
- [ ] Add Exploratory preset.
- [ ] Add advanced budget controls.

## P3.4 Review Plan

- [ ] Show plan tasks.
- [ ] Show assigned agents.
- [ ] Show expected files and dependencies.
- [ ] Show risk and verification requirements.
- [ ] Show estimated call or cost range.
- [ ] Support approve, edit, reject, and revision request.

## P3.5 Execute and Observe

- [ ] Show execution graph.
- [ ] Show current task, file, and tool action.
- [ ] Show scope state.
- [ ] Show tests.
- [ ] Show provider calls and cost.
- [ ] Show retries and healing.
- [ ] Support pause, cancel, restrict scope, and escalation approval.

## P3.6 Scope Expansion Decision

- [ ] Show requested file or capability.
- [ ] Show reason, impact, and risk.
- [ ] Support allow once.
- [ ] Support add to scope.
- [ ] Support reject and revise.
- [ ] Support mission cancellation.

## P3.7 Verification Gate

- [ ] Show requirement coverage evidence.
- [ ] Show scope evidence.
- [ ] Show architecture evidence.
- [ ] Show test evidence.
- [ ] Show security evidence.
- [ ] Show quality evidence.
- [ ] Show CI evidence.
- [ ] Show cost evidence.
- [ ] Expose command, time, exit code, commit SHA, and evidence reference for PASS claims.

## P3.8 Draft PR Review

- [ ] Show requirement and plan summary.
- [ ] Show changed files and architecture impact.
- [ ] Show tests, CI, cost, and residual risks.
- [ ] Add diff review.
- [ ] Link diff to requirement, plan task, test, and evidence.
- [ ] Support create/open Draft PR.
- [ ] Support revision request.
- [ ] Support mission rejection.
- [ ] Support evidence export.

## P3.9 P3 verification and delivery

- [ ] Run component tests.
- [ ] Run route tests.
- [ ] Run Playwright Golden Path.
- [ ] Run empty, error, offline, and blocked-state tests.
- [ ] Run keyboard and accessibility checks.
- [ ] Capture desktop screenshots.
- [ ] Capture mobile screenshots.
- [ ] Run independent design review.
- [ ] Run full repository verification.
- [ ] Open Draft PR.
- [ ] Converge CI and review comments.
- [ ] Merge only after ChatGPT review and Luke approval.

---

# Productization P4 — End-to-End Integration and Official Demo

## P4.1 Official sample repository

- [ ] Prepare Python FastAPI backend.
- [ ] Prepare React + TypeScript frontend.
- [ ] Add pytest.
- [ ] Add frontend build and UI checks.
- [ ] Add GitHub Actions.
- [ ] Add fixture or small database.
- [ ] Add documented architecture constraints.
- [ ] Keep repository within approximately 5,000–15,000 LOC.

## P4.2 Official PR Risk Summary mission

- [ ] Inspect sample architecture.
- [ ] Generate bounded execution plan.
- [ ] Assign backend agent.
- [ ] Assign frontend agent.
- [ ] Assign test and verification responsibility.
- [ ] Execute in isolated worktree.
- [ ] Enforce scope decisions.
- [ ] Run verification gates.
- [ ] Create Draft PR.
- [ ] Confirm no auto-merge.

## P4.3 Evidence linkage

- [ ] Link requirement to plan task.
- [ ] Link plan task to changed files.
- [ ] Link changed files to tests.
- [ ] Link tests to evidence.
- [ ] Link evidence to verification gates.
- [ ] Link mission to Draft PR.

## P4.4 Failure and recovery scenarios

- [ ] Normal success.
- [ ] Test failure.
- [ ] CI failure.
- [ ] Scope expansion.
- [ ] Permanent provider error.
- [ ] Transient retry.
- [ ] Budget exhaustion.
- [ ] User cancellation.
- [ ] Dirty repository.
- [ ] GitHub authentication failure.
- [ ] Runtime restart.
- [ ] Partial recovery.
- [ ] Draft PR creation failure.
- [ ] Rerun after remediation.

## P4.5 Dogfooding

- [ ] Run one bounded LAS-on-LAS mission.
- [ ] Produce Draft PR only.
- [ ] Review evidence completeness.
- [ ] Record product and architecture findings.

## P4.6 P4 verification and delivery

- [ ] Run full Playwright E2E.
- [ ] Run real repository integration.
- [ ] Run GitHub Draft PR integration.
- [ ] Verify restart recovery.
- [ ] Verify task cleanup and cancellation.
- [ ] Verify evidence completeness.
- [ ] Reconcile provider calls and cost.
- [ ] Capture demo screenshots and video evidence.
- [ ] Run full repository verification.
- [ ] Open Draft PR.
- [ ] Converge CI and review comments.
- [ ] Merge only after ChatGPT review and Luke approval.

---

# Productization P5 — Distribution and Developer Beta Release

## P5.1 Distribution architecture

- [ ] Select bundled-runtime or managed-local-runtime model.
- [ ] Integrate backend lifecycle with Tauri.
- [ ] Ensure installer is not Viewer-only without explicit labeling.
- [ ] Prevent orphan backend processes.

## P5.2 First-run onboarding

- [ ] Start runtime automatically or provide managed startup.
- [ ] Add runtime health check.
- [ ] Add provider setup.
- [ ] Add Ollama detection.
- [ ] Add Git readiness.
- [ ] Add GitHub readiness.
- [ ] Add workspace selection.
- [ ] Add sample mission launch.
- [ ] Add actionable failure recovery.

## P5.3 Version and release alignment

- [ ] Inspect existing version policy.
- [ ] Align API version.
- [ ] Align Viewer version.
- [ ] Align installer version.
- [ ] Align CHANGELOG and release metadata.
- [ ] Do not invent a version without policy evidence.

## P5.4 Windows release artifact

- [ ] Build current NSIS installer.
- [ ] Generate SHA-256.
- [ ] Record artifact evidence.
- [ ] Write release notes.
- [ ] Document installation.
- [ ] Document upgrade.
- [ ] Document uninstall.
- [ ] Document data retention.
- [ ] Disclose unsigned status when applicable.

## P5.5 Fresh-machine validation

- [ ] Validate clean Windows 10.
- [ ] Validate clean Windows 11.
- [ ] Validate no preinstalled Python.
- [ ] Validate no preinstalled Node or Rust.
- [ ] Validate Ollama route.
- [ ] Validate hosted-provider route.
- [ ] Validate paths with spaces.
- [ ] Validate paths with Chinese characters.
- [ ] Validate non-admin installation.
- [ ] Validate offline startup.
- [ ] Validate upgrade from 0.1.1.
- [ ] Validate uninstall and retained data.
- [ ] Validate checksum and reproducibility evidence.

## P5.6 P5 verification and release closure

- [ ] Run full automated test suite.
- [ ] Run Viewer and runtime checks.
- [ ] Run official Golden Path on installed artifact.
- [ ] Verify no orphan runtime process.
- [ ] Verify README, CHANGELOG, versions, and artifact agree.
- [ ] Open release PR.
- [ ] Converge CI and review comments.
- [ ] Merge only after ChatGPT review and Luke approval.
- [ ] Verify main CI after merge.
- [ ] Publish Developer Beta artifact only after explicit Luke approval.

---

# Final Definition of Done

- [ ] Developer Agent Control Plane positioning is reflected in product and documentation.
- [ ] Mission state is durable and recoverable.
- [ ] Four-area Viewer navigation is implemented.
- [ ] Repository connection and bounded mission definition work.
- [ ] Plan approval is mandatory before execution.
- [ ] Scope expansion requires explicit approval.
- [ ] Execution, cost, risk, and tests are observable.
- [ ] Every PASS claim has evidence.
- [ ] Official Python + React demo reaches a Draft PR.
- [ ] Auto-merge remains disabled.
- [ ] Current runtime and Viewer ship together or are explicitly managed.
- [ ] Clean Windows installation reaches the Golden Path without manual dev-toolchain setup.
- [ ] README, CHANGELOG, version metadata, installer, and release evidence agree.
- [ ] Full tests, CI, security review, and post-merge main verification pass.

---

# Completion Statement

When all tasks are complete, report exactly:

```text
Developer Beta Productization Track: COMPLETE
Developer Agent Control Plane Golden Path: VERIFIED
Distribution status: DEVELOPER BETA READY
Auto-merge policy: DISABLED
Human approval gate: ACTIVE
```
