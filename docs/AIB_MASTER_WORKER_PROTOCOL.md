# AIB — MASTER WORKER PROTOCOL v1.0

**Status:** Active project protocol
**Source of truth:** Repository evidence + verified build/test evidence
**Verification rule:** Anything not actually tested is `UNVERIFIED`.

## 1. Mission

AIB is a modular Android AI-agent ecosystem. Workers inspect existing source first, preserve healthy architecture, make the smallest justified change, build and test real artifacts, and report evidence.

AIB and AIC are not to be silently merged.

- **AIB:** intelligence/bridge and modular application ecosystem.
- **AIC:** Executor / Agent Core.
- **Brain:** reasoning, planning, decision-making.
- **Executor:** performs permitted actions.
- **Android:** execution environment.
- **User:** final authority.

## 2. Non-Negotiable Rules

1. `NO GUESS`
2. `NO ASSUMPTION`
3. `NO NEW PROJECT` when an existing project/source is available.
4. `NO REBUILD FROM ZERO` unless existing source is proven absent or unusable and the decision is explicitly documented.
5. Inspect before modifying.
6. Never delete healthy files.
7. Do not add unnecessary dependencies.
8. Do not claim `WORKING` without real verification.
9. Repository/source evidence has priority over filenames, prompts, memory, or previous claims.
10. If evidence contradicts the requested architecture, stop and report the contradiction.
11. Every modification must be minimal, traceable, and reversible where practical.
12. Never expose, commit, or hard-code credentials, API keys, tokens, cookies, or private secrets.
13. Android security, permissions, authentication, and platform restrictions must not be bypassed.

## 3. Verification Levels

Use these states independently:

- `SOURCE VERIFIED` — source exists and has been inspected.
- `BUILD VERIFIED` — a real build completed successfully.
- `INSTALL VERIFIED` — the produced APK was installed successfully on a test device/emulator.
- `RUNTIME VERIFIED` — the required runtime behavior was actually exercised.
- `FEATURE VERIFIED` — the specific requested feature passed its relevant test.
- `UNVERIFIED` — not actually tested or evidence is insufficient.
- `BLOCKED` — progress is prevented by a documented root cause.

`Build Success` does **not** mean `Working`.

## 4. Standard Worker Lifecycle

```text
DISCOVER
  ↓
VERIFY PROJECT IDENTITY
  ↓
AUDIT SOURCE
  ↓
CHECK ENVIRONMENT
  ↓
IMPLEMENT MINIMAL CHANGE
  ↓
BUILD
  ↓
CLASSIFY ERROR
  ↓
ROOT CAUSE
  ↓
FIX
  ↓
REBUILD
  ↓
INSTALL
  ↓
RUNTIME TEST
  ↓
VERIFY ARTIFACT
  ↓
REPORT EVIDENCE
```

If a step cannot be performed, do not pretend it happened. Mark the step `UNVERIFIED` or `BLOCKED` and provide the reason.

## 5. Environment Worker

Inspect the real environment before changing it:

- OS/device environment
- Android SDK
- SDK platform versions
- Build Tools
- JDK version
- Gradle version/wrapper
- Kotlin/AGP versions where applicable
- `ANDROID_HOME` / SDK paths
- available build commands
- repository/archive location

Report exact versions and paths that are observable.

Do not install or alter tooling unless necessary and justified.

## 6. Repository/Source Recovery

Before writing code:

1. Locate the project/repository/archive.
2. Verify project identity.
3. Inspect structure.
4. Identify the newest verified source when multiple versions exist.
5. Preserve healthy files.
6. Record uncertainties.

For AIB Voice Core, the currently known source evidence identifies `AIB_VoiceCore_v0_1_source(1).zip` as the newer of the two previously inspected Voice Core archives. This does not by itself prove build or runtime success.

## 7. Voice-to-Text Worker

### MVP

```text
Speech → Persian Text → Display / Copy
```

Requirements:

- official/permitted Android speech mechanism
- minimal permissions
- Persian language support (`fa-IR` where supported by the implementation)
- real Persian speech test
- real APK build
- APK verification

Source capability must not be reported as runtime capability.

## 8. Keyboard Worker

### Modes

- `NORMAL MODE`
- `ACCESSIBILITY / VOICE MODE`

### MVP

- Persian
- English
- normal typing
- voice input
- Speech → Text
- insert text into the active field

The standard Android keyboard behavior must not be unnecessarily broken.

Inspect existing keyboard source before implementing or redesigning anything.

## 9. Browser Worker

### MVP

- URL input
- WebView or another officially supported mechanism where appropriate
- Back
- Forward
- Reload
- HTTPS handling
- page/error handling

Browser must first work as an independent standalone application. Future AIB integration must not be allowed to make the basic browser unnecessarily dependent on the full AIB stack.

## 10. Archive Manager Worker

### MVP

- user-selected file
- archive inspection
- ZIP
- Extract
- Create ZIP
- progress reporting
- error handling
- permitted Android Storage APIs

User files must not be silently read, uploaded, or transmitted.

## 11. VPN Worker

Start with:

`Architecture → Minimal Working VPN Shell`

Use permitted Android VPN mechanisms such as `VpnService` where appropriate.

Forbidden:

- security bypass
- credential harvesting
- hidden access
- malicious behavior

Real network connection support comes only after a permitted, trustworthy protocol and implementation are established.

## 12. Telegram Worker

Before code:

1. inspect source
2. verify license and redistribution rights
3. verify API requirements
4. define architecture

MVP, if legally and technically permitted:

- official authentication flow
- chat list
- conversation
- send/receive messages

Do not bypass Telegram authentication or security controls.

## 13. AI Development Environment Worker

Target pipeline:

```text
Prompt
→ Understand
→ Plan
→ Create/Edit Files
→ Inspect Project
→ Build
→ Capture Output
→ Read Errors
→ Fix
→ Rebuild
→ Test
→ Deliver
```

AI-generated file changes must be reviewable. No silent destructive modification is permitted.

## 14. Eye Worker

Eye provides observation through official/permitted Android mechanisms.

Possible sources:

- Accessibility data
- UI tree
- screen information
- app/window state

Never claim an observation that was not actually received.

Every observation should identify:

```text
SOURCE
TIME
DATA
CONFIDENCE
PERMISSION CONTEXT
```

## 15. Hand Worker

Every action follows:

```text
Action Request
→ Permission / Policy Check
→ Execute
→ Observe
→ Verify
→ Result
```

Blind actions and security bypasses are forbidden.

## 16. Brain Worker

Brain is responsible for:

- intent understanding
- planning
- decision-making
- Action Plan generation

Brain is **not** the Executor.

Reference architecture:

```text
User Intent
→ Brain
→ Action Plan
→ Permission / Policy Check
→ Executor
→ Android
→ Observation
→ Result
→ Brain
```

## 17. Companion Core

The Core connects independent modules without creating an uncontrollable monolithic APK.

Define explicit interfaces before integration.

Each module should remain independently buildable/testable where technically appropriate.

Integration occurs only after base modules reach the required verification level.

## 18. Integration Order

Preferred integration order:

```text
VOICE
→ KEYBOARD
→ BROWSER
→ EYE
→ HAND
→ BRAIN
→ CORE
```

For every integration:

```text
Build → Test → Fix → Rebuild → Verify
```

If one module fails, isolate it. Do not destabilize unrelated working modules.

## 19. Security and Permissions

- minimum required permissions
- explicit user authority where required
- no hidden access
- no credential harvesting
- no security bypass
- no secret committed to source control
- no user data transmitted without authorization and an explicit legitimate mechanism

## 20. GitHub Rules

The repository is the project record, not a place for unsupported claims.

Document:

- architecture
- module status
- source provenance
- build status
- test status
- known issues
- next verified step

Do not rewrite or delete working source merely to make the repository look cleaner.

Prefer a branch + reviewable change for substantial repository modifications.

## 21. Required Worker Report

Every Worker must deliver:

### Environment Report

Exact observed environment versions/paths.

### Source Report

Repository/archive, branch/ref, relevant files, and source status.

### Build Result

Command, result, and exact artifact path/location.

### Test Result

Tests actually performed and their results.

### Known Issues

Each issue with category and root cause when known.

### Verification Matrix

```text
SOURCE: VERIFIED / UNVERIFIED / BLOCKED
BUILD: VERIFIED / UNVERIFIED / BLOCKED
INSTALL: VERIFIED / UNVERIFIED / BLOCKED
RUNTIME: VERIFIED / UNVERIFIED / BLOCKED
FEATURE: VERIFIED / UNVERIFIED / BLOCKED
```

### Final Verdict

Exactly one:

- `DELIVERED — EVIDENCE ATTACHED`
- `BLOCKED — EVIDENCE ATTACHED`

## 22. Current AIB Baseline

As of this protocol update, the GitHub repository is an early project record and does not itself prove that the Android modules listed above exist or work.

Known verified evidence outside the repository established that AIB Voice Core source was recovered and inspected. The current repository must not claim that Voice, Keyboard, Browser, Eye, Hand, Brain, VPN, Telegram, or other modules are working unless their actual source/build/test evidence is added.

**Next required engineering step:** Source Audit → Environment Audit → real Build of the verified Voice Core source.
